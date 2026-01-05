---
layout: page
title: About my listening room
permalink: /room/
---

- My room is 275" W × 172" L × 104" H. 
- Floor is shag carpet over poured concrete (this is a basement room).
- Listening position is 26" from rear wall on a leather sectional sofa. 
- Distance from R speaker to wall is 80" and from L to wall is 100".
- Listening Position is 125" from right wall, 148" from left.
- measurement of the noise floor in the room was below 40 dB (measured with a phone app--my meter range does not extend that low)

# Diagram

A diagram from REW that models the listening position in the room:

![room diagram](/i/room-diagram.png)

# Mode analysis

Here are the top 30 modes derived from the room's geometry.

Why is this at all important? The parallel walls will tend to reinforce certain frequencies--it's a resonant system with frequency is related to the distance between the walls. By dividing the speed of sound by twice the distance, you will determine the wavelength that is reinforced. Integer multiples (harmonics) of that fundamental wavelength are also reinforced, check out this pic from my textbook to help you visualize this:

![room modes diagram](/i/modes.png)

So I got a little help from Copilot to calculate the meaningful modes to pay attention to in my room:

## Conventions
- Speed of sound assumed: **1130 ft/s** (typical room temperature approximation)
- Mode index format: **(nx, ny, nz) = (Length, Width, Height)**
- Mode types:
  - **Axial:** two indices are zero
  - **Tangential:** one index is zero
  - **Oblique:** no indices are zero

## Axial Modes (dominant) — up to 200 Hz
### Width (W)

|   n |   Frequency (Hz) |
|----:|-----------------:|
|   1 |            24.65 |
|   2 |            49.31 |
|   3 |            73.96 |
|   4 |            98.62 |
|   5 |           123.27 |
|   6 |           147.93 |
|   7 |           172.58 |
|   8 |           197.24 |


### Length (L)

|   n |   Frequency (Hz) |
|----:|-----------------:|
|   1 |            39.42 |
|   2 |            78.84 |
|   3 |           118.26 |
|   4 |           157.67 |
|   5 |           197.09 |


### Height (H)

|   n |   Frequency (Hz) |
|----:|-----------------:|
|   1 |            65.19 |
|   2 |           130.38 |
|   3 |           195.58 |


## Lowest 30 Modal Frequencies (Axial + Tangential + Oblique) — ≤ ~126 Hz
|   # | Type       | Mode (nx,ny,nz)   |   Frequency (Hz) |
|----:|:-----------|:------------------|-----------------:|
|   1 | Axial      | (0,1,0)           |            24.65 |
|   2 | Axial      | (1,0,0)           |            39.42 |
|   3 | Tangential | (1,1,0)           |            46.49 |
|   4 | Axial      | (0,2,0)           |            49.31 |
|   5 | Tangential | (1,2,0)           |            63.13 |
|   6 | Axial      | (0,0,1)           |            65.19 |
|   7 | Tangential | (0,1,1)           |            69.7  |
|   8 | Axial      | (0,3,0)           |            73.96 |
|   9 | Tangential | (1,0,1)           |            76.18 |
|  10 | Axial      | (2,0,0)           |            78.84 |
|  11 | Oblique    | (1,1,1)           |            80.07 |
|  12 | Tangential | (0,2,1)           |            81.74 |
|  13 | Tangential | (2,1,0)           |            82.6  |
|  14 | Tangential | (1,3,0)           |            83.81 |
|  15 | Oblique    | (1,2,1)           |            90.75 |
|  16 | Tangential | (2,2,0)           |            92.99 |
|  17 | Tangential | (0,3,1)           |            98.59 |
|  18 | Axial      | (0,4,0)           |            98.62 |
|  19 | Tangential | (2,0,1)           |           102.3  |
|  20 | Oblique    | (2,1,1)           |           105.23 |
|  21 | Oblique    | (1,3,1)           |           106.18 |
|  22 | Tangential | (1,4,0)           |           106.2  |
|  23 | Tangential | (2,3,0)           |           108.1  |
|  24 | Oblique    | (2,2,1)           |           113.56 |
|  25 | Tangential | (0,4,1)           |           118.22 |
|  26 | Axial      | (3,0,0)           |           118.26 |
|  27 | Tangential | (3,1,0)           |           120.8  |
|  28 | Axial      | (0,5,0)           |           123.27 |
|  29 | Oblique    | (1,4,1)           |           124.62 |
|  30 | Oblique    | (2,3,1)           |           126.24 |

---
*Generated from room geometry only; does not include soffit effects, damping, speaker placement, or boundary compliance.*

Each of the above is a potential (theoretical) problem with the evenness of my room's frequency response. If it turns out to be an actual (measured) problem, the steps I can take to attempt to correct it mainly involve moving the positions of the speakers and the listener, since the room geometry is not changing.

In recording studios, the designers avoid parallel walls to keep these effects from contributing negatively to the sound. Peaks and nulls of 30dB or more are not unusual, and most rooms suffer from at least a couple of these. 

> Updated on 2026-01-05

 