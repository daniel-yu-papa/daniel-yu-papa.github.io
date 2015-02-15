---
layout: post
title: "The Birth of Maggie OpenMax Library"
description: 
category: multimedia
tags: [magomx]
imagefeature: 
comments: true
share: true
---

The [Maggie OpenMax Library v0.1](https://sourceforge.net/projects/maggieopenma/files/latest/download) just released several days ago. So it is the right time to review it and give out the plan for next step.

<!--more-->

I'v been working on several multimedia processing projects for embedded platform; for example video surveillance encoding/decoding streamer, media player for set-top-box/dongle etc. Even though the hardware platforms are quite different, the data flow and control flow are similar from the application point of view. However, given the code base, nothing common could be found at all. Not much software modules could be re-used in the future development. What a huge lost of time and human resoures with such developing practice!

Then here comes the OpenMax specification, which is trying to build up the multimedia processing framework to lighten the burden of programmers. Hence the developer could just focus on the coding related to the different embedded platform. What's more, It enables the user to construct graphs of media-handling components in terms of their requirements. It becomes as easy as building the Lego as children's slide, seesaw and even the kindergarden. How wonderful it is!

Yes, it is really what gstreamer does. however, the initial motivation of gstreamer is not for embedded system specific though it could be used for that purpose. It appears to me that gstreamer is almighty but too complicated for the embedded system, specially for those resources limitted systems.  Correct me if i was wrong!

That's why i decided to develop the lightweight multimedia framework in terms of the OpenMax spec. Below are the design targets i am trying to achieve:

1. Easily ported to different embedded platforms
9. Small and customized system footprint
9. Rely on the third party open source projects as less as possible
9. Architect the software in Object-oriented way by programming with C

This is the Maggie OpenMax library and another part of the software is the MagPlayer, which is based upon OpenMax IL library. MagPlayer is actually coming from my another project and later on i will refactor it into the OpenMax content pipe architecture. For now, the MagPlayer is used as the Demo player to present the capabilities of the Maggie OpenMax library. The MagPlayer exposes few APIs to application to implement all playback related functionalities.  