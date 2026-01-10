---
layout: post
title: "See how it sounds"
date: 2026-01-08 18:36:17 -0600
categories: [audio, hifi]
tags: [setup, measurement, acoutsicts, REW]
author: Rob Arnold
# Optional: uncomment and set if you want custom permalink
# permalink: /custom-slug/
# Optional: summary for listing pages
excerpt: Haha any dumbass knows you can't see sound
---

## No really this is kind of the entire point

The best reason to take these absurdly detailed acoustic measurements in your room is so you can see and more easily perceive defects in your listening setup that you can (ideally) do something about. Hopefully you do something that makes it better. And hopefully you show with additional measurements that it *is* better, and how much better. And onward and upward.

## OK, so you moved your couch

The first question under consideration is "did it help or hurt" and for that evaluation we're gonna use Room EQ Wizard (REW). I blathered endlessly about why it should be a good idea in a previous post, but now we get to find out if it really was a (measurable) improvement. Because confirmation bias is a hell of a thing.

## Quick detour: confirmation bias

Confirmation bias works against all of us in subtle ways. I think of it as a bug in human firmware. You can know you suffer from it, which is better than not knowing, but you can't just turn it off. It's not really a weakness or a defect, but it's there and it has real effects.

How confirmation bias works is you show up to any evaluation with some prior beliefs about how things work. And you go ahead and collect some observations in order to form some conclusions. And your brain has evolved to have a tendency to disregard the observations that don't confirm your prior beliefs, and give more significance to the observations that do.

## C'mon man, make wth the graphs

All right, this is what I started this blog for after all.

![SPL chart comparing two listening positions](/i/couch-effect-spl.png)

This chart illustrates the measured SPL at the listening position for two different placements of my couch. Yellow trace shows away from the back wall, blue is closer to the back wall (where a normal person would put their couch). When I measured, I actually did *six* sweeps, even though I'm showing you two of them. The L and R channel behave distinctly differently, and those differences can be diagnostic when it comes time to evaluate correcting problems. So I gathered more details than I am showing you right now.

Very impressive, but what do we learn from this picture? Imagine for a moment a perfect frequency response, where the room contributes nothing and the speakers were absolutely ideal at all frequencies--that would appear as a horizontal line. So you can think of any deviation from that ideal as a defect. One of the challenges is identifying and corrrecting that defect (okay that's two of the challenges). Let's focus on identifying: when the line drops a bunch, that's a null. That means that *at the listening position,* there's a drop in the amplitude at a speciific frequency (shown on the x-axis of our chart), and it's kind of up to us to determine why (comb filter, room mode, or maybe some other thing we aven't talked about).

The wider and deeper that notch on the chart is, the likelier that it is a *perceptible* defect in the sound. Especially in the higher frequencies, a lot of variation is expected and not particulary significant in terms of a perceptible effect on our music. To get more specific, we are hunting bass-sucking effects. So we can adjust the chart limits and "zoom in" a bit on the area from 20 Hz to 600 Hz. Which I have done before exporting this chart (I certainly measured the room up to 20kHz, and those numbers are in the file REW saves).

Two features present themselves as worth some investigation: there are notches at 90 Hz and 125 Hz. You can point at the one between 40 and 50 Hz, but it affects both positions, so it's a little less interesting to investigate to me (maybe my speakers are contributing that, or perhaps any other thing that's not couch placement). Notice that the overall SPL is higher for the closer listening position--I was quite careful to leave everything else the same as I varied my listening position between measurements. Sounds get fainter as you move away from them (a thing you certainly knew before you got here).

Let's investigate the 90 Hz notch. The procedure here is grabbing my handheld sound meter and kind of moving it around in space to see (and hear) how localized that notch is (spoiler: super localized). To really make the demo vivid, the input signal is a sine wave at 90 Hz, which is free of information that is *not* going to trigger that effect. We're expecting a big change in the meter reading as we get to the listening position (where the yellow curve measurement above was taken).

<video controls preload="metadata" width="640">
  <source src="/i/sine-test.webm" type="video/webm">
  <source src="/i/sine-test.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>

The effect is quite vivid, around 15 dB lower, which tracks what we see on the graph nicely. It's quite a bit worse when only the Right channel is putting energy into the room. Having the Left speaker also provide the test signal lessens this notch, but also reflects how I would normally use my system.

Other waveforms besides sine waves have additional frequencies (harmonic content) besides the fundamental. And that generally inclused real world musical instruments of all sorts and vocalists. So I'll repeat the test but with a sawtooth wave. The harmonics aren't affected by the notch, only the fundamental is. And human hearing is quite amazing--it [infers](https://en.wikipedia.org/wiki/Missing_fundamental) the presence of the fundamental from the harmonics, even when the actual signal is not there. That's really wild, and we knew about this in the 1950's.

<video controls preload="metadata" width="640">
  <source src="/i/saw-test.webm" type="video/webm">
  <source src="/i/saw-test.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>

As a final demo and to maybe point more at the audible effect of the notch, check out the same procedure done with pink noise as a source. More so than watching the meter change numbers, listen for the sound changing as I move. This happens in just about any real listening environment--where you are can make very perceptible sound changes.

<video controls preload="metadata" width="640">
  <source src="/i/noise-test.webm" type="video/webm">
  <source src="/i/noise-test.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>

You, the alert reader, undoubtedly noticed that I called out a 77 dB reading when the meter shows 71 dB (until I started yapping).

So we measured this, we confirmed our measurement with some further testing, and now we need to evaluate--is this a problem that is worth correcting? Did I move my heavy couch for nothing? Are we winning?

I haven't reached a final conclusion just yet, but I think the 90 Hz notch at the forward position bugs me more than the 125 Hz notch with the couch back. Maybe I can find a middle placement that avoids both of them (and ideally won't introduce something more obnoxious). I did a similar checkout with the 125 Hz notch, but I won't bore you with the videos. It occupies a much narrower slice of the spectrum, and it's less noticeable even though in absolute measurement terms it's lower. 

## Next steps

This thing is getting kind of long, so I'll let you know what I have concluded so far, what additional investigation I want to do, then I'll wrap this up. I think both couch positions are defective, but neither one is unacceptable. I also suspect that splitting the difference could keep me away from sitting right in the 90 Hz notch. That suggests another set of measurements to be taken with the LP at about 27" off the rear wall. As lnog as that doesn't introduce a worse null, it will avoid both of these. The narrower but deeper notch is way less perceptible with musical content. Not even close. So the current best case is the 18" from wall spot, but I want to test and see if 27" beats it.

> Updated on 2026-01-08
