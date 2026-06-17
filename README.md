# Laser Cutter Infrastructure Controls System
Relay-logic based controls system to manage water-cooling, fume ventilation, and other auxiliary functions for the laser cutter &amp; digital fabrication space at the Walker Art Center.

## Control Flow
<p align="center">
  <img src="media/controls-block-diagram.png" alt="block diagram" style="width:100%; height:automatic">
</p>

### Overview:
* The **Paint Booth Air Handling Unit (AHU)** and local **Blower Fan** ensured to be always on while **Laser** or **Fume Hood** in use.
* During operation, the switch in the **Paint Booth** is interrupted so that it may not be used to turn off **Paint Booth AHU**.
* Power to both a **Utility Outlet** at the fume hood workbench (to restrict access to fume-generating tools, like a soldering iron) and internal **Laser Tube** will be interrupted until correct orientation of **Blast Gates** is met, with **Indicator Lights** providing visual feedback.

## Fabrication Files
> 📂 **[acrylic parts](acrylic%20parts)/**
> - 📁 [`source`](acrylic%20parts/source)/ — *Editable Corel Draw design files*
>   - 🗒️ [`indicator-light-enclosure-WAC.cdr`](acrylic%20parts/source/indicator-light-enclosure-WAC.cdr)
>   - 🗒️ [`relay-controller-main-enclosure-WAC.cdr`](acrylic%20parts/source/relay-controller-main-enclosure-WAC.cdr)
>   - 🗒️ [`relay-controller-water-cooler-enclosure.cdr`](acrylic%20parts/source/relay-controller-main-enclosure-WAC.cdr)
> - 🗒️ [`indicator-light-enclosure-WAC.dxf`](acrylic%20parts/indicator-light-enclosure-WAC.dxf) — *Enclosre for red/green blast gate satus indicator lights*
> - 🗒️ [`relay-controller-main-enclosure-WAC.dxf`](acrylic%20parts/relay-controller-main-enclosure-WAC.dxf) — *Enclosure for primary relay logic module*
> - 🗒️ [`relay-controller-water-cooler-enclosure-WAC.dxf`](acrylic%20parts/relay-controller-water-cooler-enclosure-WAC.dxf) — *Enclosure for water cooler activation relay*
