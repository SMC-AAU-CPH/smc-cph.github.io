---
layout: post
title: "Performing & Recording with JackTrip"
date: 2022-11-27 10:00:00 +0200
categories: networked-music
author: Jack Hardwick
image: /assets/image/2022_11_27_jackeh_jacktrip_performance_recording_preview_image.jpg
keywords: jacktrip, LOLA, performing, recording, network-musical-performance
excerpt: "Performing and recording network music at home? Thanks to JackTrip, now you can do it too."
---

## What is a Network Musical Performance?

A network musical performance or NMP is a musical performance that happens over a network, be it a private network or a public one like the internet. In SMC we spend a lot of time experimenting with various software for performing and rehearsing network music. Two of our most used solutions are LOLA and JackTrip. First let's briefly compare them, and then we will dive deeper into JackTrip.

## LOLA and JackTrip

In SMC we most commonly use [LOLA](https://lola.conts.it/) for our network performances. The advantages of LOLA are many – with an ideal network, such as the LOLA network we use at UiO, we can stream uncompressed audio and video between two to three locations. This is just what we need for these concerts in which high production values are essential.

However, LOLA requires specific cameras and audio interfaces as well as powerful PCs to perform optimally, meaning it is mostly limited to performance scenarios over a dedicated network. What if we want to rehearse a larger ensemble across the internet on the go? What if we can do without low-latency video? Step forward [JackTrip](https://www.jacktrip.org/).

Unlike LOLA, JackTrip does not support video, but neither does it require specific hardware. It is available for Windows, Mac and Linux and can support a far higher number of participants. Testing has shown that it can support up to 500 participants connecting to a single JackTrip server. Check out [this article](https://25ms.org/2020/07/21/scaling-to-254-and-beyond/) for more details on that experiment. As with LOLA, a limiting factor will always be the network itself. Any client connecting to JackTrip with a poor connection will both send and receive with latency.

<figure style="float: none">
   <img src="/assets/image/2022_11_28_jackeh_jacktrip_interface.jpg"/>
   <figcaption>The JackTrip user interface</figcaption>
</figure>

Now let's take a look at some of the performance and recording possibilities afforded to us by JackTrip.

## Performing with JackTrip

During the recent COVID lockdowns, many ensembles tried their hand at remote performances and recordings. Anyone who attempted this through Zoom will be intimately familiar with the chaos that can ensue due to latency. However, by combining video through Zoom (other videoconferencing solutions are available) with audio through JackTrip, we can maintain the visual element of a concert while also opening the door to low-latency audio, allowing for real-time performances despite physical separation.

Take a look at this JackTrip performance featuring almost 100 performers:

<iframe width="600" height="338" src="https://www.youtube.com/embed/SJgB5QmyDfU" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

## Recording with JackTrip

We can take advantage of internal audio routing within our laptops to record high-quality audio received over the network into a DAW. In Windows, JackTrip provides a handy utility called JackRouter, a virtual audio device which we can use to send and receive audio between the JackTrip and a DAW. It appears as a send and receive location in the JackTrip patch bay, at which point one can simply send channels to it to receive them in a DAW using JackRouter as its audio device.

In our own testing with JackTrip in SMC4024, my fellow SMC student Kristian and I recorded two channels, one local and one from the network, while also sending out a drum track for us over which we would both improvise. We routed my microphone connected via XLR into an audio interface and Kristian’s synth received over the network into JackTrip and out into Ableton via the JackRouter receive patch point. There I recorded both of our instruments directly to Ableton audio tracks. Both of these received channels plus the pre-recorded drum machine track were then all routed back into JackTrip through the JackRouter receive. This allowed us to monitor ourselves and the drums with negligible latency, while also recording the whole session.

<figure style="float: none">
   <img src="/assets/image/2022_11_28_jackeh_jacktrip_routing_diagram.png"/>
   <figcaption>The JackTrip routing for the above setup. Note both live audio sources being sent into Ableton and out again before going to our headphones.</figcaption>
</figure>

See the result of our experiment in the video below:

<figure style="float: none">
  <video width="75%" controls>
    <source src="https://www.uio.no/english/studies/programmes/SMC-master/blog/assets/video/2022_11_28_jackeh_jacktrip_recording_demo.mp4" type='video/mp4'>
  </video>
  <figcaption>JackTrip performance over the LOLA network</figcaption>
</figure>

We recorded the video separately but simultaneously using our laptop webcams because we were unable to access the internet, and therefore Zoom, while also being connected to the LOLA network. While is this not an issue if you are using JackTrip over the internet, in our case it meant we could not communicate visually while recording. As a result it did dampen the feeling of a live performance somewhat.

We found JackRouter to be the easiest solution for internal audio routing on Windows when using JackTrip. JackRouter is unfortunately Windows-only for now, but the above can also be replicated on other operating systems using audio routing utilities such as BlackHole on Mac.

## Conclusion

JackTrip opens up a wealth of possibilities for network music performance and recording between many participants. I highly recommend you give it a try!