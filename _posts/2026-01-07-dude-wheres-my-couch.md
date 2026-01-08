---
layout: post
title: "Dude where's my couch"
date: 2026-01-07 18:36:02 -0600
categories: [audio, hifi]
tags: [setup, acoustics]
author: Rob Arnold
# Optional: uncomment and set if you want custom permalink
# permalink: /custom-slug/
# Optional: summary for listing pages
excerpt: In which we examine my motivations for moving a large piece of furniture around
---

## Overview

I think in this post I'll attempt to describe the theory of moving my couch, and have the empirical results be a separate post. Is that because I'm too lazy to do it all today? Who can say, really?

## Comb filters

Understanding comb filter effects is a significant enough thing that my acoustics book spends the entire chapter 5 developing the theory. Let me try to cook that down to the highlights.

When a signal is present along with a delayed copy of itself, then there will be peaks that line up, making the signal louder, as well as points where a peak coincides with a valley, which will tend to cancel it out. From the time of the delay, you can predict or model where the pakes and valleys fall in the frequency spectrum.

My couch began its journey today at a distance from the wall that places my head at 18" distance from the rear wall of my listening room. We can use the speed of sound to figure that (1.5 ft) / (1130 ft/s) gives a delay of 1.3 ms between the signal that hits my ear fresh out of the speaker and the delayed reflection from the back wall. That will result in a null at 1/(2t) Hz or 376 Hz. But that's just the first null. You get one every 753 Hz. And peaks and nulls will occur evry 753 Hz after that. The closer the amplitude of the reflection is to the original signal, the more severe the peaks and nulls are.

Now, all that is very tidy for drawing on graphs and such, but can you hear those nulls? There has been some research about this, but more needs to occur. From my book, we learn that:

- Single peaks are easier to perceive than dips of the same magnitude
- Single dips an octave wide are easily perceived at 10 dB depth
- Single dips an octavve wide at 5 dB are at the threshold of perceptible
- Narrower dips are harder to perceive

These tests were done with music and speech. Frequency plays a role too, but we can kind of get a sense of how severe a null needs to be to become a real problem from these heuristics. Remeber an octave is the distance between a frequency and double that frquency, such as 200-400Hz. So maybe comb filter effects aren't super hazardous, unless they fall into the more perceptible kinds of conditions.

## Moving away

If I can't make the wall less reflective, a good strategy is to move farther from it. Today for reasons unrelated to acoustic perfection (I was changing some light bulbs) I moved my couch out and decided I would measure the effects of doing it on the reflections I get from the rear wall. Ideally, such as outdoors, you get zero reflections from behind, so nothing interferes or distorts the pristing sound arriving from in front of you. 

But getting my ladder behind the couch allowed me to move my listeing position to 36" off the rear wall. Keeping the math super simple, just double my numbers from above--the first null is at 753 Hz, with copies at every 1,506 Hz onward.

At least in theory, that rules. The null due to the reflection is now moved out of bass and into midrange territory. So I'm way less likely to perceive any comb filtering effects at making the bass or kick drum sound wimpy. And the wider spacing between those nulls means fewer of them show up across the audio spectrum. All good, at least in theory.

## Next Steps

Tomorrow I'll try to post about the actual observed result of the move. I have a way to compare the two listening positions directly, and we can go over how well theory predicts the experimental result of moving my ridiculously heavy couch around. And whether it *might not be worth the fight* to leave it where it is now.

If my explanation of constructive and destructive interference above left you unsatisfied, go check out [Audio University](https://audiouniversityonline.com/comb-filtering-explained/) where they also show some cool visual depictions of the effect, along with recordings so you can hear it.

> Updated on 2026-01-07
