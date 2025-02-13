---
layout: post
title: "Music Between Salen and the World"
date: 2023-05-18 21:23:12 +0200
categories: networked-music
author: Jack Hardwick, Alexander Wastnidge, Masoud Niknafs, Emin Memis, Nino Jakeli, Henrik Sveen, Kristian Eicke, Fabian Stordalen, Aysima Karcaaltincaba
image: "/assets/image/2023_05_10_henrikhs_SMC_nmp_poster_square.jpg"
keywords: portal, audio, latency, concert, jacktrip
excerpt: "We played in a global NMP concert. Check out our experiences."
---

For our final network music performance **Dispersionology and Other Tales**, we performed with musicians in several countries in a performance conducted by composer [Douglas Van Nort](https://dvntsea.com/). The concert on our side happened in Salen, our favourite in-house auditorium.

# Concept

For this telematic experience, as SMC Students, we contributed an improvisational performance conducted in the United States and performed in more than four countries.

Douglas Van Nort describes the performance as:
>"In the world of physics, dispersion describes a phenomenon in which the rate of propagation of a wave in a medium, its phase velocity, is dependent on its frequency. This can be seen in light, sound, gravity waves, etc. Its a property of telecommunications signals, including the pulses of light in optical fibre cables, describing how the signal broadens and spreads out as it moves across the channel. Dispersion therefore is inherent in the medium that more-and-more binds us these days, in the movements of light pulses that transports our attention, and our listening, around the globe. A beautiful consequence of dispersion is a change in the angle of refraction of different frequencies, leading to a prismatic opening up of a full colour spectrum from incoming light. This ability to broaden out as signals propagate through the network reflects a much wider expansion of distributed listening and sounding that is made possible in the context of telematic musicking. It occurred to me recently that, as of early 2023 I’ve engaged this medium now for 20 years, with an ear towards exploring the myriad ways that the shared real/virtual and nowhere/everywhere site of performance can act as both a point of convergence towards a singular locus of performative attention -- yet also a dispersive prism, reflecting individual voices and the preservation of creative agencies of every performer."

## Pieces
__*Tuning Meditation* by Pauline Oliveros__ An improvisational piece where every performer picks a pitch not represented at that point and plays that pitch with sustain of a breath time.

__*Dispersionology* by Doug Van Nort__
An improvisational piece whereby all locations and performers were directed/conducted/cued by Doug Van Nort.  This was either via a system of gestures which referred to a location or grouping of musicians (layers), their volume, tone vs. noise, which musical "palette"  they should respond to, as well as "sound painting", whereby musicians freely interpreted Van Norts physical actions.

__*And Other Tales* by Doug Van Nort__
An improvisational piece whereby all musicians responded to a variety of randomised on-screen prompts and images.

# Preparation

We started planning 3 weeks in advance to get ready for this big event.

In our first planning session we tried to draw an outline for our part in the concert, and our composition. We roughly decided on the performers and the instruments. We also discussed the various compositional concepts for our own piece we wanted to perform, with room for other musicians. Sadly, since we were significantly less people in the end, we decided to not to include a composition and only perform in the concert with other people.

We were also involved in a rehearsal/technical test with the other participants of the event on the Sunday evening prior, where we were able to troubleshoot audio and video routing, as well as learn in greater detail the artistic intensions, the gestures involved, and the musical palettes of the performance.


## Performers and Instruments

We performed with variety of instruments and techniques covering a wide spectral range in addition to the balance between tone and noise.

| Performer        | Instrument          |
|------------------|---------------------|
| Fabian           | No-Input Mixing     |
| Aysima           | Accordion           |
| Emin             | Ney Flute           |
| Alex             | Electronics         |
| Nino             | Vocal with effects  |
| Kristian         | Experimental Acoustic Guitar |
| Kristin Nordeval | Vocals              |

Fabian's __No-input mixer__ is a standard mixer where the outputs are connected to the inputs creating a feedback loop which is then controlled by the mixer's controls and several guitar pedals.

__Accordion__ can play both melody and bass section in a composition. For the parts lead by Douglas, accordion had different roles. While playing a musical composition like phone ringing, accordion contributed with the keyboard part and played notes in sequence. For some other parts it was better for accordion to bring sustain sounds with high or low pitches depending on the character of the composition.

__Ney__ is a _fretless_ wooden flute capable of creating both noisy and tonal sound, which enables an experimental space for its performer. With his Ney, Emin played melodic lines and noise effects during the concert.

Alex contributed __Electronics__ playing a small Eurorack modular synthesiser through delay and reverb pedals.

Nino experimented with improvisational __vocal__ performance. She processed the sound with various modulation effects with a kaleidoscopic vibrato that created strong pitch variations.

Kristin as a soprano soloist, improvised with the group in both classical and avant-garde styles.

Kristian explored unorthodox techniques for acoustic __Guitar__, laying the instrument flat, using a bottleneck to slide along the strings, tap the body of the instrument etc.  This was run through an effects chain in Ableton Live.

<figure style="float: none">
   <img
      src="/assets/image/2023_05_18_akarcaal_douglas_rehearsal2.jpg" width="100%" />
   <figcaption>Us discussing the different sound palettes that were a conceptual characteristic of Douglas Van Nort's composition</figcaption>
</figure>

# Getting Technical

In this concert, we transmitted audio using a network music performance software, [JackTrip](https://www.jacktrip.org/). We connected to a jacktrip server set up by the team around Douglas Van Nort with one of the [SMC's portable LoLa kits](https://github.com/SMC-master/NMP-Portable-Kits/wiki).

## Audio Engineering
Audio routing for this project meant allowing for a FOH stereo mix for our local audience, three foldback mixes for Oslo-based musicians, as well as sending a stereo sub-mix of our instruments to the Jacktrip server. The plot below shows the routing used.

<figure style="float: none">
   <img
      src="/assets/image/2023_05_18_alexanjw_dispersionplot.jpg" width="75%" />
   <figcaption>Audio Routing in Salen</figcaption>
</figure>

## Video Connection

During the concert, all the participants met in a Zoom call to follow Douglas' conducting and interact with other musicians. We used the Logitech PTZ meeting camera in Salen to share the video of the entire stage.

To follow the conductor and the live score, we placed two monitors on the stage in front of us: one for Douglas' video, one for the live score page. These two screens were connected to a laptop. We also projected both on the projection screen on the stage for the audience, which was connected to the stationary computer in the Salen.

<figure style="float: none">
   <img
      src="/assets/image/2023_05_18_akarcaal_douglas_performance.jpg" width="100%" />
   <figcaption>For the third piece of the performance, we setup a live sheet on the stage and followed it</figcaption>
</figure>

# Latency Measurements

Measurements have been done beforehand on two different jacktrip servers with a loopback. We used the same setup we had been utilizing for other [concerts](https://github.com/SMC-master/portal-wiki/wiki/2023-Mid-Semester-Networked-Music-Performance-in-Salen). Server 1 had a Roundtrip latency time of 188ms whereas server 2 came in on 261ms RTT. High latency times were expected and did not really affect performance since the concert and musical pieces were planned to be a latency-accepting. The final concert happened over server 1 with a global sampling rate of 44.1 kHz and a buffersize of 256 ms.

# Reflections

Despite this mode of improvisational performance being outside the experience of many in the class, it was both technically and musically executed to a standard we were pleased with. Our participation in the event went smoothly without any technical mishaps.

Watch the performance on YouTube here:

<iframe width="560" height="315" src="https://www.youtube.com/embed/Iqycm1G2M5A" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
