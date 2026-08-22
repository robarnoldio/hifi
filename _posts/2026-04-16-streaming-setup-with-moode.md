---
layout: post
title: "Streaming setup with moOde server"
date: 2026-04-16 18:44:29 -0600
categories: [audio, hifi]
tags: [setup, DAC, digital]
author: Rob Arnold
# Optional: uncomment and set if you want custom permalink
# permalink: /custom-slug/
# Optional: summary for listing pages
excerpt: Details of how modern hi-fi works with legacy stuff
---

# Streaming setup with moOde server

## Overview

Wouldn't it be cool to audition the same music presented in a modern, high-resolution bit stream and as a Vinyl LP record? That's the idea behind this project. With the aux input on my receiver, I can conveniently AB test two representations of the music, keeping the amplification and speakers parts of the signal chain constant. But getting the digital side of that correct was not as obvious as it looked.

## First prototype

My first tests were playing from Plexamp on an iPad through a pretty cheap DAC (like 10 bucks) sold as a headphone adapter for the lightning jack. Plexamp made it easy to browse my large-ish library of files on my Network Attached Storage (NAS--a Synology Diskstation). I proved the concept this way, but two things really bugged me:

- wiring the iPad to the receiver made it terribly inconvenient to use from the couch and browse the collection
- the audio quality of the cheapest gizmo in the chain (the headphone adapter) seemed likely to limit the fidelity of the digital side

## Second prototype

Then I expanded my Plexamp knowledge a bit more and determined I could remote control one Plexamp app instance from another on the same network which solved the first problem. But I wanted to hold my iPad and use it to browse. So I put a Windows laptop in the chain as a "player" Plexamp instance being controlled by the "remote" iPad instance. I needed to add the device in order to disconnect from the receiver.

I also for this prototype upgraded to a better DAC: A [Fosi Audio DAC-Q4](https://fosiaudio.com/products/fosi-audio-q4-mini-stereo-gaming-dac-headphone-amplifier). I was able to grab a working one at surplus for pretty cheap, a fraction of what it costs new. This is what I would consider a prosumer device in that it supports some decent high resolution audio standards, but not the highest, and is built on a low-cost chip unlike expensive alternatives. But the specs are good, it has a volume knob so I can level match my other sources, and maybe **good enough** for listening to 60's jazz.

![cheap and cheerful DAC](/i/IMG_1068.jpeg)

This solution worked pretty well, but I got frustrated by a few different things:

- The laptop uses a bunch of power and space compared to a tablet
- I wanted to have it available for other work at times (the big issue)
- I had to nail the power management up on that box so Windows wouldn't power it down when it idles

## Shrinking the player

My next attempts to overcome the above complaints involved recycling/upcycling some old Apple TV 2 units I had sitting around. On the plus side, they offer TOSLink digital output to the DAC. But installing Plexamp on there would at minimum involve jailbreaking the device, which I was up for but haven't done before. I did briefly set one up as an AirPlay target and use the digital output to the DAC. That **mostly** worked, but the idea that AirPlay may compress my audio was bothering me.

I also have a few older Raspberry Pi computers sitting around from earlier tinkering projects (whole house ad-blocker, network security, arcade emulation). So I went in search of a software that could do Plexamp's job of playing files stored on my NAS, but would run on the RPi. Plexamp will only support their RPi client for subscription customers, and I did not and do not want to become one of those.

And that led me to [moOde audio player](https://moodeaudio.org).

This approach fixed pretty much my whole list of gripes, is open-source unlike Plexamp, and runs well on even an older RPi model 3B like I had a few on hand. Including one I picked up for 0.25 USD at a church sale. Plus I had pretty good familiarity with the platform, unlike working on a jailbroken Apple gizmo.

Keeping a RPi on 24/7 is not a big deal, it uses about 2 Watts (measured with my kill-a-watt meter). It's got onboard WiFi so putting it on the network was a breeze, and I could locate it close to the receiver. It doesn't have a lot of other useful jobs unlike the Windows 11 laptop, so dedicating it to the music player job was an easy choice. And the combo of the moOde player stack with the USB audio support for the Fosi DAC gave me a well-controlled, bit-perfect representation of the music. 

![my new 10-year-old music player](/i/IMG_1067.jpeg)


A quick detour into bit-perfect: anything like bluetooth or AirPlay has a decent chance of altering the bit stream on its way to your ears somehow. Because those systems have goals that don't necessarily include high fidelity. I wanted to keep a wired connection for the digital audio, but wireless networking to grab the files off the NAS is fine, that's not an audible portion of the chain (so long as the file can reliably reach the player).


## The entire signal chain, visualized

Now we can look at the system diagram to see how the various parts of the system work together to achieve my hi-fi goals.

![engineers love diagrams--this is my streaming setup](/i/IMG_1106.jpeg)

This diagram is organized with the digital bits on the left, analog on the right. The DAC's job is to connect those two worlds in the way that sounds best.

The moOde player presents a web server to the network, which allows me to control it from literally any device with a browser on my home network--my phone, iPad, laptop, anything will work. I'm showing the iPad here because that was my preferred controller. Because it's wireless, I don't need to be close to the receiver any more.

The USB connection to the DAC from the RPi is configured in software--I have locked its bit depth and sample rate to 24bit/96kHz, which does require me to upsample any audio files that are at lower quality. Incidentally I also must resample any files that are **higher** resolution than this (really just the sample rate). The reason here is that the USB input, unlike the optical input of the DAC is limited to 96kHz. this is a limitation of a cheap DAC, and I accepted that in order to have a cheap DAC. I'd need to spend a couple hundred bucks to overcome that, so I decided to live with it until I felt like it became worth spending the money to overcome it.

## Next Steps

This post is long enough, so I'm not going to cover how to configure or use moOde. Stay tuned for more about the world of streaming audio though...

> Updated on 2026-04-16
