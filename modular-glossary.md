---
description: simpler definitions that everyone can understand
---

# Modular Glossary

### AC coupled

An AC coupled input attempts to remove any constant DC voltage going through it. This is useful if you want to remove any accidental DC offset that might have crept into it. These offsets can cause one half of the AC waveform to clip prematurely, or can cause clicks at the start and end of envelopes or mutes.

### Analog Shift Register

A shift register is a device that takes one thing, then copies it and puts it in a different place. A bucket brigade works like this: you have a line of people holding buckets, and they pass water along to the next person. The person at the end of the line dumps the water out. An analog shift register is like a bucket brigade, but with electricity instead of water. It copies what it gets, and puts it in a different place.

### Attenuator

An attenuator is a device that reduces (or “attenuates”) the level of a signal. A fader on a mixer is an attenuator. Attenuators are particularly useful for adjusting how much “depth” of modulation you send from one module to another module’s parameter – for example, whether an LFO makes the pitch of a VCO go up and down a lot (the result with no attenuation) or a little (the result of attenuating the LFO’s signal).

### Attenuverter

An attenuverter is a special type of attenuator that can also invert the polarity of the signal or voltage going through it. Most attenuverters use pass through no signal at their center position; as you turn them clockwise, you turn up the normal version of the signal; as you turn them counterclockwise, they turn up an inverted version of the signal. Some attenuverters are a normal attenuator with a polarity switch added on.

### Buffered Multiple \[Active Multiple]&#x20;

A multiple (also called a mult) is a common module used to split a signal into several outputs. A buffered multiple is an active multiple that has buffering to isolate the outputs from each other. The buffer circuit will prevent the signal from losing its strength or integrity by being split too many times, and will prevent any funny business happening on one of the outputs from affecting any of the other connections. Some modules do have good buffering built into their outputs, and can drive multiple modules without issue. But if you try to use a passive mult to connect to, say, three oscillators, and you realize the tracking isn’t very good (they quickly go out of tune as you go up and down).

### Burst Generator&#x20;

When you send this module a trigger, it outputs a stream or “burst” of triggers in response. You usually have control over the number of triggers, the spacing between them, and often the probability that individual trigger output will be sent or skipped (for random patterns). At its most tame, it can be use to create “double pluck” triggers in response to a normal note on; and its most extreme, it is used to trigger a high-energy, chaotic stream of drum hits that may or may not be in time with the music. "Burst Generator" is a module that generates bursts of triggers. It is often used to create a trigger pattern that feels pseudo-randomly generated.

### Comparator&#x20;

A comparator is a circuit which compares two voltages and outputs a voltage which is high when the first voltage is higher than the second voltage and low when the first voltage is lower than the second.&#x20;

### Composite waveform&#x20;

A composite waveform is a waveform which contains more than one waveform. The most common composite waveforms are square, sawtooth, and triangle. Composite waveforms are created by adding together two or more other waveforms. In this way they can be used to create new sounds or manipulate existing ones. Composite waveforms can be used to create new sounds or manipulate existing ones.

### DC Coupled&#x20;

When a module says its inputs are DC Coupled, that means it can accept DC voltages (constant or slowly changing voltages) and pass them through unaltered. This is important if, for example, you want to use a VCA to control the amplitude of an envelope going through it: You would need one that was DC coupled, as an AC coupled input would try to remove the DC component of the signal (such as its sustain level) and return it to 0v

### Euclidian Rhythms&#x20;

Euclidean rhythms are based on a neat math trick and cosmic coincidence promoted by Godfried Toussaint at McGill University in Canada. In short, you take a pattern length – such as 16 – and a number of beats – such as 6 – and spread those beats out across the pattern using an algorithm based on mathematician Euclid’s Elements (circa 300 B.C.). The results are rhythmic patterns that closely or exactly matched many world music styles – in particular, from Sub-Saharan Africa, and especially if you rotate them in time to change where the downbeat falls. For example, 6 into 16 (notated “6,16” or “3,8”) creates a pattern like this: 1001001010010010 The pattern above is the same as the Cuban Tresillo, considered “the most fundamental and most prevalent duple-pulse rhythmic cell in Sub-Saharan African music traditions.” Several modules exist that are based on Euclidean rhythms; since the algorithm is easy to compute, they also appear as an extra feature in other modules including Mutable Instruments’ Grids and Yarns, ALM’s Pamela’s New Workout, as well as the DIY Ornament & Crime.The most well known of the dedicated Euclidean rhythm modules is vpme.de’s EuclideanCircles. It creates either three or six independent sequences at once, with multi-functioncontrols to set the sequence length.

### Function Generator&#x20;

The term function generator is a generic name to refer to a generator of any type of signal. Envelope Generators can also be called function generators because they generate a function (an envelope) in response to an input event.

### Gate&#x20;

This is one of the main signal types that are passed around inside a modular synthesizer. It jumps to high level – typically 5 volts – when a new note is supposed to start (such as when you press a key on a keyboard controller), or when a sequencer jumps to the next “stage” or note. A gate typically stays at that level for the duration of the note (i.e. while the key is being held down), and suddenly drops or “goes low” to its resting level – typically 0 volts, but sometimes –5 volts or another number – when the note ends (i.e. when the key is released). In practice, when a gate signal is sent to a typical envelope generator, the start of the gate (when it “goes high”) tells the envelope to go through its Attack and Decay stages; while the gate remains high, the envelope stays at its Sustain level, and when the gate goes low again, the envelope moves onto its Release stage.&#x20;

### Glide&#x20;

Refers to a note that glides from one pitch to another while it is still audible. The music term for this effect is portamento, which is a slurring between notes. In a synthesizer, this effect is created by causing the control voltage for the pitch of a note to slide from the pitch of the previous note rather than make a discrete jump. The module that creates this effect is sometimes known as a slew generator, slew limiter, slope generator, or lag. Some use the terms glide, glissando, and portamento interchangeably, but if you want to split musical hairs, a glissando (gliss) is a different effect where the intermediate notes are more distinct – such as played rapidly in order – rather than slurred through.&#x20;

### Horizontal Pitch&#x20;

HP = Horizontal Pitch. In the Eurorack format for synthesizer modules, the width of a module is defined as the number of hp (horizontal pitch) units. Each hp is 0.2” (0.5 cm). Most modules are even numbers of hp wide, although some are odd numbers. Also, modules tend to be ever so slightly less than exactly some multiple of 0.2” wide, just to make sure you don’t run into problems with ever so slightly too wide modules overlapping.

