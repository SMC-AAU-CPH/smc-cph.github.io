---
layout: post
title: "Experiencing Ambisonics Binaurally"
date: 2019-05-19 09:00:00 +0200
categories: networked-music
author: Guy Sion
image: https://www.uio.no/english/studies/programmes/SMC-master/blog/assets/image/2019_05_19_guysi_ambisoniclogo.png
excerpt: "During the SMC2022 Physical-virtual communication course we have had two sessions where we explored multichannel and ambisonic decoding. The first session, on February 27th, was mainly about recording a four channel A-format stream with an Ambisonic 360 sound microphone. We converted the A-format mic signal into a full-sphere surround sound format which was then decoded to 8 loudspeakers layout we placed evenly across the portal space. We have used the AIIRADecoder from the free and open source IEM plug-in suite."
Keywords: Ambisonics, Music, Technology, Max4Live, Binaurally, E4L, Giant Steps
---

![Logo](https://www.uio.no/english/studies/programmes/SMC-master/blog/assets/image/2019_05_19_guysi_ambisoniclogo.png "Logo")

During the SMC2022 Physical-virtual communication course we have had two sessions where we explored multichannel and ambisonic decoding. The first session, on February 27th, was mainly about recording a four channel A-format stream with an Ambisonic 360 sound microphone. We converted the A-format mic signal into a full-sphere surround sound format which was then decoded to 8 loudspeakers layout we placed evenly across the portal space. We have used the AIIRADecoder from the free and open source <a href="https://plugins.iem.at/" target="_blank">IEM plug-in suite</a>. Although the setup was not ideal, mostly because of the LOLA connection between the Trondheim and Oslo portals, and the fact that the loudspeakers were not at the same level of the listener’s head, we did manage to get a 3D spatial sound stream between the two campuses.

For our second session on April 24th, we focused on decoding binaurally the input from four large diaphragm condenser microphones placed in a square formation. It required us to use headphones for a better perception of the sound stream and enhanced immersive environment. The decoding was done this time with <a href="http://www.envelop.us/software" target="_blank">E4L (Envelop for Live)</a> free collection of spatial audio production tools. We created four audio channels and placed the E4L Source Panner device on each of the audio tracks. On a fifth audio track, we set the E4L Master Bus device and directed all output from the four microphones into that channel. You can see the setup we have used in Ableton Live in the pictures below.

![1](https://www.uio.no/english/studies/programmes/SMC-master/blog/assets/image/2019_05_19_guysi_amb1.png "1")

![2](https://www.uio.no/english/studies/programmes/SMC-master/blog/assets/image/2019_05_19_guysi_amb2.png "2")

![3](https://www.uio.no/english/studies/programmes/SMC-master/blog/assets/image/2019_05_19_guysi_amb3.png "3")

![4](https://www.uio.no/english/studies/programmes/SMC-master/blog/assets/image/2019_05_19_guysi_amb4.png "4")

![5](https://www.uio.no/english/studies/programmes/SMC-master/blog/assets/image/2019_05_19_guysi_amb5.png "5")

![6](https://www.uio.no/english/studies/programmes/SMC-master/blog/assets/image/2019_05_19_guysi_amb6.png "6")

We were given the time to experiment with this setup. Several class members have started to whisper, talk loudly or sing into their dedicated microphones, trying to create unique sonic material for the listeners who wore headphones in Trondheim and Oslo. I seized on the opportunity to play the saxophone with this ambisonic setup and resorted to the Giant Steps melody which seemed to be a recurring theme whenever I am being asked to play something (have you checked out my <a href="https://SMC-master.github.io/sound-programming/2019/02/11/Giant-Player.html" target="_blank">(Giant Steps Player already?).</a>

<p>I stood in the middle of the four-microphone setup and played into each of the mics at a time. During the first round of the melody, I played segments of the song into each different mic, and for the second round of the tune, I played (almost) each note into a different mic. That resulted in an audio clip where you can hear me play parts of the melody in four positions (Front-Right, Front-Left, Back-Right, Back-Left). I would recommend listening to this audio clip with headphones to be able to clearly identify the direction I am playing from (from the listeners perspective).

<figure align="middle">
   <audio controls>
     <source src="https://docs.google.com/uc?export=download&id=1xhMuN5UaaoMb17ZL2lCtVsPyNd4t_W4N" type="audio/mpeg" volume="1.0">
     Your browser does not support audio tag.
   </audio>
</figure>

<p>When listening to it again in a quiet environment at home, I now wish I had more time to experiment with playing longer tones while moving between the microphones (maybe a ballade would fit better next time?). I wanted to hear the movement of my sound in the spatial environment.

<p>In any case, I decided to continue the extermination at home with several sound effects like footsteps, a clock ticking and writing marker. I placed all sound samples on an audio track containing the E4L Source Panner device and mapped the Azimuth knob to a physical knob on my midi controller.

<p><center><iframe width="560" height="315" src="https://www.youtube.com/embed/bTKGFT1Ivxk" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe></center>

<p><center><iframe width="560" height="315" src="https://www.youtube.com/embed/A5nIflG8a6Y" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe></center>

<p><center><iframe width="560" height="315" src="https://www.youtube.com/embed/2Sh4TgIk4vY" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe></center>

<p>Give it a listen (with headphones of course) and see what you think! The Envelop for Live free tool pack has some great collection of devices which can really utilize space as a compositional element, and it would be interesting to see how this type of devices can elevate my artistic output in the future.
