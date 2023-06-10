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
- Select icon of a bug to enable Electrical Rules Checker
    - Icon has changed from the bug to a list (Still in the same general area)
- Warnings and Labels
# Mounting Holes
[Mark](https://www.youtube.com/watch?v=C7-8nUU6e3E&t=4375s)
- Add Mounting Holes
# Assigning footprints to symbols
[Mark](https://www.youtube.com/watch?v=C7-8nUU6e3E&t=4425s)
- Assign PCB Footprints
    - Find parts in JLC PCB's Library
    - Micro USB in Video is Custom
    - MP2359DJ-LF-Z1 is a custom component, but the package type is included in the KiCad Library
# Generating the netlist
[Mark](https://www.youtube.com/watch?v=C7-8nUU6e3E&t=5076s)
- Select Generate NetList Icon
    - Now this is done automatically
    - Manually generate netlist by Pressing F8 on the keyboard
        - https://www.reddit.com/r/KiCad/comments/sg0qqu/where_is_the_netlist_button/
# Choosing the number of PCB layers
[Mark](https://www.youtube.com/watch?v=C7-8nUU6e3E&t=5095s)
- How many layers are going to be available to use?
    - (Generally) The more layers that you have the easier it is to route
    - Determined by the PCB Company
        - JLC PCB (at the time of the video) offers PCBs with 1, 2, 4, and 6 Layers
        - Change in cost is not significant
    - Can use to have a dedicated Power Plane, Ground Plane, and Signal Planes
# Design rules
[Mark](https://www.youtube.com/watch?v=C7-8nUU6e3E&t=5171s)
- Select Board Setup
    - Change the number of Layers in the Pop-Up Window
    - Design Rules are determined by the manufacturer
        - Assumes JLC PCB Well
        - Exact Specifications can be found on the manufacturer's website
# Rough layout (section by section)
[Mark](https://www.youtube.com/watch?v=C7-8nUU6e3E&t=5246s)
- Select Load Netlist (In Video)
    - Choose Netlist File
    - Update PCB
- Select Update PCB with Changes... (In New Version)
    - Update PCB
- Make a rough layout
- Change Grid size from default to ``1.000 mm``
- Hotkey: Hover + M = Move
- Hotkey: Hover + R = Rotate
- Components selected in the schematic are also selected in the PCB Layout
    - Similarly, Components selected in the PCB Layout are Selected in the schematic
- Compnents in close distance in the schematic would be good to have close in the PCB Layout
- Determines the board size
# Improving the layout, finer details
[Mark](https://www.youtube.com/watch?v=C7-8nUU6e3E&t=5709s)
- In tutorial Designators are moved to the ``F.Fab`` Layer.
- You want to get close within reason, too close desoldering can be difficult
- Prioritize Decoupling
    - Decoupling, Crystal, Critical Sections Should be Prioritized
- Update Changes with the Schematic
    - In Video
        - Save Schematic
        - Update Netlist
        - Update PCB Layout
    - In Current Version
        - Save Schematic
        - Update PCB Layout
# Mounting hole placement
[Mark](https://www.youtube.com/watch?v=C7-8nUU6e3E&t=6797s)
- When moving components (mounting hole is the example) press space to reset the origin for measurements
    - Hotkey: With Component Selected + Spacebar = Center Origin to Component
    - Use arrow keys to move in increments of the grid
# Board outline and rounded corners
[Mark](https://www.youtube.com/watch?v=C7-8nUU6e3E&t=6910s)
- Without an outline an automatic board outline is drawn that fits all elements in the space, with pointed corners
- Select the Edge Cuts Layer
    - Select Graphic Line (Video)
        - Select Draw a Line
    - Select Add Graphic Arc
        - Draw an Arc
        - Counter Clockwise to start at 0 degrees
        - Clockwise to start with 360 degrees
# Rearranging connectors
[Mark](https://www.youtube.com/watch?v=C7-8nUU6e3E&t=7060s)
- Can use the Space Hotkey to check alignment
- For finer alignment make the grid increments smaller
- Use the 3D Layout to check the overall Layout
    - Keep in mind space for manually soldering
# Adding track widths
[Mark](https://www.youtube.com/watch?v=C7-8nUU6e3E&t=7219s)
- Select Track Sizes
    - Select pre-defined sizes... to add additional track sizes
        - Select ``+`` Button to add trace width
            - ``0.3mm`` useful for LP/PFP Package Pins
            - ``0.5mm`` to ``1mm`` Typically used for Power
        - Confirm choices by selecting ``OK``
# Power and ground planes (copper pours)
[Mark](https://www.youtube.com/watch?v=C7-8nUU6e3E&t=7255s)
- Select Inner Planes
    - Select add filed zones
        - Select a Corner of the Board (Or where edges would converge)
            - Select the type of Net
                - Select ``OK``
                    - Draw Net around the Board
                        - Do not really need to fit around the board, KiCad will do it for you
- Fill Zone by selecting the Zone you want to fill then select ``Edit`` > ``Fill all Zones``
- Connection to Thermal Reliefs are known as (Thermal) Spokes
- To copy the same on one onto another layer use Select + CTRL + D then left click then open properties then change layer
- Dedicated Power and Ground Planes allow for Easier Routing (Use a Short Wire Trace and Via) and Low Inductance
# STM32 and routing (critical items first)
[Mark](https://www.youtube.com/watch?v=C7-8nUU6e3E&t=7390s)
- Select Front Copper layer
- Route the most important things first (High Speed or Critical)
- Hotkey: X = Add Traces
- Grounding and Power can be done with Vias
# Tombstoning
[Mark](https://www.youtube.com/watch?v=C7-8nUU6e3E&t=7481s)
- For small SMD Parts
    - occurs with uneven thermal mass distribution
# Track spacing
[Mark](https://www.youtube.com/watch?v=C7-8nUU6e3E&t=7555s)
- Keep in mind track spacing to avoid cross talk interference
    - Generally 2 to 3 times the track width
- Try to have a most traces on the Top Layer and Sort Traces on the Bottom Layer
- Hotkey: (When drawing a Trace) V = Add a Via
# Buck converter routing
[Mark](https://www.youtube.com/watch?v=C7-8nUU6e3E&t=7729s)
- For Power use Thick Traces or Copper Pours
- Using Add Filed Zone you can Trace Around the Footprint to make connections
    - When Filling Select the appropriate flag
# Track width calculator
[Mark](https://www.youtube.com/watch?v=C7-8nUU6e3E&t=7800s)
- Track Width Calculator is on the Main Window
    - Can be used to calculate current
- Thicker Traces Low Inductance, good for power circuits
# USB controlled impedance differential traces
[Mark](https://www.youtube.com/watch?v=C7-8nUU6e3E&t=7959s)
- Can determine on KiCad or JLC PCB
# JLCPCB impedance calculator
[Mark](https://www.youtube.com/watch?v=C7-8nUU6e3E&t=7988s)
- Add Differential Pair by editing the predefined track sizes
- To use select Route and Select Differential Pair
- Select Differential Pair dimensions by right cliking and selecting ``Select Differential Pair Dimensions``
- Differential Pairs are denoted with ``+`` and ``-``, otherwise an error is given
# Connecting GND and 3V3 (with vias to internal copper pours)
[Mark](https://www.youtube.com/watch?v=C7-8nUU6e3E&t=8169s)
- Vias depend on the maufacturer
- Select add Vias (Video)
    - Add free-standing vias (In current version)
    - When dropped on a net it will inherit that net (node ID)
    - Get as close as possible to pad, but not in pad
        - When via is on pad solder may fall through the via in assembly
    - The more vias and the closer that they are the less inductance that is produced
    - Use Thick Short Traces
    - Minimize Inductance
- Adding Keepout Area Prevents Copper Pours from being made
- Keep in mind distances of vias to each other, specifically drill specifications
- Avoid Putting vias on the silkscreen
- Be sure to refill the coppper pours before continuing
# Design rules checker (DRC)
[Mark](https://www.youtube.com/watch?v=C7-8nUU6e3E&t=8880s)
- Select the Design Rules Checker Icon
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