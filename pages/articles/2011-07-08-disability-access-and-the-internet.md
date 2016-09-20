---
id: 16
title: Disability Access and the Internet
date: 2011-07-08T12:56:34+00:00
author: Rahul Gonsalves
excerpt: |
  Anybody who has ever used the internet will agree that it is an immensely useful tool; it acts as a constantly updated storehouse of information, provides societal information (and is thus an agent of democracy), facilitates interaction between people and provides recreational possibilities.
  
  For people with impairments, the internet is doubly useful; many impairments make simple tasks, social interaction and participation in civil society extremely difficult, expensive or both. Thus access to the internet for all, regardless of ability, is a prerequisite for a democratic society. However, poor coding practices and a lack of awareness on the part of web content authors on how to design for accessibility together render  large portions of the internet, in its current form, inaccessible to people with impairments.
  
  This paper will examine ways in which people with various impairments - both physical and mental - engage with online content, and will demonstrate practical ways in which authors can make online content accessible to people with disabilities.
layout: post
guid: http://rahulgonsalves.com/?p=16
permalink: /accessibility/disability-access-and-the-internet/
categories:
  - Accessibility
---
> I presented this paper in September 2008 for the National Conference on ICT for People with Disabilities, an event organised by the Computer Society of India. To do: add links and references.

## Abstract

Anybody who has ever used the internet will agree that it is an immensely useful tool; it acts as a constantly updated storehouse of information, provides societal information (_and is thus an agent of democracy_), facilitates interaction between people and provides recreational possibilities.

For people with impairments, the internet is doubly useful; many impairments make simple tasks, social interaction and participation in civil society extremely difficult, expensive or both. Thus access to the internet for all, regardless of ability, is a prerequisite for a democratic society. However, poor coding practices and a lack of awareness on the part of web content authors on how to design for accessibility together render  large portions of the internet, in its current form, inaccessible to people with impairments.

This paper will examine ways in which people with various impairments &#8211; both physical and mental &#8211; engage with online content, and will demonstrate practical ways in which authors can make online content accessible to people with disabilities.

## Impairments

While impairments span a broad spectrum, for the purpose of this paper, they fall into five broad categories: visual, hearing, speech, mobility and cognitive. Within these categories, there are broad ranges &#8211; the following section will examine them and their implications for authors in some detail.

### Visual Impairments

Visual impairments may be subdivided into three distinct categories: users with mild vision impairments (_someone who requires reading glasses, for instance_), users with severe vision impairments or who are completely blind and those who are colour blind, in whatever form. The different methods by which online content may be made accessible to each of these groups takes into account their differing requirements.

#### Poor Vision and Scalable Fonts

Users with poor vision may find using alternate fonts or larger font sizes helpful (_or essential_). Most of the popular operating systems have built-in accessibility features that allow a user to magnify part of the screen &#8211; Microsoft Windows has the Windows Magnifier and Apple’s OS X has a built-in, operating system level feature called Zoom. Most web browsers also have the ability to increase the font size and the latest versions of Microsoft Internet Explorer, Mozilla Firefox and Opera have a feature called ‘full-page zoom’, which allows not merely text but images and videos as well to be magnified.

#### Completely Blind Users and Screen Readers

Users who are completely blind use special software programs called ‘screen readers’, which convert the on-screen text into spoken audio. Popular screen readers are Freedom Scientific’s JAWS, GW Micro’s Windows Eyes and Apple’s VoiceOver (_built in to OS X_). There are several ways in which website authors can enhance a screen reader user’s experience online &#8211; I shall go into some of them at length later in this paper.

#### Colour Blindness

Lastly, colour-blindness, or the inability to distinguish adequately between different groups of colours, is a problem which affects approximately 13 out of every 1000 people. The most common forms of colour blindness are protonopia, deuteranopia, and tritanopia. People with protonopia and deuteranopia are both unable to distinguish reds and greens; in addition, for protonopes, shades of red appear darker than other comparably bright colours while tritanopes have difficulty distinguishing between blue and green.

Problems arise while building websites, when an author uses colour as a means of attaching meaning. Most commonly, colour is used as a means of distinguishing between ordinary and hyperlinked text. Colour is also used to distinguish between state changes; links change colour when hovered over, and visited and unvisited links are often differentiated solely on the basis of colour. Furthermore, the use of colour as a means of reference (_fix the errors highlighted in red_) is not uncommon. Thus in cases where colour is used to convey information, care should be taken to ensure that the colour combinations used are such that they allow users with colour blindness to perceive the difference. Furthermore, merely using colour to indicate an item will lead to problems &#8211; using additional markup (_like the strong or em tags_), or explaining the situation using text is recommended.

### Auditory

Deaf visitors to a website are often the easiest to cater to, from a website author’s perspective. Very little content on a normal website is rendered as sound &#8211; however, there are exceptions to this rule. YouTube, an online video sharing site is (_as of June 2008_) the third-most popular website in the world and allows visitors to upload and share videos with each other. Adding captioning, or a textual description to the audio component of videos on these and similar sites is a massive undertaking in terms of labour but there are few, if any, technical barriers to doing so. On rare occasions &#8211; though increasingly so, with web applications becoming widespread &#8211; sound is being used as a means of alerting users to changes on a website. Google’s webmail service has a built-in chat facility which alerts users of a new message via a chime. Deaf users, or users with their sound turned off, need to be catered to by an additional visual alert, which Google incorporates, by helpfully changing the text in the title bar to read “Rahul says&#8230;”.

### Speech

Visitors with speech impairments will rarely, if ever, find it difficult to navigate through a website, as there are practically no websites which require a user to use speech as an input mechanism.

### Mobility

While the wheelchair as a symbol of a person with disabilities is near universal, wheelchair users are of little significance in the discourse on online accessibility. Other mobility impairments, however, do impede a visitor’s ability to access websites &#8211; visitors who are unable to move one or more parts of their body (_perhaps a visitor who is quadriplegic)_ &#8211; use a range of other devices: on-screen keyboards, sip-and-puff straws, head-sticks, trackballs and so forth to engage with computers. While these devices differ significantly in the way they are operated, the important thing to remember is that they are keyboard analogues, and thus if a webpage is keyboard accessible, users of these devices are likely to be able to navigate through it. Authors should ensure that all parts of a website are keyboard accessible, including forms and rich media components.

### Cognitive

Cognitive disabilities, often termed learning disabilities, are the least understood of the various impairments, and are consequently the hardest to account for. Very broadly, they refer to difficulties that people have with comprehending or dealing with time, space, quantity, quality and cause (_Kylen, 1985_). The Web Content Accessibility Guidelines 1.0 sidesteps this decidedly non-trivial limitation with the anemic “Ensure that documents are clear and simple so they may be more easily understood”. The newer 2.0 Guidelines (_technically, the Candidate Recommendation_) are equally cryptic, specifying that if textual content require reading skills greater than the lower secondary education level, an alternate version be made available. There is some evidence to show that webpages that can be personalised to a user’s preferences, which do not contain more than ten to fifteen different elements on the same screen and which facilitate the users ability to go back to the starting point, are easily navigable by people with cognitive disabilities. In this context, links which open in different windows (_the infamous “`target: _blank`” code_) are confusing, as they disrupt the linear navigation style that users are used to, and ‘break’ the Back button. Care should be taken that if links open in new windows, this behaviour is clearly and unambiguously described.

With a clearer understanding of the various types of disabilities and their implications for web content authors, we can now move to specific technical steps that may be taken to facilitate online accessibility.

## Screen readers and supplementary benefits

Earlier in this paper, we talked of screen readers, which are software programs which blind users use to navigate web pages. Screen readers parse the content of a web page in a linear manner (_top to bottom, left to right_), and ‘read out’ the contents. They may be customised, both in the type of voice and how fast they ‘speak’. It is not uncommon for an advanced screen reader user to have theirs’ set to read out content at 300 words-per-minute.

In the following section, we examine whether it is possible to provide a more efficient experience to screen reader users by taking into account the linear manner in which screen readers parse web pages, and altering existing coding practices accordingly. Designing for screen readers has numerous spillover benefits for users with cognitive impairments as well as for search engine optimisation &#8211; after all, Google, the world’s largest search engine, is blind.

### Images and Alternate Text

WCAG 2.0 Guideline 1.1 reads: “Provide text alternatives for any non-text content so that it can be changed into other forms people need such as large print, braille, speech, symbols or simpler language”

Images, videos and other “non-text” content cannot be parsed, in their original form, by non-visual user agents, or assistive technology devices, such as screen readers, text-to-speech software and text-to-Braille hardware devices. The HTML specifications require all images to have an ‘alternate text’ or an ALT attribute. Furthermore, the HTML specification also includes an optional ‘long description’, or LONGDESC attribute, which specifies a link to a a longer description of the same content. Reading the description of an image from the ALT tag is often the only way in which people with visual impairments can engage with an image. Thus, web content authors should ensure that if an image conveys meaning, that meaning should be conveyed in text form via either the ALT attribute or the LONGDESC attribute.

_Figure 1, image with HTML markup showing correctly specified ALT _

`<img src=”images/Geese.jpg” alt=”A flock of geese in flight over snow-capped mountains” />`

### Source Ordering

WCAG 2.0 Guideline 3.2 specifies that web pages should “appear and operate in predictable ways”.

All website users rely on preconceived notions of how web-pages are ordered or must quickly form mental maps of the ordering of information on a particular web-page in order to navigate through it effectively. Visually impaired users (_or those using text-browsers or screen-readers_) cannot rely on the visual arrangement of content to help them navigate a website and thus these pre-conceived notions are especially important.

Non-visual user agents parse web-pages in a linear manner, based on the order of the HTML source code; therefore, if navigation elements appear above informational content within the source code, the user will be exposed to the navigational elements before the primary, or informational content. By separating website content from presentational data &#8211; typically achieved by using Cascading Style Sheets or CSS to lay out webpages &#8211; one can affect the way a page is laid out visually while retaining a different order within the HTML source code. The advisability of this technique has sparked debate in some fora, with some arguing for informational content to be displayed first in the source code and for navigation elements to be displayed last, and others preferring the reverse.

A study of 23 text-browser and screen-reader users (Hudson et al.) states that non-visual users unequivocally expect that “[&#8230;] the main site navigation will be presented before the informational content of the page”. This result seems to support the conclusion that navigation elements should be specified prior to the informational content of a document; however, further research with a larger study size is urgently needed.

### Structural Markup and Structural Labels

The use of structural markup is one of the best means of ensuring that an HTML document  is accessible. Structural markup refers to the appropriate use of HTML tags &#8211; for example, using a header tag to denote a heading, and a blockquote tag to denote a quotation. This allows user-agents to attach different meanings to different groups of content; visual user-agents (i.e, web browsers) often denote quotations marked up as a blockquote by indenting and italicizing the quotation, or rendering text marked up in a “strong” tag, bold. “[JAWS] &#8230;announces when long quotations, marked with the HTML ‘Blockquote’ tag are entered and exited”. Similarly, most screen readers have distinctive mechanisms to announce and navigate to different levels of headings, lists and data tables.

Structural labels identify different blocks of content using descriptive labels. While not required by the WCAG, these have been noted to enhance non-visual users’ experience. They may be ‘hidden’ from visual user agents by positioning them off-screen.

### Skip Links

WCAG 2.0 Guideline 2.4 states that authors should “provide ways to help users with disabilities navigate, find content and determine where they are”, with 2.4.1 specifying that blocks of content which are repeated over multiple web pages be bypassable. Intra-page hyperlinks, often called ‘skip links’ are used to to bypass navigational elements, or to skip to different sections within an HTML document.

Many screen-reader and assistive technology devices have built-in mechanisms that allow for intra-page navigation based on the document structure; however, familiarity with these mechanisms is usually restricted to more experienced users. Web content authors would do well to ensure that they add these skip links to pages which have a large list of navigational items on them.

### Tables

HTML originated within the scientific community and was originally intended for displaying and sharing scientific documents. In its original form it had few features to control the way a web page looked, and so as the Internet started becoming mainstream, early web designers used data tables to lay out pages. This has accessibility implications, as screen readers have to navigate complicated data tables and extract information from them. Furthermore, while screen readers parse content in a linear manner, the visual layout may be non-linear (_a two-column layout, for example_) leading to a disorienting experience for screen reader users.

Cascading Style Sheets today allow for non-linear page layouts without affecting the underlying source code, and thus web content authors should use CSS for presentation, and ensure that both visual users and screen reader users have optimal online experiences.

## Conclusion

These are merely some of the methods web content authors can use to ensure that online content is made accessible to screen reader users. As mentioned earlier, these methods have numerous external benefits &#8211; web pages built with structural markup will automatically be ranked higher by search engines and there are significant and demonstrable usability enhancements that are obtained ‘for free’ as it were, when building for accessibility. Furthermore, designing for accessibility has significant benefits for mobile devices which are increasingly being used to access the internet, especially in developing economies.

The internet can be a powerful force for empowerment, more so for people with disabilities. Web content authors need to be aware of methods by which websites may be made accessible; not only is there a strong social case for doing so but the subsidiary benefits in terms of usability and search engine ranking ensure that there is a strong business case as well for doing so. Furthermore, by becoming a signatory to (_and ratifying_) the United Nations Convention on the Rights of Persons with Disabilities, India is likely to introduce legislation that will require all electronic communication to be accessible.

## References

  * Stock, S. E., Davies, D. K. and Wehmeyer, M. K.  (2000).  _Enhancing Independent Internet Access for Individuals with Mental Retardation through Use of a Specialized Web Browser: A Pilot Study,_ Education and Training in Mental Retardation and Developmental Disabilities, 2001, 107-113.
  * Harrysson, B.  (2003).  _Web Design for Cognitive Accessibility._ Division of Ergonomics and Aerosol Technology, EAT. Department of Design Sciences, Lund University, Sweden.
  * Kaye, H.S.  (2000).  _Computer and Internet Use Among People with Disabilities._ Disability Statistics Report. U.S. Department of Education, National Institute on Disability and Rehabilitation Research.
  * Sutherland, E.  (2008).  Counting mobile phones, SIM cards and customers. LINK Center, South Africa, for the International Telecommunications Union.