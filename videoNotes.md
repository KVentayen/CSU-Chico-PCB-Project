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

# Introduction | SKIP
[Mark](https://www.youtube.com/watch?v=C7-8nUU6e3E)
- Refer to previous Tutorial
# Topics Covered | SKIP
[Mark](https://www.youtube.com/watch?v=C7-8nUU6e3E&t=14s)
- Video Overview
# JLC PCB Assembly Showcase | SKIP
[Mark](https://www.youtube.com/watch?v=C7-8nUU6e3E&t=31s)
- Showcase PCBs
# Parts used in design (JLCPCB parts library) | SKIP
[Mark](https://www.youtube.com/watch?v=C7-8nUU6e3E&t=58s)
- Show the JLC PCB parts library jlcpcb.com/parts
- Show design decisions for components
# STM32 pin assignment in STM32CubeMX | SKIP
[Mark](https://www.youtube.com/watch?v=C7-8nUU6e3E&t=208s)
- Configure Microcontroller using STM32 CubeMX
# KiCad project and schematic
[Mark](https://www.youtube.com/watch?v=C7-8nUU6e3E&t=583s)
- Start a new Project
- Start a Scematic
# Schematic page settings
[Mark](https://www.youtube.com/watch?v=C7-8nUU6e3E&t=606s)
- Select Edit Page Settings
- Main Parameters:
    - Page Size
    - Orientation
    - Issue Date
    - Revision
    - Title
    - Company
# Adding STM32F405 to schematic
[Mark](https://www.youtube.com/watch?v=C7-8nUU6e3E&t=653s)
- Locate the STM32 Microcontroller and place it in schematic
# STM32 power pins
[Mark](https://www.youtube.com/watch?v=C7-8nUU6e3E&t=730s)
- Place the Power Symbols
    - Ground
    - +3.3V
    - +3.3VA
- Hotkey: Hover + M = Move Symbol
- Hotkey: Hover + W = Add Wires
# Labeling pins/global labels
[Mark](https://www.youtube.com/watch?v=C7-8nUU6e3E&t=854s)
- Label Pins Using Global Labels
# VCAP pins
[Mark](https://www.youtube.com/watch?v=C7-8nUU6e3E&t=897s)
- Add Capacitor Symbols
- Hotkey: Hover + C = Copy Component
    - Different from Video: Hover + Ctrl + C
# NRST and BOOT0 pins, Bootmodes
[Mark](https://www.youtube.com/watch?v=C7-8nUU6e3E&t=997s)
- Discuss about NRST and BOOT0
    - Refer to the Datasheet
- Add Switch Component
# Transferring assignments from CubeMX to KiCad
[Mark](https://www.youtube.com/watch?v=C7-8nUU6e3E&t=1224s)
- Add more global labels
# 'NoConnect' flags
[Mark](https://www.youtube.com/watch?v=C7-8nUU6e3E&t=1438s)
- Add No Connects
    - Connect to Ground
    - Hotkey: Insert = Continuously Add No Connects
# Decoupling capacitors
[Mark](https://www.youtube.com/watch?v=C7-8nUU6e3E&t=1488s)
- Add Decoupling Capacitors to the Power Supplies
# VDDA pin decoupling
[Mark](https://www.youtube.com/watch?v=C7-8nUU6e3E&t=1570s)
- Basic Filtering with Inductor and Capacitors
    - Add Inductor
    - Add Capacitor
# Crystal circuitry (HSE)
[Mark](https://www.youtube.com/watch?v=C7-8nUU6e3E&t=1674s)
- Add a Ceramic Crystal Oscillator
    - Review Documentation for the Crystal Oscillator for suggested circuitry
    - Add Capacitors
    - Add Resistor
    - Connect HSE_IN
    - Connect HSE_OUT
- Add Text Comment
- Rearrange Schematic
- Use the ``Place Graphic Lines or Polygons`` tool to group different parts of the schematic
- Add Text to Label Group
# LED and current limiting resistor
[Mark](https://www.youtube.com/watch?v=C7-8nUU6e3E&t=2235s)
- Add Status LED Label
- Add LED
- Add Resistor
- Add Ground
# Buck converter and circuitry (+ fusing, reverse polarity protection)
[Mark](https://www.youtube.com/watch?v=C7-8nUU6e3E&t=2366s)
- Add power to the board
- Refer to Data Sheet for Buck Regulator
- This Symbol is a Custom Symbol
    - Add Custom Symbol
    - Add ``BUCK_IN`` Label
    - Add ``BUCK_EN`` Label
    - Add ``BUCK_BST`` Label
    - Add ``BUCK_SW`` Label
    - Add ``BUCK_FB`` Label
- Add Additional Circuitry
- Review Transistor Datasheet
    - Use Mosfet for Reverse Polarity Protection
    - Add ``BUCK_IN`` Label
- Add a Ferrite Bead
- Used a Voltage Divider to Step Down Voltage from ``Buck_IN``
    - Add Resistors
    - Add ``BUCK_IN`` Label
    - Add ``BUCK_EN`` Label
    - Add Ground
- Add Bootstrap Capacitor
    - Add Capacitor
    - Add ``BUCK_BST`` Label
    - Add ``BUCK_SW`` Label
- Add Buck Switch Circuitry
    - Add Schottky Diode
    - Add Ground
    - Add Inductor
    - Add Capacitors
    - Add ``BUCK_SW`` label
- Use Resistors in series to produce the Feedback Circuitry
    - Add ``BUCK_FB`` label
    - Add Resistors
- Add Lines to Group Circuit
- Add Label to Group Circuit
# Connectors (SWD, I2C, UART)
[Mark](https://www.youtube.com/watch?v=C7-8nUU6e3E&t=3375s)
- Add Screw Terminal Symbol
    - Add +12V Power Supply
    - Add Ground
- Add Serial Bus Connector (02x05)
    - Add +3.3V Power Supply
    - Add Ground
    - Add a No Connect
    - Add Resistor
    - Add Global Labels
- Add Pull Up Resistors to ``I2C1_SCL`` and ``I2C1_SDA``
    - Add Resistors
    - Add +3V3 Power Supply
- Add Connector (02x04)
    - Add +3V3 Power Supply
    - Add Ground
    - Add ``I2C1_SCL`` Label
    - Add ``I2C1_SDA`` Label
- Add Connector (02x04)
    - Add +3V3 Power Supply
    - Add Ground
    - Add ``USART3_TX`` Label
    - Add ``USART3_RX`` Label
# USB
[Mark](https://www.youtube.com/watch?v=C7-8nUU6e3E&t=3760s)
- Add USB Connector (USB B)
    - Add Ground
    - Add No Connect
- Add ESD Protection
- Add Schottkey Diode to the Power Circuitry
    - Add +5V Power Supply
- Add ``USB_CONN_D+``
- Add ``USB_CONN_D-``
- Assign Labels and Nmbering for Components
    - Done Automatically in Newer Version
- Add Power Indicator LED
    - Add Red LED
    - Add Resistor
    - Add +3V3 Power Supply
    - Add Ground
- Add Label
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