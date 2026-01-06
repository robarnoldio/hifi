---
layout: post
title: "Talking about measurement"
date: 2026-01-06 08:30:25 -0600
categories: [audio, hifi]
tags: [measurement, audio]
author: Rob Arnold
# Optional: uncomment and set if you want custom permalink
# permalink: /custom-slug/
# Optional: summary for listing pages
excerpt: In which we discuss precision, accuracy, and dimensions
---

# Talking about measurement

## Terms and conditions

One of the things that makes this a technical blog instead of some random crank expressing opinions is that I will try my best to precisely use technical terms and units to describe the things I'm talking about. So, a random crank *with an engineering degree* expressing opinions *with precision*. With the caveat that I don't work in the engineering field.

On this page, I'll try to condense down the most important parts that I learned from an entire course I took called "Electrical measurements" and combine that with a few things from audio engineering and from music theory that I thing will help us have that more precise conversation. Maybe this page can be a helpful guidepost in later posts.

## Things to know about measurements

Measurements have error. Error is the difference between the true quantitiy and the measured quantity. Error can be observational or systematic.

> If a 1kg calibrated reference mass gives you a scale reading of 999g, that is a 1g error. If the error is consistent across repeated measurements, that is systematic error. If my scale isn't clean because I was making bread and got four on it, that could be a source of observational error. My coffee scale (which I love and use for all kinds of things) is rated to be accurate with a one gram error in the range from 500-2000g (see the tiny writing on the scale).
![scale getting calibrated kind of](/i/IMG_0337.jpeg) 

People who take measurements seriously tend to state the uncertainty in their measurements, in order to convey both the accuracy and precision. We could say that scale reads 1000g &plusmn;1g. 

Even without a statement of uncertainty, the number of significant digits in a measurement can imply a precision. We can say that scale reads 1.00 kg or 1.00 x 10<sup>3</sup>g to express 10 gram precision, or 1.000 kg or 1.000 x 10<sup>3</sup> g to express 1 gram precision.

Okay, what's up with the exponents? If you are bummed out by the 10<sup>3</sup> notation, just know that it is very convenient when the quantities vary fairly widely over a range, and allows expression of the precision separately from the magnitude, and also make it much easier to multiply (or divide) numbers by adding (or subtracting) their exponents. 4.2 x 10<sup>8</sup> / 2 x 10<sup>3</sup> is easy to do in your head: divide the coefficients (4.2 / 2 = 2.1) and then subtract the exponents (8 - 3 = 5) giving you 2.1 x 10<sup>5</sup>.

## Electrical quantities to know

- Volt: Measures the electical potential difference between two points. 
- Amp: Measures the magnitude of the electrical current, which has a direction.
- Watt: Measures the electrical power; eual dimentionally to current x voltage.
- Ohm: Measures the resistance to the flow of current or impedance to a time-varying current. The abbreviation is &Omega; (capital omega--we use lowercase for different things)
- Hertz: Measures frequency; equivalent to "per second" or s<sup>-1</sup>.

## Audio quantities to know

- Frequency, measured in Hz (Hertz), is equivalent to cycles per second. Any time-varying signal (eletrical or sound pressure) can be measured this way for frequency.
- Sound pressure level, mesured in B (bels) or more commonly dB (decibels) is defined by reference to [a threshold level](https://en.wikipedia.org/wiki/Absolute_threshold_of_hearing) at the lower limit of human hearing. This may deserve its own post, but for now, know that audio loudness expressed in dB is shorthand for "dB SPL," which refers to that 20 micropascal pressure that corresponds to the quietest sound humans can perceive. Hearing has enormous dynamic range, and so the threshold of pain is somewhere around or above 120 dB SPL, depending on frequency. 
- dB units are dimensionless--anything measured in dB is actually a ratio between some measurement and the reference point which has the identical dimensions. Therefore the numerator and denominator dimensions cancel and dB are "dimensionless." So it can be tricky or confusing to know exactly what quantity is being expressed, although usually from context you can figure it out. We won't go crazy deep into audio engineering where the going gets rougher as yoou model gain staging througha complex signal chain, so most of the time on this blog dB will refer to dB SPL, or how load the sound is. I'll try to labe other usages clearly in the interests of <strike>being a giant nerd</strike> precision and clarity of expression.
- 83 dB SPL is a sort of *de facto* reference level for listening critically, such as during mixing or mastering. This is a recommendation from SMPTE, the Society of Motion Picture and Television Engineers. The tradeoffs are this is loud enough that the frequency response is flatter (than at quieter levels) but not so loud to be fatiguing.
- 1 dB (change, not an absolute level in SPL) is about the smallest perceptible change in level.
- 3 dB corresponds to twice the power in Watts (-3 dB to half). So if your system generates a level of 77 dB sPL with 1 Watt applied, applying 2 watts will geenrate an 80 dB SPL. 
- 6 dB corresponds to twice the pressure/level/loudness. It takes 4 times the power to achieve.
- 10 dB corresponds to a tenfold increase in power.
- 20 dB is a tenfold increase in loudness, and a 100-fold increase in power.

## Musical quantities to know

- An octave is the pitch distance between two muscial notes that share the same name (pitch class). In musical terms, 440Hz is defined as A4 by international standard [ISO 16:1975](https://www.iso.org/standard/3601.html). A5 is one octave above A4, and is 880Hz. A6 is twice the frequency of A5. A3 (220Hz) is half the frequency of A4.
- Harmonics are the music theory term for integer multiples of a fundamental frequency. Physical objects that vibrate tend to also vibrate at a series of multiples of their fundamental frequency.

> Updated on 2026-01-06
