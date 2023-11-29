![maintenance](https://img.shields.io/maintenance/yes/2023)
[![Donate using Liberapay](https://liberapay.com/assets/widgets/donate.svg)](https://liberapay.com/xengi/donate)

![pcb][pcb]
![3d model front][3d-front]
![3d model back][3d-back]

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
| -                    | 1   | 0603  | D2     | Green TX LED     |
| -                    | 1   | 0603  | D1     | Red RX LED       |
| -                    | 2   | 0402  | R3, R4 | 270 Ohm Resistor |
| -                    | 2   | 0402  | R1, R2 | 27 Ohm Resistor  |
| -                    | 2   | 0402  | C5, C6 | 47 pF Capacitor  |
| -                    | 1   | 0402  | C1     | 10 nF Capacitor  |
| -                    | 1   | 0402  | C3     | 4.7 uF Capacitor |
| -                    | 2   | 0402  | C2, C4 | 100 nF Capacitor |
| Laird MI0805K601R-10 | 1   | 0805  | FB1    | Ferrite Bead     |

See [Octopart][octopart] for a detailed list with links.
With current prices this totals to € 3.84 just for parts excluding costs for the PCB manufacturing. If you need a PCB, just ask. I have lots of them. :)


Schematics
----------

![schematics][schema]


Create Gerber files
-------------------

Export the gerber and drill files from KiCAD to a subdir like `gerber`. To create a ZIP file with the needed gerber files for a PCB fab:

```
cd gerber
zip darling.zip *.gbr *.drl
```

I recommend [JLCPCB][jlcpcb]. It's the cheapest way to get the PCBs and they offer decent quality.
If you want purple PCBs you can also use [OSHPark][oshpark].
If you want it faster and you're in Germany I uploaded it to [Aisler][aisler] to.

[![pcb top][oshpark_darling_top] ![pcb bottom][oshpark_darling_bottom]][oshpark]

---

_Made with :heart: and aliexpress_


[pcb]: https://gitlab.com/xengi/darling/raw/master/darling_pcb.png
[3d-front]: https://gitlab.com/xengi/darling/raw/master/darling_3d_front.png
[3d-back]: https://gitlab.com/xengi/darling/raw/master/darling_3d_back.png
[schema]: https://gitlab.com/xengi/darling/raw/master/darling_schema.png
[octopart]: https://octopart.com/bom-tool/4VikRkAe
[jlcpcb]: https://jlcpcb.com/
[oshpark_darling_top]: https://644db4de3505c40a0444-327723bce298e3ff5813fb42baeefbaa.ssl.cf1.rackcdn.com/4cf1ffcfeee0332e9eda92195310da6b.png
[oshpark_darling_bottom]: https://644db4de3505c40a0444-327723bce298e3ff5813fb42baeefbaa.ssl.cf1.rackcdn.com/1f266f38a687f960f46bc39729592b03.png
[oshpark]: https://oshpark.com/shared_projects/s8UnAcGC
[aisler]: https://aisler.net/p/RTBHDJQK
