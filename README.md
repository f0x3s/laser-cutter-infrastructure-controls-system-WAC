# Laser Cutter Infrastructure Controls System
Relay-logic based controls system to manage water-cooling, fume ventilation, and other auxiliary functions for the laser cutter &amp; digital fabrication space at the Walker Art Center.

## Control Flow
<p align="center">
  <img src="media/controls-block-diagram.png" alt="block diagram" style="width:100%; height:automatic">
</p>
<br>
<em>Additionally: Laser and Cooling module placed on same switched circuit, ensuring Cooling Module is always engaged during Laser operation. OPTIONAL: uptime counter placed parallel to this circuit to facilitate tracking machine hours & water replacement intervals.</em>

## Fabrication Files
> 📂 **[acrylic parts](acrylic%20parts)/**
> - 📁 [`source`](acrylic%20parts/source)/ — *Editable Corel Draw design files*
>   - 🗒️ [`indicator-light-enclosure-WAC.cdr`](acrylic%20parts/source/indicator-light-enclosure-WAC.cdr)
>   - 🗒️ [`relay-controller-main-enclosure-WAC.cdr`](acrylic%20parts/source/relay-controller-main-enclosure-WAC.cdr)
>   - 🗒️ [`relay-controller-water-cooler-enclosure.cdr`](acrylic%20parts/source/relay-controller-main-enclosure-WAC.cdr)
> - 🗒️ [`indicator-light-enclosure-WAC.dxf`](acrylic%20parts/indicator-light-enclosure-WAC.dxf) — *Enclosre for red/green blast gate satus indicator lights*
> - 🗒️ [`relay-controller-main-enclosure-WAC.dxf`](acrylic%20parts/relay-controller-main-enclosure-WAC.dxf) — *Enclosure for primary relay logic module*
> - 🗒️ [`relay-controller-water-cooler-enclosure-WAC.dxf`](acrylic%20parts/relay-controller-water-cooler-enclosure-WAC.dxf) — *Enclosure for water cooler activation relay*
