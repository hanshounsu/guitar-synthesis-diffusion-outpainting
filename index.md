---
layout: default
---

<!-- Text can be **bold**, _italic_, or ~~strikethrough~~. -->

<!-- [Link to another page](./another-page.html). -->

## Abstract

Synthesizing performing guitar sound is a highly challenging task due to the polyphony and high variability in expression. Recently, deep generative models have shown promising results in synthesizing expressive polyphonic instrument sounds given music score input. They usually use a generic MIDI input representation to accommodate multiple types of instruments. In this work, we propose an expressive acoustic guitar sound synthesis model with a customized input representation to the instrument, which we call _guitarroll_. We implement the proposed approach with a diffusion-based model based on outpainting which can generate audio with long-term consistency. To overcome the lack of MIDI/audio-paired datasets, we used not only an existing guitar dataset but also collected data from a high quality sample-based guitar synthesizer. Through quantitative and qualitative evaluations, we show that our proposed model has higher audio quality than the baseline model and generates more realistic timbre sounds than the previous leading work.

## Model Overview

<p align="middle">
  <img src="https://github.com/hanshounsu/guitar-synthesis-diffusion-outpainting/blob/main/image/model_architecture.png?raw=true" width="350">
  &emsp;&emsp;&emsp;
<!-- ![Model_Architecture](https://github.com/hanshounsu/guitar-synthesis-diffusion-outpainting/blob/main/image/model_architecture.png?raw=true){: width="500" height="500"} -->
  <img src="https://github.com/hanshounsu/guitar-synthesis-diffusion-outpainting/blob/main/image/inpainting_algorithm_5.png?raw=true" width="350">
</p>
<p style="text-align: center;">
<b>Model Architecture &ensp; &emsp; &emsp; &emsp; &emsp; &emsp; &emsp; &emsp; &emsp; Outpainting Procedure </b>
</p>

## Audio examples

> This is a blockquote following a header.
>
> When something is important enough, you do it even if the odds are not in your favor.

### Sample 1 (comp)

<p style="text-align: center;">
Ground-truth &emsp; &emsp; &emsp; &emsp; &emsp; &emsp; &emsp; &emsp; &emsp; BaselineFT
</p>
<p align="center">
  <!-- <audio src='https://github.com/hanshounsu/guitar-synthesis-diffusion-outpainting/blob/main/audio_examples/00_Rock3-117-Bb_solo_mix_bse.wav' controls preload='auto' type="audio/wav"> </audio> -->
  <!-- <audio src='./audio_examples/00_Rock3-117-Bb_solo_mix_bse.wav' controls preload='auto' type="audio/wav"> </audio> -->
  <audio src='./audio_examples/03_SS3-84-Bb_comp_mix_gtr.wav' controls preload='auto' type="audio/wav"> </audio>
  <audio src='./audio_examples/03_SS3-84-Bb_comp_mix_bse.wav' controls preload='auto' type="audio/wav"> </audio>
</p>
<p style="text-align: center;">
&emsp; &ensp; OutpaintingFT &emsp; &emsp; &emsp; &emsp; &emsp; &emsp; &emsp; &nbsp; Hawthorne Demo
</p>
<p align="center">
  <audio src='./audio_examples/03_SS3-84-Bb_comp_mix_ipt.wav' controls preload='auto' type="audio/wav"> </audio>
  <audio src='./audio_examples/03_SS3-84-Bb_comp_mix_haw.wav' controls preload='auto' type="audio/wav"> </audio>
</p>

### Sample 2 (comp)

<p style="text-align: center;">
Ground-truth &emsp; &emsp; &emsp; &emsp; &emsp; &emsp; &emsp; &emsp; &emsp; BaselineFT
</p>
<p align="center">
  <audio src='https://github.com/hanshounsu/guitar-synthesis-diffusion-outpainting/blob/main/audio_examples/02_Rock3-117-Bb_comp_mix_gtr.wav' controls preload='auto'> </audio>
  <audio src='https://github.com/hanshounsu/guitar-synthesis-diffusion-outpainting/blob/main/audio_examples/02_Rock3-117-Bb_comp_mix_bse.wav' controls preload='auto'> </audio>
</p>
<p style="text-align: center;">
&emsp; &ensp; OutpaintingFT &emsp; &emsp; &emsp; &emsp; &emsp; &emsp; &emsp; &nbsp; Hawthorne Demo
</p>
<p align="center">
  <audio src='https://github.com/hanshounsu/guitar-synthesis-diffusion-outpainting/blob/main/audio_examples/02_Rock3-117-Bb_comp_mix_ipt.wav' controls preload='auto'> </audio>
  <audio src='https://github.com/hanshounsu/guitar-synthesis-diffusion-outpainting/blob/main/audio_examples/02_Rock3-117-Bb_comp_mix_haw.wav' controls preload='auto'> </audio>
</p>

### Sample 3 (solo)

<p style="text-align: center;">
Ground-truth &emsp; &emsp; &emsp; &emsp; &emsp; &emsp; &emsp; &emsp; &emsp; BaselineFT
</p>
<p align="center">
  <audio src='https://github.com/hanshounsu/guitar-synthesis-diffusion-outpainting/blob/main/audio_examples/00_Rock3-117-Bb_solo_mix_gtr.wav' controls preload='auto'> </audio>
  <audio src='https://github.com/hanshounsu/guitar-synthesis-diffusion-outpainting/blob/main/audio_examples/00_Rock3-117-Bb_solo_mix_bse.wav' controls preload='auto'> </audio>
</p>
<p style="text-align: center;">
&emsp; &ensp; OutpaintingFT &emsp; &emsp; &emsp; &emsp; &emsp; &emsp; &emsp; &nbsp; Hawthorne Demo
</p>
<p align="center">
  <audio src='https://github.com/hanshounsu/guitar-synthesis-diffusion-outpainting/blob/main/audio_examples/00_Rock3-117-Bb_solo_mix_ipt.wav' controls preload='auto'> </audio>
  <audio src='https://github.com/hanshounsu/guitar-synthesis-diffusion-outpainting/blob/main/audio_examples/00_Rock3-117-Bb_solo_mix_haw.wav' controls preload='auto'> </audio>
</p>

### Sample 4 (solo)

<p style="text-align: center;">
Ground-truth &emsp; &emsp; &emsp; &emsp; &emsp; &emsp; &emsp; &emsp; &emsp; BaselineFT
</p>
<p align="center">
  <audio src='https://github.com/hanshounsu/guitar-synthesis-diffusion-outpainting/blob/main/audio_examples/01_Jazz3-137-Eb_solo_mix_gtr.wav' controls preload='auto'> </audio>
  <audio src='https://github.com/hanshounsu/guitar-synthesis-diffusion-outpainting/blob/main/audio_examples/01_Jazz3-137-Eb_solo_mix_bse.wav' controls preload='auto'> </audio>
</p>
<p style="text-align: center;">
&emsp; &ensp; OutpaintingFT &emsp; &emsp; &emsp; &emsp; &emsp; &emsp; &emsp; &nbsp; Hawthorne Demo
</p>
<p align="center">
<audio src='https://github.com/hanshounsu/guitar-synthesis-diffusion-outpainting/blob/main/audio_examples/01_Jazz3-137-Eb_solo_mix_ipt.wav' controls preload='auto'> </audio>
<audio src='https://github.com/hanshounsu/guitar-synthesis-diffusion-outpainting/blob/main/audio_examples/01_Jazz3-137-Eb_solo_mix_haw.wav' controls preload='auto'> </audio>
</p>

<audio controls>
  <source src='https://github.com/hanshounsu/guitar-synthesis-diffusion-outpainting/blob/main/audio_examples/01_Jazz3-137-Eb_solo_mix_ipt.wav'  preload='auto'>
</audio>
* * *


