# ArduinoComponentSketches
Collection of sketches for ATTiny to replace logic blocks in lunetta like circuits


Arduino Component Sketches
==============


## Objective:
Create a library of Arduino Sketches that can be loaded on ATTiny AVR microcontrollers to use in lo-fi synth/noise circuits.   Either replacing a block of logic or creating a new type of circuit block altogether.  The intent is not to create a synth on a chip, but to have a series of building blocks to create richer devices with an actual lower device count.  Rather than write the code to tailor the circuit, these are a prewritten library of sketches that can be used to plug into your breadboard or whatever.  Kinda like if you discovered a whole new series of CMOS chips like the 4000 series.

Of course, these are really arduino chips with the limitations that they have.  I am focusing on ATTiny85, 84 and 2313 for the most part.  Again, these are components, not full blown products.

The closest thing I have found is the Rad-fi System from Bleep Labs.

http://bleeplabs.com/store/the-rad-fi-system/

A collection of ATTiny micros with these sketches would be completely compatable with this system.


## Background:
Circuits like the NandSynth and Atari Punk Console are used to make all kinds of lo-fi noise and they sound horrible.  My cats hate them.  I even find them grating at times, but I am totally fascinated by learning how synths are made and always find great joy in building circuits with lots of bzzt, wacka and of course, blinky lights.  Oh those delightful lights.

Modular synths are generally pretty complicated pieces of work.  They have a few general formats and work in the analog realm.  Voltages generally are 1v/octave with +/- 15 rails ( I think) as well as gates, triggers and other signals. Assuming you know what your doing, modules are somewhat interchangeable and allow you to take basic sound building blocks and connect them together to make all sorts of musical goodness.

A much simpler format out there is what is referred to as a Lunetta.  These are far simpler in design, yet are still  capable of many things.  There are no real formats, rules nor form factors here.  Components are as likely to be in a nice walnut lined cabinet as a Power Rangers lunchbox or an 'I cant believe its not butter' tub.

A great starting point to explore here are
http://electro-music.com/forum/forum-160.html
http://cmoslove.blogspot.com/
http://milkcrate.com.au/_other/sea-moss/


The basic block of a lunetta is the cmos chip.  Signals are generally squarewave in the audible range.  CMOS chips are very easy to string together and experiment with.  Typical building blocks are squarewave generators, counters, mixers and the like.

Half the fun is digging through a CMOS book and reading about the components available and then dreaming up weird ways to squeeze sounds from them.


## Requirements:
Ability to program ATTiny chips.  This only requires an arduino uno and a breadboard.
Some links on how to do this are here.

## System:
An Index.  The biggest thing I would like is a good indexing system.  Everybody that plays with lunetta circuits knows exactly what to expect form a CD40106.  They have specs. Thats what Im going for.

Another good thing about that is that it helps keep the functionality of components from turning to mud.  An existing sketch can always be improved, but there is no need to do it if that functionality exists elsewhere.  For example, the CD40163 is an excellent Cmos counter.  It does not count up AND down however.  If thats functionality thats needed, use the CD40193 instead of adding that functionality to the CD40163.


Proposed numbering is as follows

ACS-[85,84,23]-xyyy

For example the first component in the series is

ACS-85-0001

Range   | Description  
--- | ---
000-199 | Oscillators, Vco, LFO
200-299 | Envelope generators, VCA
300-499 | Modulation.  Adders, Mixers, dividers, Multiplexers, Gates, Vibrato
500-699 | Shift, Delay, Melody Makers, Atari Punk Console
700-899 | Interface, Control, Midi, Visualization
900-999 | Other

The next digit is for Attiny clock.

0xxx is 8Mhz no xtal

1xxx is 1Mhz

2xxx is 16Mhz with xtal


if we run outta space...we can start over at 5.


So say we have
ACS-85-0104 as PsychoLfo
it would be nice to have
ACS-84-0104 as the ATTiny 84 port and
ACS-84-2104 as the 16Mhz Attiny 84 port




 

### ATTiny85



Number    | Title   | Status   | Description  
--- | --- | --- | ---
[ACS-85-0001](https://github.com/robstave/ArduinoComponentSketches/tree/master/ACS-85%20ATTiny85%20sketches/ACS-85-0001) | Simple VCO | Ready| Fixed VCO with High and Low Frequencies and a Ramp
 



### ATTiny84



Number    | Title   | Status   | Description  
--- | --- | --- | ---
[ACS-84-0001]((https://github.com/robstave/ArduinoComponentSketches/tree/master/ACS-84%20ATTiny85%20sketches/ACS-84-0001) | Simple VCO | Ready | Fixed VCO with High and Low Frequencies and a Ramp and Triangle


