---
id: 14
title: 'Acknowledging the Elephant in the Room &#8211; Moving Toward Media Accessibility'
date: 2011-07-08T12:13:57+00:00
author: Rahul Gonsalves
excerpt: 'Accessibility evangelists have long touted the ease with which inaccessible online content may be made accessible - merely convert your nasty, table-based website to spanking clean HTML and CSS, sprinkle on a few skip links and and you were home scot free. However, the accessibility of online media - videos, audio and interactive presentations which combine the two - has been carefully ignored and cannot be solved via technical means alone.'
layout: post
guid: http://rahulgonsalves.com/?p=14
permalink: /accessibility/acknowledging-the-elephant-in-the-room-moving-toward-media-accessibility/
categories:
  - Accessibility
---
> Note: [This article was originally written in August 2008, for A3](http://a3.barrierbreak.com/media2008.php), a newsletter published by [Barrier Break Technologies Ltd](http://www.barrierbreak.com/).

Accessibility evangelists have long touted the ease with which inaccessible online content may be made accessible &#8211; merely convert your nasty, table-based website to spanking clean HTML and CSS, sprinkle on a few skip links and and you were home scot free. The argument was a compelling one &#8211; multiple groups of people with impairments _(screen reader, keyboard and assistive technology device users)_ benefit from these technical fixes, it makes for an elegant and easily-digested business case and more over, can be carried out relatively cheaply.

However, the accessibility of online media &#8211; videos, audio and interactive presentations which combine the two &#8211; has been carefully ignored and cannot be solved via technical means alone. No amount of tinkering with source code is going to make them accessible to people who cannot see, hear or who are deaf-blind. The solution is obvious &#8211; captioning is needed for those who cannot hear while text descriptions which can be both accessed on a Braille device and converted to speech are required for the deaf-blind and the blind respectively.

Three problems exist: firstly, adding captions and writing text descriptions involves a significant amount of effort; secondly, it is often unclear &#8211; even in countries where accessibility legislation exists &#8211; whose responsibility it is to provide these alternatives; and lastly, even in the rare case where there are content authors who are willing to add captioning to media, there are further technical issues which harken back to the Dark Ages of web design &#8211; multiple, incompatible _(proposed)_ standards, fragmented or non-existent application support and little or no adoption by content creators.

What is urgently needed is to standardise on a file format for captions, encourage application vendors to adopt it and to ensure that tools that produce these files exist and are used. The World Wide Web Consortium’s proposed standard, [Synchronized Multimedia Integration Language](http://www.w3.org/TR/REC-smil/) (SMIL), an XML-based language that allows authors to “describe multimedia presentations”, is one possibility. It uses an XML-like syntax and is thus easy to repurpose existing editors to generate these files.

Secondly, there is a need to educate content authors on best practices for captioning. Captioning is a far more comprehensive exercise than subtitling _(which merely involves translating dialogue for hearing viewers who do not understand the original language)_. Captioning describes sound effects, moves to indicate who is speaking _(thus requiring the ability to add layout or positioning information, which SMIL provides)_ and may be displayed on an assistive technology device (_text-to-speech convertor, refreshable braille device, etc_).

Media accessibility is often carefully swept under the carpet; however, there is an urgent need to start addressing it’s absence. Large portions of the internet otherwise risk becoming unavailable including incredibly popular websites like Youtube (_currently ranked the third-most popular website in the world_) &#8211; to visitors with impairments.

Most people with impairments would benefit greatly from the greater social participation that access to these resources would give them. Furthermore, the [United Nations Convention on the Rights of Persons with Disabilities](http://www.un.org/disabilities/default.asp?id=150) has been signed and ratified by a large number of countries, India included. It is time for accessibility evangelists to move away from the low-hanging fruit of web standards towards advocating rich media accessibility and for content creators to embrace media accessibility best practices.