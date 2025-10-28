---
content_type: page
description: ''
learning_resource_types: []
ocw_type: CourseSection
parent_title: Assignments and Projects
parent_type: CourseSection
parent_uid: 6e81c0bd-4e52-5a46-1f05-35f350963ca7
title: Design Report 3 sample
uid: 6989e57d-2a83-ca14-8d25-9e22f19e5141
---

Cat sounds source, PD generated
-------------------------------

_Courtesy of MIT student, used with permission._

This assignment was generated completely in PD. I based the patch on one I used to play sounds at an event in early April. That piece was a series of cat purrs and I used the same source material for this piece (purrs, meows, and field sound). Most of the material sampled I found online in free sound databases (notably freesound.org) but I also spent a significant amount of time capturing sounds from my own cat, Eegloo. None of those sounds are used except for the "bird" sound that contains some birds outside my window that start talking at about 4:00 a.m.

The piece mainly uses array-controlled multiple granular synthesizers to cut up material. Both the phasor and pitch shift aspects are controlled by arrays. Each one moves at a different speed to create some interesting aspects when the values are at a maximum together, for example. A base of purrs is used to give some bottom to the sound where the granular synthesis is the top. The purrs have a low-pass filter on them to isolate them. The piece sounds the best on headphones or on a floor populated with transducers. Two different purrs begin (one in each channel) and then a faster, more frantic purr provides a setting for the other sounds. The granulated sounds are allowed to mingle for the main section of the piece before being removed and only the bird sound and a purr is left. The bird sound is then slowed to almost its recorded speed and pitch before exiting and allowing the purrs to finish the piece. The PD file does contain some objects to allow me to "punch" in meow sounds via MIDI input but I decided not to use them.

I am pleased with the sounds in the piece, though they do move slowly. More sculpting of the granular synthesis parameters could always strengthen their use, including developing more precise graphs in athenaCL to use in PD. I also think using a variable metro rate would be interesting too (using the reading of one graph to control the reading speed of another graph). Maybe another granular synthesizer would add more texture and could be used in the middle of the piece to have something super dense that is just a knot of sound and then it untangles back to discernible noises.

{{< resource 711f9dfc-e6f7-2980-aad4-7e8b227e85c1 >}}

Design Report 3 sample: Cat sounds source, PD generated

Code file ({{% resource_link 2d1cc967-b575-4900-07c4-c08a85e8e973 "PD" %}})