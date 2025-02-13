---
layout: post
title: "Norway's First 5G Networked Music Performance"
date: 2022-07-05 08:00:00 +0200
categories: networked-music
author: Joachim Poutaraud, Kristian Wentzel, Leigh Murray, Lindsay Charles
image: /assets/image/2022_06_21_joachipo_modem.jpg
excerpt: "We played Norway's first 5G networked music performance in collaboration with Telenor Research."
keywords: Telematic, Network, NMP, Jazz
---

<figure style="float: none">
   <iframe
      width="100%"
      height="315"
      src="https://www.youtube.com/embed/UDqO1gerwL0"
      title="YouTube video player"
      frameborder="0"
      allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen>
      </iframe>
  <figcaption></figcaption>
</figure>

When it comes to playing over wide area networks such as the internet, the main problem is trying to keep a common rhythm between musicians in different locations. Maintaining a shared beat is difficult if it takes too long for one musician’s sound to reach another’s ears, and if this time (called latency) is too long (around 25ms [[1]](#references)), it can make playing music together almost impossible. However, some techniques can be employed to work with latency, and not against it.

In late spring 2022, we were engaged by [Telenor Research Group](https://www.telenor.com/innovation/research/) to perform a Network Music Performance (NMP) over their 5G network at the _Telenor Festival_. Previously, We have had extensive experience with NMP over wired networks but this was the first foray into performing over a 5G cellular network.

## **Technical Setup**

We used the Next Generation 5G platform by Telenor Research as an autonomous private network for the NMP. Telenor setted up a transmission with 80 Mhz in the C-Band with a pure _standalone 5G_ network for the occasion.

<figure style="float: none">
   <img src="/assets/image/2022_07_07_joachipo_5Ggraph.png" alt="Next Generation 5G platform by Telenor Research" title="" width="auto" />
   <figcaption><i>Next Generation 5G platform by Telenor Research</i></figcaption>
</figure>

To connect, we used a pair of [Huawei H138-380 CPE Pro 3 5G](https://nettbutikk.emcom.no/) routers and [NMP Portable Kits](https://github.com/SMC-master/NMP-Portable-Kits/wiki) to facilitate ultra-low-latency music performances between two remote locations. These portable kits are essentially bundles of high-end software, audio/video peripherals and networking tools that can provide the lowest possible latency on audio/video transmissions over the network.

### **Audio transmission**

For transmitting audio through the network, we narrowed our options to [LOLA](lola.conts.it/) Low Latency, developed by GARR and Conservatorio G.Tartini in Italy, is a unique audio-visual streaming technology, which enables musicians to play together in real-time and [JackTrip](https://www.jacktrip.org/), a popular audio transmission application developed by CCRMA at Stanford University (USA). In comparing the test results and requirements of the project, the 5G could not accommodate the buffering requirements (very small packets) to use LOLA, therefore, we had to use JackTrip which can work with larger buffer sizes [[2]](#references). We tested different parameters for the buffer and queue sizes and ended up with the following parameters.

<table>
  <tr>
    <th>Buffer size</th>
    <th>Queue buffer</th>
    <th>Latency</th>
    <th>Quality</th>
  </tr>
  <tr>
    <td>256</td>
    <td>4 (default value)</td>
    <td>125 ms</td>
    <td>Bad</td>
  </tr>
  <tr>
    <td>512</td>
    <td>4 (default value)</td>
    <td>163 ms</td>
    <td>Good</td>
  </tr>
  <tr>
    <td>512</td>
    <td>5</td>
    <td>132 ms</td>
    <td>Good</td>
  </tr>
</table>

This relatively large buffer size (512) and queue buffer (5) resulted in 53 milliseconds of latency being added at the receiving end as the audio is buffered before playback, for a total Round Trip Time (RTT) of 132 milliseconds. Regarding the network, we measured a ping delay of 6 ms with an upload bandwidth of 127.44 Mbps against a testing server ([Blix Solutions AS](https://www.blix.com/servers/)). Upload speed was significantly improved over 5G compared to the LAN (average upload speed usually corresponds to 74.96 Mbps for fixed broadband, according to [Speedtest](https://www.speedtest.net/global-index)). While downloading information is more common, NMP requires data to travel in the opposite direction as well. Playing live music on the network needs fast upload speeds in order to send data to the other musician's server.

### **Video transmission**

For transmitting video through the network, we used [OBS Ninja](https://vdo.ninja/) a cutting edge Peer-to-Peer forwarding technology that offers privacy and ultra-low latency. We disabled the audio and added the maximum resolution for the video source.

## **Setup locations : Mainstage and Villa Haraløkka**

### **Setup at the Mainstage**

The mainstage was at the Telenor HQ itself, a tent was set up next to the 5G on wheels trailer.

- [NMP Portable Kit](https://github.com/SMC-master/NMP-Portable-Kits/wiki)
- A condenser mic for the saxophone (played by Joachim)
- An SM58 mic to communicate and for announcements
- A Pair of Genelec 8030a speakers as PA system
- A Large screen for showing the video received from ‘Villa Haraløkka’
- A XA series Canon video camera

<figure style="float: none">
   <img src="/assets/image/2022_07_05_lindsay_mainstage.jpg" alt="Kristian performing at Villa Haraløkka" title="" width="auto" />
   <figcaption><i>Mainstage</i></figcaption>
</figure>

### **Setup at the Villa Haraløkka**

The Villa is located around 300 meters from the mainstage.

- NMP Portable Kit
- Two line in for the Keyboard. (played by Kristian)
- Two SM58 microphones for communication
- A pair of Genelec 8020a speakers for monitoring
- A XA series Canon video camera

<figure style="float: none">
   <img src="/assets/image/2022_06_24_joachipo_villa.jpg" alt="Kristian performing at Villa Haraløkka" title="" width="auto" />
   <figcaption><i>Kristian performing at Villa Haraløkka</i></figcaption>
</figure>
## **Performance Reflections**

Kristian and Joachim decided to play two jazz standards ([**A Child Is Born**](https://www.youtube.com/watch?v=-M2ADUgffFE) written by Thad Jones in 1969, and [**A Night in Tunisia**](https://www.youtube.com/watch?v=v3GhgSTzAxw) written by Dizzy Gillespie around 1940–42) with medium tempo as it can tolerate slight deviations in the playing of the melody and can leave some place for the development of the melody between the chords.

<figure style="float: none">
   <iframe
      width="100%"
      height="315"
      src="https://www.youtube.com/embed/WGTF7fL8w-Q"
      title="YouTube video player"
      frameborder="0"
      allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
      allowfullscreen>
   </iframe>
  <figcaption></figcaption>
</figure>

For Kristian, the tempo and style of song had a direct influence on how much latency could be tolerated. Consequently, difficulties in synchronizing timing for up tempo standards were experienced. This has already been studied in a previous blogpost on [Mastering Latency](https://SMC-master.github.io/portal/2022/02/21/joachipo-measuring-latency.html).

In preparation for this NMP, we practiced over the Local Area Network (LAN) at UiO with artificially added latency. For the ballad “A Child Is Born”, it felt quite good to perform even when we had high latency. The more rhythmic “A Night In Tunisia” was a bit harder with high latency, where Kristian had to keep the focus mostly on his own playing so as to not lose the groove.

<figure style="float: none">
   <img src="/assets/image/2022_06_24_joachipo_telenor.jpg" alt="Telenor Festival 2022" title="" width="auto" />
   <figcaption><i>Network Musical Performance in Telenor Festival 2O22</i></figcaption>
</figure>

Furthermore, there was not a significant difference in playing over 5G compared to the UiO LAN with added latency from the musicians point of view. The advantageous part of it was that the 5G had higher upload speeds compared to LAN which is mentioned in the technical section.

### References

**[1]** Carôt, A., & Werner, C. (2009). _Fundamentals and principles of musical telepresence_. Journal of Science and Technology of the Arts, 1(1), 26-37. https://doi.org/10.7559/citarj.v1i1.6

**[2]** Fasciani, S., & Tidermann, A. (2022, April 11). [5G Networked Music Performances - Will It Work?](https://SMC-master.github.io/portal/2022/04/11/aleksati-5g-nmp.html)
