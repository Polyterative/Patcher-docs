---
description: >-
  simpler definitions that everyone can understand. This has been assembled from
  various sources online. Some edited via group effort. This is WIP
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

### Impedance&#x20;

Impedance is the measure of how something resists to the flow of energy. The higher the impedance, the harder it is for something to flow. There are two kinds of impedance: input impedance and output impedance. Input impedance measures how much a module resists to have energy flowing into it from source. Output impedance measures how easy it is for the module to deliver energy to a destination (like a speaker, or another module). Output impedance is usually much higher than input impedance.

**Inverter** An inverter multiplies an incoming control voltage by –1. In the case of a gate or logic inverter, it reverses the high and low states so that (for example) 0v becomes 5v and 5v becomes 0v. This is sometimes referred to as a polarizer, as it changes the polarity (+ versus –) of a signal. A control voltage inverter is often combined with an offset voltage to adjust the output voltage into the desired range. For example, if you had an envelope generator that had an output range of 0 to +8 volts, and you just inverted it, the result would be 0 to –8 volts. Since some modules such as voltage controlled amplifiers usually expect only positive voltages, you would then need to add 8 volts to that result to get an upside-down (inverted) envelope that still had an overall range of 0 to +8v.

**Inverting Mixer**&#x20;

Most signal mixers make an effort to keep the same polarity of a signal as it passes through the mixer. However, some mixers may invert the polarity or “phase” of a signal (as it’s a simpler design); other mixers may allow you to invert a signal on purpose so that you can experiment with tricks like adding one waveform or filter mode output out of phase with another coming from the same oscillator or filter.

**Karplus Strong**&#x20;

This is a physical modeling synthesis algorithm designed to replicate the sound of plucked, vibrating strings – although it has also proven useful for some percussion sounds as well. A short sample – originally noise, although it can be a high frequency chirp or other sound – is sent to both the output, and to a delay line. The output of a delay line is connected to a filter – originally a one-pole low pass filter; changing the filter has a huge effect on the character of the sound – and then back to both the main output and the input of the delay line. A few modules implement Karplus Strong synthesis, although it is an interesting challenge to patch yourself and play with the results.

**Line Level**&#x20;

Most consumer and lower-cost professional audio equipment use a signal level reference known as line level or –10dBV (decibel volts). The most common connectors are RCA (phono) or 3.5mm, although 1/4” is also used; the signal is “unbalanced” (it uses two wires: signal and ground). In the line level standard, a sine wave that varies between +/– 0.447 volts is considered to be at –10dBV. By contrast, a typical oscillator signal in a modular synthesizer is +/–5 to +/–8 volts. As a result, you will need either an output module in your modular synth or one heckuva input attenuator on your mixer or recorder to plug your synth into equipment that runs at line level. Similarly, you will need to substantially boost a line level signal to get it up to modular standards to process in your modular synth.

**Linear VCA**&#x20;

A linear voltage-controlled amplifier (VCA) uses a simple mathematical relationship between control voltage input and signal level output – for example, 50% of nominal control voltage in would result in the output signal being at 50% of the level of the input signal. This, however, is not how our ears perceive loudness; a sound must be amplified by 10x in order to be perceived as twice as loud. This makes a linear VCA desirable for scaling control voltages, but perhaps less so for scaling audio signals. If you connect an envelope generator with an exponential output to a linear VCA, then you will get the desired aural result. Confusing? That’s why it’s great when an envelope generator or VCA has a switch or control to vary it between linear and exponential response. A linear mixer is similar to a linear VCA: “half” on the input level control equals the output having half the voltage swing as the input. Again, this is fine for altering control voltages, but not for mixing audio signals; in that case you want a mixer with exponential controls.

**Logic**&#x20;

Binary or Boolean logic is a way of combining gate signals (on or off voltages) to create new outputs. Each section of a logic module typically includes 1 to 3 inputs, with 2 being the most common. Here are some of the most common logic functions: An OR function says if there is a gate on (or “high”) signal at any of the inputs (i.e. input 1 or input 2 or input 3, etc.), to output a gate on signal.

An AND function says only output a gate on signal if all of the inputs see “high” gate signals (i.e. input 1 and input 2 etc. all have gate ons). Adding an “N” to the front of a function’s name says “not” this function – in other words, a NOR function would only output a high signal if all inputs were low (not input 1 nor input 2 are high). Other common logic functions are inverters (often symbolized with a bar over the top of a letter corresponding to the input), and flip-flops that toggle between high and low every time they receive an input trigger (i.e. the first trigger would set the output high, the second trigger sets it low again, and so on). (Logic is also the name of a popular and long-lived MIDI sequencing program and DAW. But this site is about modular synths, and there are logic modules available.)

**Logic Functions**&#x20;

In a modular synth, control voltages tend to be continuous in nature, while gate and trigger signals are binary: on or off; high or low. This is the same as logic signals in digital circuitry. Therefore, some make digital logic modules. A common logic function is OR: If either signal A or signal B is high (on), then output a high gate signal (on); otherwise output a low gate (off). Another is AND: If and only if signal A and signal B are both, then output a high gate (on); otherwise, output a low gate (off). These are great functions for combining beat triggers from different timing sources.

**Low Pass Gate**&#x20;

By strict definition, a low pass gate (LPG) is a low pass filter whose cutoff frequency goes down into the subsonic range as its control voltage goes towards 0 volts, resulting in the input signal being filtered almost into silence. Some replicate this by combining a low pass filter and a voltage controlled amplifier into the same module, with both following the same control voltage. In either case, as an input envelope falls from a high level to 0 volts, the output gets duller (higher harmonics are filtered more) as it falls to silence. This mimics the way many natural sounds work. Click through for more details and examples, including a discussion of vactrols which are often used in low pass gates.

**Normalled**&#x20;

The power of modular synthesizers is that you can patch a signal to flow the way you prefer through your system. This can also be a time-consuming bummer when you’re just trying to patch a “typical” signal flow. Therefore, some manufacturers have created “semi- modular” synths that have all of these typical connections pre-wired for you, with the important feature that many of these wirings can be overridden by inserting patch cables into the correct jacks. These pre-wired connections are often referred to as being normalled. For example: An internal noise source may normally be connected to one channel of a mixer that appears before the filter, but if you insert a patch cable into a jack usually labeled external input, this “normalled” connection is broken and replaced by your external connection.

**OR function**&#x20;

One of the most common Boolean or binary logic functions, OR says if there is a gate on (or “high”) signal at any of the inputs (i.e. input 1 or input 2 or input 3, etc.), to output a gate on signal. A NOR function has an inverted output: it would only be on (high) if all inputs were low (not input 1 nor input 2 are high). An XOR (Exclusive OR) would only output a high signal if one of the inputs was high, but not if both inputs were high (or low). Finally, an XNOR is the invert of an XOR function.

#### PLL

A phase locked loop is, in essence, an oscillator that tries to match the frequency of – or more importantly, a division or multiple of the frequency of – another signal. This is most commonly used to create a frequency that is much higher than the incoming reference signal – such as a timing module that can create an output clock that is 2, 4, 8, or more times the tempo of an incoming clock, or a very high frequency oscillator that is locked to a multiple of an incoming pitch – perhaps to drive a special circuit such as a switched- capacitor filter. The problem and opportunity is that it’s very hard for a PLL to exactly, tightly follow change in the incoming reference pitch. A circuit (the phase comparator) needs to detect a difference between the input and the PLL’s oscillator and send a change in voltage to that oscillator; this voltage is usually smoothed by a slew or filter circuit to get rid of noise and other small wiggles in the difference. Therefore, a PLL tends to lag behind changes in the input signal. A couple of examples of modules that expose the inner workings of a PLL to the user are the Doepfer A-196 and WMD Synchrodyne – see the links below. A clocking module like the 4ms Quad Clock Distributor is a good example of an internal PLL applied to timing signals.

**Ping**&#x20;

In modular synthesis, a "ping" input is a place where you can patch a trigger or gate of any duration, and it converts it into a simple envelope. In particular, some filters and low pass gates (LPGs) have Ping inputs that create an instant attack and fairly quick decay to form a percussive-style envelope, internally patched the the filter's cutoff frequency. If the filter is oscillating due to high resonance, this creates simple analog percussion sounds such as classic drum machine kicks.

**Pingable**&#x20;

In modular synthesis, a "ping" input is a place where you can patch a trigger or gate of any duration, and it converts it into a simple envelope. In particular, some filters and low pass gates (LPGs) have Ping inputs that create an instant attack and fairly quick decay to form a percussive-style envelope, internally patched the the filter's cutoff frequency. If the filter is oscillating due to high resonance, this creates simple analog percussion sounds such as classic drum machine kicks.

**Polarizer**&#x20;

An inverter multiplies an incoming control voltage by –1. In the case of a gate or logic inverter, it reverses the high and low states so that (for example) 0v becomes 5v and 5v becomes 0v. This is sometimes referred to as a polarizer, as it changes the polarity (+ versus –) of a signal. A control voltage inverter is often combined with an offset voltage to adjust the output voltage into the desired range. For example, if you had an envelope generator that had an output range of 0 to +8 volts, and you just inverted it, the result would be 0 to –8 volts. Since some modules such as voltage controlled amplifiers usually expect only positive voltages, you would then need to add 8 volts to that result to get an upside-down (inverted) envelope that still had an overall range of 0 to +8v.

**Portamento**&#x20;

This refers to a note that glides from one pitch to another while it is still audible – in other words, a slurring or sliding between notes. In a synthesizer, this effect is created by causing the control voltage for the pitch of a note to slide from the pitch of the previous note rather than make a discrete jump. The module that creates this effect is sometimes known as a slew generator, slew limiter, slope generator, or lag. Some use the terms glide, glissando, and portamento interchangeably, but if you want to split musical hairs, a glissando (gliss) is a different effect where the intermediate notes are more distinct (including being played individually) rather than slurred through.

**Precision Adder**&#x20;

Synthesizers are very sensitive to unintentional variations in pitch control voltage – any error can result in the oscillators under control going out of tune. Therefore, whenever you add together pitch control voltages inside a modular synth, you really should be using a precision adder that precisely adds together the pitch voltages without introducing an error. Ordinary mixers might slightly attenuate or amplify a voltage passed through them, which in most cases would create tuning errors.

**Quantizer**&#x20;

Modular synths tend to follow a scheme were a specific change in voltage – such as 1. volts – results in a precisely one octave change in pitch. In a 1 volt per octave scheme, 1/12 of a volt change results in a semitone change in pitch. It can be difficult to precisely set a knob (say, on a sequencer) to hit the exact voltage required to get the desired pitch. A quantizer auto-corrects the input voltage to the nearest desired target, such as the voltage that corresponds to a semitone or other note in a scale. These are occasionally built into modules like sequencers or oscillators, but quite often they are standalone modules. You don’t have to use a quantizer just for pitch voltages; it can also be interesting to use one to convert a smoothly varying input voltage into a “stepped” voltage on output to create machine-like modulations and the such.

**Ramp**&#x20;

In general, a ramp refers to any voltage that is steadily raising or falling; quite often it resets when it reaches a target voltage and starts over again. A sawtooth oscillator waveform is sometime referred to as a ramp. Sometimes, the individual stages of an envelope generator are also referred to a ramp as it raises from 0 volts to a maximum level such as 5v for the attack stage, then falls from this peak to the sustain level for the decay stage.

**Ratcheting**&#x20;

This is a trick used with sequencers where one stage of the sequence may be triggered quickly multiple times, rather than just once as you step to that stage. For example, the result may be a series of quarter notes, with a burst of four sixteenth notes appearing instead for one or more stages. There are a few ways to patch a ratcheting sequence. In most cases, the step or stage number of the sequence is driven by a steady tempo; the trick is sending the burst of faster clocks to the gate input on the envelope generators. You can then send different clock divisions (such as quarter notes and sixteenth notes) to a sequential switch with the ability to step between those different inputs; then send the output of the switch to the envelope gate inputs. Another is to use a clock multiplier or divider that allows you to set

the multiplication or division with an external control voltage, such as another row from the sequencer.

**Sample & Hold**&#x20;

A sample and hold (S/H) module has two inputs: a signal that is being sampled, and a trigger input that indicates when the first input should be sampled. When a trigger is received, the current voltage at the first input is sampled (measured) and held (stored), and presented at the output. This stable voltage is held until a new trigger is received. Sample and holds are most often associated with creating stepped random voltages. To do this, noise is fed to the main input; whenever a trigger is received, the voltage present at that input is some random value, which is then dutifully sent to the output.

**Sequential Switch**&#x20;

This module comes in a few different forms; in the most common, a few different inputs are routed to one output (although they are usually symmetrical – one input can be switched between several outputs). A pulse or gate input then steps through the inputs one at a time, switching which ones is routed to the output. Fancier sequential switches allow you to set the number of stages, to divide an input clock so it switches at a slower tempo than the master clock, or might directly route a series of inputs to corresponding outputs (with usually a summed output as well).

**Shift Register**&#x20;

A Shift Register is a cross between a Sample & Hold module and a Bucket Brigade Delay. When initially triggered, it samples the incoming voltage, and presents that at its first output. On the second trigger, the incoming voltage is sampled again with this new voltage presented at the first output, while the original voltage is now moved to a second output. These voltage typically are sent to different oscillators, which will then play intervals and chords based on what notes you feed in one at a time. The output is akin to an echo with two or three repeats, but rather than being spaced at equal intervals of time, the "echoes" are triggered at the timing of your choosing, creating what has been called an arabesque pattern.

**Slew Limiter**&#x20;

This function smoothes out an incoming signal so that the change in voltage level cannot exceed a certain number of volts per second. As a result, it is sometimes called a lag generator or processor, or more technically as an integrator. One common use of a slew limiter is to introduce portamento (a glide between notes) when you feed a pitch control voltage through it. For this application, you’re fine with having one control for both positive and negative slew (a rising or falling voltage). Another common use is to smooth out the sudden on/off voltage of a gate signal into a more gradual envelope signal. In this application, you would a prefer a slew limiter with separate rising and falling rates – for example, to convert a gate signal into an envelope with fast attack (rising voltage) and slower decay (falling voltage). You can also use a slew limiter for other functions, such as knocking the sharp edges of a triangle LFO wave to create something slightly more like a sine waveshape. It can also smooth out random or noisy signals.

**Slope Generator**&#x20;

A slope generator creates ramps: rising or falling voltages. It is essentially a gate generator and a slew limiter (see above) wired together in the same module. A common example of a slope generator is an attack/decay (AD) or attack/release (AR) envelope generator. However, since it can be used for generalized control voltage functions – even creating a sawtooth or triangle wave oscillator – some companies such as Buchla and Serge referred to by its elemental function of generating sloping voltage changes.

**Strike**&#x20;

This term appears on several Make Noise modules, although it has been creeping into the general lingo. Some filters, amplifiers, and low pass gates (LPGs) that use or simulate vactrols (a light sensitive resistor placed next to a light source such as an LED, allowing a voltage to be turned into a resistance to control a parameter) may have a strike input. When you flash an LED at a light sensitive resistor, it does not change the resistance instantaneously and stay there – instead, there is some delay as it glides to the desired resistance. When you turn the LED off, the resistance may not go instantaneously to full; instead it might take a brief moment to decay. These characteristics are useful for creating percussive sounds and attacks. The purpose of a strike input is either to pass just a short pulse, or to allow you to re-attack while the LED is otherwise still on.

**Sync**&#x20;

Sync can have two different meanings, depending on whether we’re talking about oscillators or about clock signals. Some oscillators support a mode where they reset their waveshapes to the beginning when they receive a signal (usually a pulse or the rising edge of a square wave). The oscillator being synchronized is sometimes referred to as the “slave” oscillator. That sync signal comes from a second oscillator (sometimes called the “synchronizing” oscillator), usually tuned to a lower frequency than the one being synchronized. If there is not a precise octave relationship between the two oscillators, the result is a modified waveform that has been reset prematurely, following the frequency of the second oscillator. You can create some very cool “ripping” sounds by modulating the frequency of the slave oscillator; a simple AD envelope works well. There are two types of sync: hard and soft. Hard is where the slave oscillator always resets when the master tells it to, no matter what. Soft is where the slave oscillator only resets when it is close to the end of its own wave, meaning it ignores the sync signal unless the two oscillators are tuned close to some octave interval. In the context of timing, when you are synchronizing sequencers or drum patterns, it is common to send a master timing or sync signal around the modular for all the relevant modules to follow. This is typically a gate or trigger signal (beware of triggers that are too short in duration; some modules might miss the sync pulse – fortunately gate extenders exist). It can be a pulse that goes to a high voltage every note (such as a quarter or eighth note) of the overall pattern; it can be a clock going at a higher speed such as the common 24 ppqn (pulses per quarter note) used by MIDI and Roland DIN Sync compatible gear. This clock is tied to the desired tempo, and varies with the tempo (as opposed to video rate or sample rate synchronization, which tends to be a steady speed).

**Tru-Zero Frequency Modulation**&#x20;

Think of a patch where you feed the output of one oscillator (the modulator) into the frequency control voltage input of a second oscillator (the carrier). As the waveform output of the modulator rises above zero volts, it is added to the normal pitch control voltage for the carrier, and the pitch of the carrier goes up. As the waveform output of the modulator goes below zero, it is subtracted from the normal pitch control voltage, and the pitch goes down. But what happens if the result of subtracting the modulator from the pitch control goes below zero volts? In many oscillators, the carrier would slow down to a standstill, and wait there until the combined input voltage went above zero again. But in an oscillator that explicitly says it implements through-zero frequency modulation, the carrier will start playing backwards – in essence, a negative frequency. (The same applies to modulating the frequency of an LFO.) This generally produces a more pleasing result, and is a desirable characteristic for an oscillator. It’s relatively easy for a digital oscillator to implement through-zero FM; it’s trickier for an analog oscillator – but it’s becoming more common.

**Track & Hold**&#x20;

This is a variation of a Sample & Hold. Both have two inputs – a gate signal, and a voltage reference signal – and a voltage output. When a Sample & Hold receives a gate high signal, it freezes and outputs the voltage reference coming into the reference input. This voltage is maintained until a new gate high signal; gate low signals are ignored. With a Track & Hold, when the gate is high, the reference input it passed along to the voltage output (this is the “tracking” phase); when the gate goes low, the input voltage at that instant is frozen and maintained at the voltage output until a new gate high signal is received.

**Tracking**&#x20;

Tracking usually refers to how well an oscillator follows the pitch control voltage (CV) sent to it. As the voltage rises, the oscillator “tracks” it and produces a higher pitch. Most (but not all!) synths follow a 1 volt per octave system where a rise of 1.00 volts on the pitch input should produce exactly a doubling (one octave rise) in the oscillator’s pitch. If this is indeed what happens, the oscillator has good tracking. If the oscillator goes slightly out of tune, it is considered a tracking error, or to have poor tracking. Sometimes you will find voltage-controlled filters have a “tracking” switch for a CV input where the pitch of the filter’s corner frequency only rises at 1/3, 1/2, or 2/3 of the corresponding change of the pitch input. This can prevent high notes from sounding too bright without the bass notes sounding too dull. Sometimes you will find voltage-controlled filters have a “tracking” switch for a CV input where the pitch of the filter’s corner frequency only rises at 1/3, 1/2, or 2/3 of the corresponding change of the pitch input.

**Trigger**&#x20;

A trigger is a very short electrical pulse signal, rising from 0 volts to a standard level such as 5 or 10 volts for a few milliseconds before falling back to 0 volts. It is often used to start or “trigger” the playback of a percussion sound, including starting an envelope generator. They can also be used to pass clock signals around a synth so connected modules all know when a note (or finer subdivision of a note) starts. A trigger usually has a fixed duration, compared to a gate signal which also rises from 0 volts to a higher voltage and falls back to zero again, but which stays “high” a variable length of time depending on the length of a note.

**Unipolar** Many voltages in a modular synth – including the output of an audio oscillator, and most low frequency oscillators – fluctuates between positive and negative voltages. This is known as a bipolar voltage. Some voltages – such as the output of an envelope generator only vary between 0 volts and some maximum positive voltage; this is referred to as unipolar. This is handy for “opening” a voltage-controlled amplifier or filter. This variation between modules and functions drives some users crazy, especially when you want to use a voltage to control something other than what the module’s creator might have envisioned. That’s why it’s useful to have a utility module or two that can scale (attenuate or optionally amplify) and offset a voltage: among other tasks, it can convert a bipolar voltage to unipolar and vice versa.

**Vactrol** A vactrol is a light depending resistor (LDR) placed next to a light source (previously an incandescent bulb; nowadays an LED). As the light gets brighter, the resistance goes lower. This is a great way to add voltage control to what would otherwise be a resister in a circuit. What makes people excited about vactrols is that the relationship between the light and resistance is nowhere near linear or instantaneous: It takes some time to slew up or down to the desired resistance. These ringing and settling characteristics are useful for creating percussive sounds and attacks.
