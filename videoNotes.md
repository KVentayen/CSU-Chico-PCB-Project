<!--

TOGGLE PREVIEW IN VISUAL STUDIO CODE:
    Ctrl + Shift + V

This space is designated for Markdown resources:
    - General Markdown Documentation: https://markdown-guide.readthedocs.io/en/latest/index.html

    - Markdown in Visual Studio Code Documentation: https://code.visualstudio.com/docs/languages/markdown

-->

[Comment]: <> (Inline Comment)
[//]: <> (This is also a comment)
[//]: # (This is also a comment)
<!--
    This is a multiline comment
-->

This document saves notes taken on the [kicad stm32 + usb + buck converter pcb design and jlcpcb assembly (update) - phil's lab #11](https://www.youtube.com/watch?v=c7-8nuu6e3e) by [phil's lab](https://www.youtube.com/@philslab) on [YouTube](https://www.youtube.com)

# Introduction
[Mark](https://www.youtube.com/watch?v=C7-8nUU6e3E)
# Topics Covered
[Mark](https://www.youtube.com/watch?v=C7-8nUU6e3E&t=14s)
# JLC PCB Assembly Showcase
[Mark](https://www.youtube.com/watch?v=C7-8nUU6e3E&t=31s)
# Parts used in design (JLCPCB parts library)
[Mark](https://www.youtube.com/watch?v=C7-8nUU6e3E&t=58s)
# STM32 pin assignment in STM32CubeMX
[Mark](https://www.youtube.com/watch?v=C7-8nUU6e3E&t=208s)
# KiCad project and schematic
[Mark](https://www.youtube.com/watch?v=C7-8nUU6e3E&t=583s)
# Schematic page settings
[Mark](https://www.youtube.com/watch?v=C7-8nUU6e3E&t=606s)
# Adding STM32F405 to schematic
[Mark](https://www.youtube.com/watch?v=C7-8nUU6e3E&t=653s)
# STM32 power pins
[Mark](https://www.youtube.com/watch?v=C7-8nUU6e3E&t=730s)
# Labeling pins/global labels
[Mark](https://www.youtube.com/watch?v=C7-8nUU6e3E&t=854s)
# VCAP pins
[Mark](https://www.youtube.com/watch?v=C7-8nUU6e3E&t=897s)
# NRST and BOOT0 pins, Bootmodes
[Mark](https://www.youtube.com/watch?v=C7-8nUU6e3E&t=997s)
# Transferring assignments from CubeMX to KiCad
[Mark](https://www.youtube.com/watch?v=C7-8nUU6e3E&t=1224s)
# 'NoConnect' flags
[Mark](https://www.youtube.com/watch?v=C7-8nUU6e3E&t=1438s)
# Decoupling capacitors
[Mark](https://www.youtube.com/watch?v=C7-8nUU6e3E&t=1488s)
# VDDA pin decoupling
[Mark](https://www.youtube.com/watch?v=C7-8nUU6e3E&t=1570s)
# Crystal circuitry (HSE)
[Mark](https://www.youtube.com/watch?v=C7-8nUU6e3E&t=1674s)
# LED and current limiting resistor
[Mark](https://www.youtube.com/watch?v=C7-8nUU6e3E&t=2235s)
# Buck converter and circuitry (+ fusing, reverse polarity protection)
[Mark](https://www.youtube.com/watch?v=C7-8nUU6e3E&t=2366s)
# Connectors (SWD, I2C, UART)
[Mark](https://www.youtube.com/watch?v=C7-8nUU6e3E&t=3375s)
# USB
[Mark](https://www.youtube.com/watch?v=C7-8nUU6e3E&t=3760s)
# Electrical rules checker (ERC)
[Mark](https://www.youtube.com/watch?v=C7-8nUU6e3E&t=4269s)
# Mounting Holes
[Mark](https://www.youtube.com/watch?v=C7-8nUU6e3E&t=4375s)
# Assigning footprints to symbols
[Mark](https://www.youtube.com/watch?v=C7-8nUU6e3E&t=4425s)
# Generating the netlist
[Mark](https://www.youtube.com/watch?v=C7-8nUU6e3E&t=5076s)
# Choosing the number of PCB layers
[Mark](https://www.youtube.com/watch?v=C7-8nUU6e3E&t=5095s)
# Design rules
[Mark](https://www.youtube.com/watch?v=C7-8nUU6e3E&t=5171s)
# Rough layout (section by section)
[Mark](https://www.youtube.com/watch?v=C7-8nUU6e3E&t=5246s)
# Improving the layout, finer details
[Mark](https://www.youtube.com/watch?v=C7-8nUU6e3E&t=5709s)
# Mounting hole placement
[Mark](https://www.youtube.com/watch?v=C7-8nUU6e3E&t=6797s)
# Board outline and rounded corners
[Mark](https://www.youtube.com/watch?v=C7-8nUU6e3E&t=6910s)
# Rearranging connectors
[Mark](https://www.youtube.com/watch?v=C7-8nUU6e3E&t=7060s)
# Adding track widths
[Mark](https://www.youtube.com/watch?v=C7-8nUU6e3E&t=7219s)
# Power and ground planes (copper pours)
[Mark](https://www.youtube.com/watch?v=C7-8nUU6e3E&t=7255s)
# STM32 and routing (critical items first)
[Mark](https://www.youtube.com/watch?v=C7-8nUU6e3E&t=7390s)
# Tombstoning
[Mark](https://www.youtube.com/watch?v=C7-8nUU6e3E&t=7481s)
# Track spacing
[Mark](https://www.youtube.com/watch?v=C7-8nUU6e3E&t=7555s)
# Buck converter routing
[Mark](https://www.youtube.com/watch?v=C7-8nUU6e3E&t=7729s)
# Track width calculator
[Mark](https://www.youtube.com/watch?v=C7-8nUU6e3E&t=7800s)
# USB controlled impedance differential traces
[Mark](https://www.youtube.com/watch?v=C7-8nUU6e3E&t=7959s)
# JLCPCB impedance calculator
[Mark](https://www.youtube.com/watch?v=C7-8nUU6e3E&t=7988s)
# Connecting GND and 3V3 (with vias to internal copper pours)
[Mark](https://www.youtube.com/watch?v=C7-8nUU6e3E&t=8169s)
# Design rules checke (DRC)
[Mark](https://www.youtube.com/watch?v=C7-8nUU6e3E&t=8880s)
# Silkscreen (labeling, pin 1 indication, polarity indication)
[Mark](https://www.youtube.com/watch?v=C7-8nUU6e3E&t=8930s)
# Importing custom graphics as silkscreen
[Mark](https://www.youtube.com/watch?v=C7-8nUU6e3E&t=9370s)
# Hiding JLCPCB order number
[Mark](https://www.youtube.com/watch?v=C7-8nUU6e3E&t=9415s)
# Adding tooling holes for assembly
[Mark](https://www.youtube.com/watch?v=C7-8nUU6e3E&t=9462s)
# Generating Gerber and drill files
[Mark](https://www.youtube.com/watch?v=C7-8nUU6e3E&t=9550s)
# Footprint position file
[Mark](https://www.youtube.com/watch?v=C7-8nUU6e3E&t=9527s)
# Bill of materials (BOM) and assigning part numbers (LCSC)
[Mark](https://www.youtube.com/watch?v=C7-8nUU6e3E&t=9694s)
# Ordering PCBs via JLCPCB with assembly
[Mark](https://www.youtube.com/watch?v=C7-8nUU6e3E&t=9872s)