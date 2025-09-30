---
content_type: page
description: ''
learning_resource_types: []
ocw_type: CourseSection
parent_title: Assignments and Projects
parent_type: CourseSection
parent_uid: 6e81c0bd-4e52-5a46-1f05-35f350963ca7
title: 'Project Sample: Video Soundtrack Generation with PD '
uid: fd7d0052-b2bd-a822-1685-719b3f1f304b
---

_Courtesy of MIT student, used with permission._

My sonic system was an attempt at soundtrack generation to a given piece of film. For my video test material, I used an old 1950s PSA about surviving a nuclear attack. The footage is part of the [Prelinger Archive](http://www.archive.org/details/prelinger). It is in black and white deliberately to limit the amount of visual information I have to deal with and to make the project simpler.

I used PD as my platform for producing sound. I also used tools from GEM to both play the footage and to draw color values from frames of the video. To start, I used a 3x3 grid of pixel "sensors" to pick up color information from the frames of the video. While the GEM object "pix\_data" can also produce RGB values, I only needed the greyscale values. This gave me 9 streams of values ranging between 0-1 where 1 = white and 0 = black to use in sound generation.

The most difficult part of the process was the mappings from data to sound. I recognized that frames that were lighter in contrast had higher tension in the narrative of the film so I decided to make them softer than the other frames. I used each vertical section of data sensors to control three polyphonic granular synthesizers to generate the low base of the sound. They are fed various sound files: two explosions and one sample of bass. Then each data sensor controlled an oscillator and a noise generator. I tried to manipulate the data more by generating more information: how the current data value compares to a local average, how it compares to a local minimum and maximum, how it compares to values of closely adjacent frames. These other data streams controlled values such as the pitch of the oscillator (within a specified band), band pass values for the pink noise generator, volume of the noise, and LFO on the oscillator.

Additionally I tried to build in some "recognition" into the system. I noticed that the bombs in the film were always in the center of the frame and almost white when exploding. I calibrated a counter to trigger the sound of an explosion when a bomb was shown on the screen but not at another time.

The project is a medium success. The sound produced is mostly without large-scale contour or interest. Admittedly, most of the time was spent on making sound on a micro-scale— the amount of LFO, the frequency range, the band pass values—and not as much on overall contours (except for basic considerations such as overall contrast values controlling the master volume). There could have been more effort but into trigger-based sounds instead of continuous sounds whose control values were constantly being changed. This would introduce both more space and interest into the sound. Also using more pre-composed segments that could be triggered would be useful. There may have also been too many "sound units" going on—when listening to one voice, the oscillations and sound over time are sort of interesting but this type of concentration is lost when hearing all 9 voices together with the granular synthesizers.

I also think the project would have sounded better if the three channels were separated out in space, in an installation set-up instead through headphones or speakers. This would help to "spatialize" all of the sounds being made and allow the listener to focus more closely on individual movements in each of the channels. I hope to keep working with this patch in order to produce something that sounds much better and improve my skills in PD.

{{< resource bc773f76-bba2-d448-4f82-d84577f05252 >}}

Project Sample: Video soundtrack generation with PD 1.

{{< resource 01a3377f-ad6b-df6e-1f1c-31f8ae375c0d >}}

Project Sample: Video soundtrack generation with PD 2.

{{< resource da5cfb5f-56a4-8fdb-b6c9-2644262c6215 >}}

Project Sample: Video soundtrack generation with PD 3.

Source video: 1951 US Civil Defense film [Survival Under Atomic Attack](http://www.archive.org/details/Survival1951)

Code and input audio samples ({{% resource_link 31d5efed-e8c7-d8e5-b636-628cc9d61bc1 "ZIP" %}}) (This ZIP file contains 1 .pd and 3 .wav files)