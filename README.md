# Laser Cutter Infrastructure Controls System
Relay-logic-based controls system to manage water-cooling, fume ventilation, and other auxiliary functions for the laser cutter &amp; digital fabrication space at the Walker Art Center.

This is intended as a maintenance resource for the existing system. Instructions for building a new system from scratch are currently outside of the scope of this repo.

> ### Additional Resources:
> * [arduino-industrial-AHU-status-indicator-WAC](https://github.com/f0x3s/arduino-industrial-AHU-status-indicator-WAC) — *Real-time feedback module for the __Paint Booth AHU__*
> * [arduino-industrial-AHU-controller-WAC](https://github.com/f0x3s/arduino-industrial-AHU-controller-WAC) — *Interface beween control module and __Paint Booth AHU__ 3-phase motor controller*

## Control Flow
<p align="center">
    <img src="media/controls-block-diagram.png" alt="control flow block diagram" style="width:100%; height:automatic">
</p>

### Overview:
* **Water Cooling Pump** controlled with **Laser Power Button**, ensuring **Water Cooling Pump** is always engaged during **Laser** operation. 
* The **Paint Booth Air Handling Unit (AHU)** and local **Blower Fan** ensured to be always on while **Laser** or **Fume Hood** in use.
* Power to both a **Utility Outlet** at the fume hood workbench (to restrict access to fume-generating tools, like a soldering iron) and internal **Laser Tube** will be interrupted until correct orientation of **Blast Gates** is met, with **Indicator Lights** providing visual feedback.
* While not explicitly shown in this diagram, during operation of either the **Laser** or **Fume Hood** the switch in the **Paint Booth** is interrupted at the **Paint Booth AHU** motor controller in the **Fan Room** so that it may not be used to turn off **Paint Booth AHU**. See: ['arduino-industrial-AHU-controller-WAC'](https://github.com/f0x3s/arduino-industrial-AHU-status-indicator-WAC)

## Air Handling Diagram
<p align="center">
    <img src="media/air-handling-diagram.png" alt="air handling diagram" style="width:100%; height:automatic">
</p>

#### Air Handling Specialty Parts
| qty | name | source |
| ------------: | :-----------: | :-----------: |
| 2 | Long Ranger 4 in. Aluminum Blast Gate with Switch | [Penn State Industries](https://www.pennstateind.com/store/LRGATE.html?utm_source=google&utm_medium=cpc&utm_campaign=21194399893&utm_content=&utm_term=&gad_source=1&gad_campaignid=21194400664&gbraid=0AAAAAD_LBLIuMktPh1lfJFACbiyh2TnXP&gclid=EAIaIQobChMI3ufmtN_jkwMVvz0IBR3NKySaEAQYAiABEgKDNPD_BwE) |
| 1 | 6" Backdraft Damper | [Amazon](https://a.co/d/00BVJb6u) |

## Circuit Diagrams
#### Main Control Module
<p align="center">
    <img src="circuit%20diagrams/main-controller-circuit-WAC.png" alt="main control module electrical schematic" style="width:100%; height:automatic">
</p>

#### Indicator Light Modules
<p align="center">
    <img src="circuit%20diagrams/indicator-light-circuit-WAC.png" alt="indicator modules electrical schematic" style="width:100%; height:automatic">
</p>

#### Water Cooler Control Module
<p align="left">
    <img src="circuit%20diagrams/water-cooler-control-circuit-WAC.png" alt="water cooler control module electrical schematic" style="width:36%; height:automatic">
</p>

## Fabrication Files
All files to be cut from 0.25" acrylic unless otherwise specified.
> 📂 **[acrylic parts](acrylic%20parts)/**
> - 📁 [`source`](acrylic%20parts/source)/ — *Editable Corel Draw design files*
>   - 🗒️ [`indicator-light-enclosure-WAC.cdr`](acrylic%20parts/source/indicator-light-enclosure-WAC.cdr)
>   - 🗒️ [`relay-controller-main-enclosure-WAC.cdr`](acrylic%20parts/source/relay-controller-main-enclosure-WAC.cdr)
>   - 🗒️ [`relay-controller-water-cooler-enclosure.cdr`](acrylic%20parts/source/relay-controller-main-enclosure-WAC.cdr)
> - 🗒️ [`indicator-light-enclosure-WAC.dxf`](acrylic%20parts/indicator-light-enclosure-WAC.dxf) — *Enclosure for red/green blast gate status indicator lights*
> - 🗒️ [`relay-controller-main-enclosure-WAC.dxf`](acrylic%20parts/relay-controller-main-enclosure-WAC.dxf) — *Enclosure for primary relay logic module*
> - 🗒️ [`relay-controller-water-cooler-enclosure-WAC.dxf`](acrylic%20parts/relay-controller-water-cooler-enclosure-WAC.dxf) — *Enclosure for water cooler activation relay*

## Control Modules Parts Lists
_note: qty given as needed for assembly, without respect to package quantity from sources_
#### Indicator Light Module (per module)
_Requires 1x [`indicator-light-enclosure-WAC.dxf`](acrylic%20parts/indicator-light-enclosure-WAC.dxf)_
| qty | name | source |
| ------------: | :-----------: | :-----------: |
| 10 | M3 nuts | [McMaster](https://www.mcmaster.com/90710A030/) |
| 8 | M3 x 16mm Button Head Machine Screw | [McMaster](https://www.mcmaster.com/92095A184/) |
| 2 | M3 x 35mm Button Head Machine Screw | [McMaster](https://www.mcmaster.com/92095A201/) |
| 2 | Nylon Standoff | [McMaster](https://www.mcmaster.com/90176A166/) |
| 2 |  3/16 x 1-3/4 concrete screw | [McMaster](https://www.mcmaster.com/90161A725/) |
| 1 |  RJ45 Socket Breakout | [Amazon](https://a.co/d/0dmWGGhN) |
| 1 |  Red & Green Indicator Light Pair | [Amazon](https://a.co/d/08HnO1Rn) |
| As Needed | Misc Hookup Wire | [Amazon](https://a.co/d/0hACIMdw) |

#### Main Control Module
_Requires 1x [`relay-controller-main-enclosure-WAC.dxf`](acrylic%20parts/relay-controller-main-enclosure-WAC.dxf)_
| qty | name | source |
| ------------: | :-----------: | :-----------: |
| 24 | M3 nuts | [McMaster](https://www.mcmaster.com/90710A030/) |
| 20 | M3 x 16mm Button Head Machine Screw | [McMaster](https://www.mcmaster.com/92095A184/) |
| 4 | Nylon Standoff | [McMaster](https://www.mcmaster.com/90176A166/) |
| 4 |  3/16 x 1-3/4 concrete screw | [McMaster](https://www.mcmaster.com/90161A725/) |
| 4 |  1/2NPT Cable Grip | [Mouser](https://mou.sr/3KeBc74) |
| 4 |  1/2NPT Cable Grip Nut | [Mouser](https://mou.sr/3WWg4U7) |
| 2 | Murrelektronik Interface relay | [Automation Direct](https://www.automationdirect.com/adc/shopping/catalog/relays_-z-_timers/electro-mechanical_relays/52102) |
| 5 | 781-1C-24D Ice Cube Relay | [Automation Direct](https://www.automationdirect.com/adc/shopping/catalog/relays_-z-_timers/electro-mechanical_relays/781-1c-24d) |
| 5 | 781 Series Mounting Socket | [Automation Direct](https://www.automationdirect.com/adc/shopping/catalog/relays_-z-_timers/relay_-a-_timer_sockets/781-1c-skt) |
| 3 | 275mm DIN Rail | [Automation Direct](https://www.automationdirect.com/adc/shopping/catalog/wire_-a-_cable_management/din_rail/din_rail/dn-r35s-275-4) |
| 2 |  Solid State Relay | [Amazon](https://a.co/d/05lO5lyu) |
| 2 |  Aluminum SSR Heatsink | [Amazon](https://a.co/d/04LpVrm3) |
| 1 |  24v PSU (120w) | [Amazon](https://a.co/d/0cFTalkx) |
| 2 |  RJ45 Socket Breakout | [Amazon](https://a.co/d/0dmWGGhN) |
| 2 |  Lighted Edison Plug Set | [Amazon](https://a.co/d/048plgdh) |
| 1 |  IEC Panel-Mount Male Bulkhead | [Amazon](https://a.co/d/0hY4DzyT) |
| As Needed | Misc. Hookup Wire | [Amazon](https://a.co/d/0hACIMdw) |
| As Needed | Misc. Fork Connectors | [Amazon](https://a.co/d/01KCsaIr) |
| As Needed | Misc. Wago Connectors | [Amazon](https://a.co/d/03hsfrAt) |
| As Needed | 25a Bulk Extension Cord Wire | in-house |
| As Needed | 18ga 2-conductor speaker wire or equiv. | in-house |

#### Water Cooler Control Module
_Requires 1x [`relay-controller-water-cooler-enclosure-WAC.dxf`](acrylic%20parts/relay-controller-water-cooler-enclosure-WAC.dxf)_
| qty | name | source |
| ------------: | :-----------: | :-----------: |
| 10 | M3 nuts | [McMaster](https://www.mcmaster.com/90710A030/) |
| 10 | M3 x 16mm Button Head Machine Screw | [McMaster](https://www.mcmaster.com/92095A184/) |
| 3 | Nylon Standoff | [McMaster](https://www.mcmaster.com/90176A166/) |
| 3 |  3/16 x 1-3/4 concrete screw | [McMaster](https://www.mcmaster.com/90161A725/) |
| 3 |  1/2NPT Cable Grip | [Mouser](https://mou.sr/3KeBc74) |
| 3 |  1/2NPT Cable Grip Nut | [Mouser](https://mou.sr/3WWg4U7) |
| 1 |  12v PSU (60w) | [Amazon](https://a.co/d/06WrZoo5) |
| 1 |  Solid State Relay | [Amazon](https://a.co/d/05lO5lyu) |
| 1 |  Aluminum SSR Heatsink (Large) | [Amazon](https://a.co/d/043KxMh4) |
| 2 |  Lighted Edison Plug Set | [Amazon](https://a.co/d/048plgdh) |
| 1 | .25w 1k Resistor | in-house |
| As Needed | Misc. Hookup Wire | [Amazon](https://a.co/d/0hACIMdw) |
| As Needed | Misc. Fork Connectors | [Amazon](https://a.co/d/01KCsaIr) |
| As Needed | Misc. Wago Connectors | [Amazon](https://a.co/d/03hsfrAt) |
| As Needed | 25a Bulk Extension Cord Wire | in-house |
| As Needed | 18ga 2-conductor speaker wire or equiv. | in-house |

