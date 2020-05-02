# Mechanical Keyboard

## Backgorund and Overview
This is a simple exposed-PCB design for a Cherry MX-based mechanical keyboard. It is a full-size 104-key board, but also
includes 4 extra keys that can be used for anything. It uses PCB-mount Cherry MX switches, and can be assembled with any
color non-backlit switch (I don't care for keyboard backlighting, so I didn't include it). It runs on an STM32F070C6
microcontroller.

The PCB was designed in [KiCad](https://kicad-pcb.org), which conveniently already had Cherry MX key switches in its
component libraries. Except for the key switches and the USB port, all the components are surface mount. This can make
it a little trickier to hand solder for people with less soldering experience (especially the 108 SOD-323 diodes...),
but it's entirely possible.

I started the project in August 2019 because I needed a better keyboard for work, and I wanted to try out STM32 MCUs,
which I hadn't used before. I couldn't get the firmware woring initially, so set it aside for a few months and finally
finished it in February 2020. The first version of the firmware was written using the STM32Cube framework with
STM32 HAL, but I ended up not being satisfied with the generated code from that system, and the keyboard itself wasn't
working as well as I wanted. Eventually, in April 2020, I rewrote the entirity of the firmware using
[libopencm3](https://gitub.com/libopencm3/libopencm3), which is vastly cleaner and nicer to work with than ST's own
framework.

![](https://github.com/nelluq/mechanical_keyboard/raw/master/images/keyboard-assembled.jpg)
(Apologies for the dirty keycaps, I took them off an old keyboard and haven't gotten around to cleaning them.)

## Instructions
Coming soon