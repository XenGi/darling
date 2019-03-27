![pcb][pcb] ![3d model][3d]

darling
=======

FTDI helper for the future. With FT230X, blinky lights and USB-C! Also potentially the tinyest USB-C to Serial adapter in the world. :smiley:

__Got a smaller USB-C to serial adapter? Please send me a link!__


BOM
---

| Part                 | Qty | Pkg   | Ref    | Description      |
| -------------------- | -   | ----- | ------ | ---------------- |
| Hirose CX70M-24P1    | 1   | -     | J1     | USB-C Receptacle |
| FTDI FT230XQ-R       | 1   | QFN16 | U1     | USB-Serial IC    |
| -                    | 1   | 0603  | D2     | Red TX LED       |
| -                    | 1   | 0603  | D1     | Green RX LED     |
| -                    | 2   | 0402  | R3, R4 | 270 Ohm Resistor |
| -                    | 2   | 0402  | R1, R2 | 27 Ohm Resistor  |
| -                    | 2   | 0402  | C5, C6 | 47 pF Capacitor  |
| -                    | 1   | 0402  | C1     | 10 nF Capacitor  |
| -                    | 1   | 0402  | C3     | 4.7 uF Capacitor |
| -                    | 1   | 0402  | C2     | 100 nF Capacitor |
| Laird MI0805K601R-10 | 1   | 0805  | FB1    | Ferrite Bead     |

See [Octopart][octopart] for a detailed list with links.
With current prices this totals to € 3.84 just for parts excluding costs for the PCB manufacturing.


Schematics
----------

![schematics][schema]


Create Gerber files
-------------------

After you exported the gerber and drill friles from KiCAD you can use [gerbolyze][gerbolyze] to add the artwork to it.

Instal lgerbolyze with [pipsi][pipsi]:

```
pipsi install gerbolyze
```

To produce the template I used:

```
gerbolyze render bottom . preview.png
```

Then after adding the artwork use gerbolyze again to add it to the gerber files:

```
gerbolyze vectorize bottom . art preview_002.png
```

---

_Made with :heart: and aliexpress_


[pcb]: https://gitlab.com/xengi/darling/raw/master/darling_pcb.png
[3d]: https://gitlab.com/xengi/darling/raw/master/darling_3d.png
[schema]: https://gitlab.com/xengi/darling/raw/master/darling_schema.png
[octopart]: https://octopart.com/bom-tool/4VikRkAe
[gerbolyze]: https://github.com/jaseg/gerbolyze
[pipsi]: https://github.com/mitsuhiko/pipsi

