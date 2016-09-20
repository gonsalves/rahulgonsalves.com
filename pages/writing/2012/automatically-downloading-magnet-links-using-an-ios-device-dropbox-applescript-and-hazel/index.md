---
id: 21
title: "Automatically downloading .magnet links using an iOS device, Dropbox, Applescript and Hazel"
date: 2012-05-05T15:04:03+00:00
layout: post
---
People who have had the misfortune of encountering me anytime in the last two months will know that I have been on a computer automation spree; to that end have automated the process of downloading, encoding, renaming and filing all manner of media files &#8211; both audio and video. However, there was one chink in this process &#8211; which I spent the morning fixing, and have, for your viewing pleasure dear reader, outlined below.

### The Setup

I&#8217;ve got a Macbook Pro ([lyssa)](https://en.wikipedia.org/wiki/Lyssa) running 10.7, an iPhone and an iPad. I want to be able to trigger a torrent download from any of these devices and have Transmission on the Macbook Pro start the download, after which the file is kicked into a workflow for encoding/categorising which ensures that it is (theoretically) available on all my devices and in a format that allows for streaming, syncing etc.

### The Problem

Some of the larger torrent sites have, however, moved to using only [.magnet URLs](https://en.wikipedia.org/wiki/Magnet_URI_scheme "Magnet URI Scheme"), which poses problems for my [hitherto perfect system for automating torrent downloads](http://www.tuaw.com/2010/03/09/automatically-open-bittorrent-files-using-dropbox-and-hazel/) (tl;dr, Transmission watches a Dropbox folder which gets .torrent files dropped into it). The problem arises as Mobile Safari doesn&#8217;t understand how to handle .magnet links (and IMO, is unlikely to understand how to handle them anytime soon) &#8212; and even if it did, it would not allow me to start the download on my Macbook.

### The Solution

The Macbook Pro has Hazel ([which I cannot recommend strongly enough &#8212; GO BUY](http://www.noodlesoft.com/)), Dropbox for syncing and Transmission as my torrent client. The iOS devices both have [PlainText](http://itunes.apple.com/us/app/plaintext-dropbox-text-editing/id391254385?mt=8), which is a neat little program that lets you write plain text files and stores them in your Dropbox account. All these programs (except for Hazel) are free. I have a file saved in PlainText called, fittingly, &#8220;torrents.txt&#8221;.

Whenever I want to download something that catches my eye, or a file which someone has recommended, I now copy the .magnet link, and paste it into the &#8220;torrents.txt&#8221; file. Magnet URIs are simply plain text, and look similar to this:

<pre>magnet:?xt=urn:btih:bbb6db69965af769f664b6636e7914f8735141b3&dn=Ubuntu-12.04-desktop-i386.iso&tr=udp%3A%2F%2Ftracker.openbittorrent.com%3A80&tr=udp%3A%2F%2Ftracker.publicbt.com%3A80&tr=udp%3A%2F%2Ftracker.ccc.de%3A80</pre>

Hazel is set to monitor the folder which contains &#8220;torrents.txt&#8221;, with the following simple rule:

If the filename is &#8220;torrents.txt&#8221;, and if the contents of the file contain the word &#8220;magnet&#8221;, then run the following Applescript, which I have spent the morning putting together. There are probably better ways to write this, more efficient ones, but this seems to work just fine for me.

[<img class="alignnone size-full wp-image-23" title="Hazel Rules for Downloading .magnet URIs" src="http://rahulgonsalves.com/wp-content/uploads/2012/05/Screen-Shot-2012-05-05-at-3.11.58-PM.png" alt="Hazel Rules for Downloading .magnet URIs" width="681" height="527" srcset="http://rahulgonsalves.com/wp-content/uploads/2012/05/Screen-Shot-2012-05-05-at-3.11.58-PM.png 681w, http://rahulgonsalves.com/wp-content/uploads/2012/05/Screen-Shot-2012-05-05-at-3.11.58-PM-300x232.png 300w, http://rahulgonsalves.com/wp-content/uploads/2012/05/Screen-Shot-2012-05-05-at-3.11.58-PM-387x300.png 387w" sizes="(max-width: 681px) 100vw, 681px" />](http://rahulgonsalves.com/wp-content/uploads/2012/05/Screen-Shot-2012-05-05-at-3.11.58-PM.png)

`<br />
open for access theFile<br />
set fileContents to read theFile using delimiter {linefeed}<br />
close access theFile`

`tell application "TextEdit"<br />
set theString to fileContents<br />
end tell`

`tell application "Finder" to set the clipboard to theString as text`

`tell application "Transmission" to activate<br />
tell application "System Events"<br />
tell process "Transmission"<br />
keystroke "u" using {command down}<br />
keystroke "v" using {command down}<br />
delay 1<br />
keystroke return<br />
end tell<br />
end tell`

`set eof of theFile to 0`

This bit of code takes the content of the text file, copies it to the clipboard, and adds it to Transmission&#8217;s &#8220;Open Internet Address&#8221; dialog box, and starts the download. It then erases the file, leaving it ready for me to add another magnet link.

&#8230;there you have it. It&#8217;s neither complex, nor terribly elegant, but it&#8217;s reliable and scratches this little itch that has been bothering me for a while. I hope to extend this to being able to handle multiple .magnet URIs (requires parsing the text file as a list and looping/repeating the process &#8212; too much for a Saturday morning!).