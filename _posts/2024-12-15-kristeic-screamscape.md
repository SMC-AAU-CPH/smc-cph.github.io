---
layout: post
title:  "DDSP-FM"
date:   2025-02-13 23:00:42 +0200
categories: masters-thesis
author: Juan Alonso, Cumhur Erkut
image: https://juanalonso.github.io/ddsp_fm/img/anim_vae01.gif
excerpt: "Explore latent space for learning the parameters of a Differentiable FM Synthesizer"
keywords: IMS, DMI, design, thesis
---
Master Thesis, May 2021
Author: Juan Alonso
Supervisor: Cumhur Erkut
[Sound and Music Computing](https://www.smc.aau.dk/) - Aalborg University, Copenhagen

### Visit [the audio examples page](https://juanalonso.github.io/ddsp_fm/) to listen to the results.

DDSP-FM is a fork of the [official DDSP library](https://github.com/magenta/ddsp). This version includes the following new features:

* a differentiable 4-op FM synthesizer
* a differentiable AM synthesizer
* a new operator, `mult`
* a new TFRecord, suitable for future develpments, such as preset matching
* a flag for stopping the training if losses are NaN

## 💡 Timbre matching demo

[![Open In Colab](https://camo.githubusercontent.com/96889048f8a9014fdeba2a891f97150c6aac6e723f5190236b10215a97ed41f3/68747470733a2f2f636f6c61622e72657365617263682e676f6f676c652e636f6d2f6173736574732f636f6c61622d62616467652e737667)](https://colab.research.google.com/github/juanalonso/ddsp_fm/blob/master/ddsp/colab/fm/Timbre_matching.ipynb) This notebook will create a random preset for the FM synth, generate 48 pitches and train a NN that will create a patch as similar as possible as the original one, using only the spectrograms of the original preset.
