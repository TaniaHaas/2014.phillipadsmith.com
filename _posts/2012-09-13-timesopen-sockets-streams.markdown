---
layout: post
title: 'TimesOpen: Sockets & Streams'
date: '2012-09-13 10:05:50 -0500'
category: coding
tags:
- journalism
- events
mt_id: 2859
---
<a href="http://www.flickr.com/photos/phillipadsmith/7982797923/" title="IMG_1207 by phillipadsmith, on Flickr"><img src="http://farm9.staticflickr.com/8169/7982797923_c6fdcdbf10_z.jpg" width="640" height="263" alt="IMG_1207"></a>

Nerd-Gods conspired for me on this trip to New York: I was finally in the city at the right time to catch a [TimesOpen event](https://www.nytimes.com/marketing/timesopen/) at the New York Times building. The last time I saw the inside of the Times building was more than a year ago while visiting the [R&D department](http://www.nytco.com/company/Innovation_and_Technology/ResearchandDevelopment.html), run by [Michael Zimbalist](https://twitter.com/zimbalist) and his team of geniuses, in the likes of [Jake Porway](https://twitter.com/jakeporway) and [Mathew Boogie](http://www.linkedin.com/in/mattboggie). Needless to say, the last time I left the building I felt very humbled by the speed of innovation that is happening at the New York Times, and last night's [Sockets & Streams event](http://timesopen2012sockets.eventbrite.com/) was no less humbling. 

The final presentation of the night was by [Tom Hughes-Croucher](http://tomhughescroucher.com/), co-author of O'Reilly's [Node](http://shop.oreilly.com/product/0636920015956.do) book and founder of [Jetpacks for Dinosaurs consulting](http://jetpacksfordinosaurs.com/). I instantly recognized Tom from some late-night technology talks watching; his British humour manages to liven up even the driest technical topic. In addition to the usual "you should use Node because" slides, Tom touched on some other interesting points, including:

* An upcoming [Streams](http://maxogden.com/node-streams) implementation that will address some challenges with [stream.pause](http://nodejs.org/api/stream.html#stream_stream_pause)
* [Node Domains](http://nodejs.org/api/domain.html) that will work to isolate errors and error handling within a Node application
* And, most interestingly, the question "_Do we really need 'real time'?_" (I haven't looked into this myself, but Tom implied that even the mighty Facebook still uses polling for a lot of it's application. Can anyone confirm?) and left the audience with some questions about using WebSockets with Node due to issues related to ISP proxies and caching. 

The second, and arguable most interesting, talk of the night was by [Michael Laing](http://www.linkedin.com/pub/michael-laing/3/938/98) and infrastructure architect at the New York Times. Michael walked us through his forty-year history with computing that started at the US Army, detoured through Harvard and various tech start-ups, and then landed at the Times, all of which worked to provide an interesting context for his presentation of 'fabric,' the Times' own real-time messaging framework. I wouldn't do fabric justice by trying to explain it here in a few sentences: suffice it to say that it's a massively distributed, scalable, redundant, real-time messaging framework that the Times has built out on Amazon Web Services and an impressive open-source software stack, including Erlang/OTP, WebSockets (using [Socks.js](https://github.com/sockjs/sockjs-client) to handle the various implementations, clients, etc.), RabbitMQ, Node, Python and few more that I've missed.

If you've ever wondered about the size and scale of technical challenges that a publication like the Times faces, you should Google around for some presentations by Michael and his infrastructure team. "Impressive" doesn't even cover it. Look for them at the [Amazon re:Invent](https://reinvent.awsevents.com/) conference. 

The first presentation by [Ted Hayes](http://log.liminastudio.com/) was a bit softball for the audience. Ted is a recent NYU [ITP program](http://itp.nyu.edu/itp/) graduate and, like many, is working at the intersection of computing and the physical world, with projects like a e-mail-triggered bubble gun and a WiFi-enabled joystick that controls a Web-based game of [Pong](https://en.wikipedia.org/wiki/Pong). Both interesting projects, but underwhelming without a diving into the technical details. The key takeaways for me from this presentation was a great list of hardware that people are working with in this area (pictured below), and an audience member that mentioned the [BeagleBone](http://hackerrevie.ws/2011/11/beaglebone-arm-development-kit-announced/), which is essentially a microprocessor the size of an [Ardiuno](http://arduino.cc/) that you can program with Node.js out of the box:

> "As standard, the BeagleBone will come with a pre-installed copy of the Maemo-based Angstrom Distribution, node.js and the Cloud9 IDE on a 2GB microSD card, which will combine to allow developers to quickly and easily upload new code to the board using a single USB connection for data and power."

<a href="http://www.flickr.com/photos/phillipadsmith/7982801242/" title="IMG_1209 by phillipadsmith, on Flickr"><img src="http://farm9.staticflickr.com/8309/7982801242_9313797b9c_z.jpg" width="538" height="640" alt="IMG_1209"></a>

Okay, so the most impressive moment of the evening was when the wall that divided the presentation room from the refreshments room folding up into itself like origami, thus making it possible for the nerds to socialize! I was lucky enough to run into [Brad Stenger](http://open.blogs.nytimes.com/author/brad-stenger/), one of the times developers that works "upstairs" (that is to say, not in the newsroom with Aaron Pilhofer's team), who let me know about the [Data Gotham](http://www.datagotham.com/) event that's happening today and tomorrow, and the [Penn Apps](http://2012f.pennapps.com/) hackathon this weekend. Thanks to Brad, I also met [Abe Stanway](https://twitter.com/abestanway), one of the founders of the very cool project [Hacker League](https://www.hackerleague.org/), and [Ben Gerst](https://twitter.com/bgerst), technology director at the Times.

All around great night. If you're in New York for [one of these events](https://www.nytimes.com/marketing/timesopen/), you should definitely try to make it out. And, by the way, the Times is hiring developers: if you're interested, get in touch with [Sonya Chada](https://twitter.com/recruitnytimes).
