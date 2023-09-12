---
layout: default
---

<!-- Text can be **bold**, _italic_, or ~~strikethrough~~. -->

[Link to another page](./another-page.html).

## Abstract

Synthesizing performing guitar sound is a highly challenging task due to the polyphony and high variability in expression. Recently, deep generative models have shown promising results in synthesizing expressive polyphonic instrument sounds given music score input. They usually use a generic MIDI input representation to accommodate multiple types of instruments. In this work, we propose an expressive acoustic guitar sound synthesis model with a customized input representation to the instrument, which we call _guitarroll_. We implement the proposed approach with a diffusion-based model based on outpainting which can generate audio with long-term consistency. To overcome the lack of MIDI/audio-paired datasets, we used not only an existing guitar dataset but also collected data from a high quality sample-based guitar synthesizer. Through quantitative and qualitative evaluations, we show that our proposed model has higher audio quality than the baseline model and generates more realistic timbre sounds than the previous leading work.

## Model Overview
![](https://github.com/hanshounsu/guitar-synthesis-diffusion-outpainting/image/model_architecture.png)


## Audio examples

> This is a blockquote following a header.
>
> When something is important enough, you do it even if the odds are not in your favor.

###### Sample 1

<p style="text-align: center;">
Ground-truth &emsp; &emsp; &emsp; &emsp; &emsp; &emsp; &emsp; &emsp; &emsp; BaselineFT
</p>
<p align="center">
  <audio src='./audio_examples/03_SS3-84-Bb_comp_mix_gtr.wav' controls> </audio>
  <audio src='./audio_examples/03_SS3-84-Bb_comp_mix_bse.wav' controls> </audio>
</p>
<p style="text-align: center;">
&emsp; &ensp; OutpaintingFT &emsp; &emsp; &emsp; &emsp; &emsp; &emsp; &emsp; &nbsp; Hawthorne Demo
</p>
<p align="center">
  <audio src='./audio_examples/03_SS3-84-Bb_comp_mix_ipt.wav' controls> </audio>
  <audio src='./audio_examples/03_SS3-84-Bb_comp_mix_haw.wav' controls> </audio>
</p>


### There's a horizontal rule below this.

* * *

### Here is an unordered list:

*   Item foo

### And an ordered list:

1.  Item one

### And a nested list:

- level 1 item
  - level 2 item
  - level 2 item
    - level 3 item
    - level 3 item

### Small image

<!-- ![Octocat](https://github.githubassets.com/images/icons/emoji/octocat.png) -->
<!-- ![Octocat](https://github.com/hanshounsu/guitar-synthesis-diffusion-outpainting/audio_examples/03_SS3-84-Bb_comp_mix_gtr.wav) -->

### Large image

![Branching](https://guides.github.com/activities/hello-world/ing.png)



### Definition lists can be used with HTML syntax.

<dl>
<dt>Name</dt>
<dd>Godzilla</dd>
<dt>Born</dt>
<dd>1952</dd>
<dt>Birthplace</dt>
<dd>Japan</dd>
<dt>Color</dt>
<dd>Green</dd>
</dl>

```
Long, single-line code bbranchlocks should not wrap. They should horizontally scroll if they are too long. This line should be long enough to demonstrate this.
```

```
The final element.
```
