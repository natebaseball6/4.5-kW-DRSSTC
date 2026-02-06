# 4.5-kW-DRSSTC

# OBJECTIVE

Create a ~4.5kW DRSSTC with enough documentation to make reproducable. 

# REQUIREMENTS

1) Must function using 120VAC source
2) Must be MIDI-modulatable
3) Must have specific safety features

# DRIVER-PLANNING
I am very familiar with the old UD2.7c designed by Loneoceans. I'm sure there are already more updated drivers out there, but I wanted to try my hand at really just updating his design from the ground-up. The only major electrical change I plan to make is to incorporate SMD and THT components. Beyond that, I may incorporate a metal shield to try and limit interference. However, the real improvement to this circuit would really just be making use of an FPGA (or something similar), which is out of the scope of this project.

Currently in the process of ironing out the KiCAD Schematic, only needing to redesign the output stage, find a suitable adjustable inductor, and add probing points. After that, I'll move to the board designer and hopefully get it ordered sooner rather than later. (But will I design a custom circuit board for the interrupter? If I make a plexiglass enclosure, do I really need that?). If this project never comes to light, at least the driver will be out there. 

# INVERTER-PLANNING
Because of the energy level I intend to operate this project at, it's a no brainer that I need to incorporate a full bridge inverter. I'll likely end up using some "brick" IGBTs, though if modern, smaller IGBTs have caught up to those monsters I see no reason to not update.

# BUS-PLANNING
The bus is one of the more annoying parts of this project, largely because of the voltage doubler circuits that are required to make it work. WIP

# INTERRUPTER-PLANNING
I plan to design a simple interrupter using a microcontroller, maybe a spare arduino Uno I have lying around, or perhaps a ESP32 or RPi Pico. I haven't been too into that field lately, but it shouldn't be too hard. All I need is an emergency off button, a "start" button, a "play" button (for music), maybe a Pulse-Width Modulator, and whatever else. 

# PRIMARY-COIL-PLANNING
I've seen a lot of designs that incorporate a simple circular coil design, but (and I don't remember where from), I'm recalling a design of a toroidal Primary Coil design, and I'd like to incorporate that. The wires must be exrremely thick and able to withstand large bursts of energy. Insulation is absolutely necessary, and air cooling isn't out of the question.

# SECONDARY-COIL-PLANNING
I plan to design the secondary coil to function at around 40kHz, though the actual value doesn't matter too much yet. The main problem I forsee is finding a suitable topload.

# MMC-PLANNING
WIP

# ENCLOSURE-PLANNING
WIP
