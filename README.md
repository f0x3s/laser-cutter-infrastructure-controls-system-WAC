# Laser Cutter Infrastructure Controls System
Relay-logic based controls system to manage water-cooling, fume ventilation, and other auxiliary functions for the laser cutter &amp; digital fabrication space at the Walker Art Center.

## Control Flow
<p align="center">
  <img src="media/controls-block-diagram.png" alt="block diagram" style="width:100%; height:automatic">
</p>
<br>
<em>Additionally: Laser and Cooling module placed on same switched circuit, ensuring Cooling Module is always engaged during Laser operation. OPTIONAL: uptime counter placed parallel to this circuit to facilitate tracking machine hours & water replacement intervals.</em>
