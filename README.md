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
| -                    | 1   | 0603  | D2     | Green TX LED     |
| -                    | 1   | 0603  | D1     | Red RX LED       |
| -                    | 2   | 0402  | R3, R4 | 270 Ohm Resistor |
| -                    | 2   | 0402  | R1, R2 | 27 Ohm Resistor  |
| -                    | 2   | 0402  | C5, C6 | 47 pF Capacitor  |
| -                    | 1   | 0402  | C1     | 10 nF Capacitor  |
| -                    | 1   | 0402  | C3     | 4.7 uF Capacitor |
| -                    | 1   | 0402  | C2     | 100 nF Capacitor |
| Laird MI0805K601R-10 | 1   | 0805  | FB1    | Ferrite Bead     |

See [Octopart][octopart] for a detailed list with links.
With current prices this totals to € 3.84 just for parts excluding costs for the PCB manufacturing. If you need a PCB, just ask. I have lots of them. :)


Schematics
----------

![schematics][schema]


Create Gerber files
-------------------

After you exported the gerber and drill friles from KiCAD to a subdir like `gerber` you can use [gerbolyze][gerbolyze] to add the artwork to it.

Install gerbolyze with [pipsi][pipsi]:

```
pipsi install gerbolyze
```

I already created the template with `gerbolyze render bottom gerber preview.png` and added the artwork to the correct places.
To add the results to the gerber files use:

```
gerbolyze vectorize bottom gerber gerber_art preview_002.png
```

This will create the needed gerber files including the artwork in a directory call `gerber_art`.

To create a ZIP file with the needed gerber files for a PCB fab:

```
cd gerber_art
zip darling.zip *.gbr *.drl
```

I recommend [JLBPCB][jlbpcb] or [PCBWay][pcbway].
If you want a purple PCB you can also use [OSHPark][oshpark]. I even uploaded the file for you: ;)

[![https://oshpark.com/shared_projects/kPzv7Vwt][oshpark_darling_top] ![https://oshpark.com/shared_projects/kPzv7Vwt][oshpark_darling_bottom]][oshpark_darling]

---

_Made with :heart: and aliexpress_


[pcb]: https://gitlab.com/xengi/darling/raw/master/darling_pcb.png
[3d]: https://gitlab.com/xengi/darling/raw/master/darling_3d.png
[schema]: https://gitlab.com/xengi/darling/raw/master/darling_schema.png
[octopart]: https://octopart.com/bom-tool/4VikRkAe
[gerbolyze]: https://github.com/jaseg/gerbolyze
[pipsi]: https://github.com/mitsuhiko/pipsi
[jlbpcb]: https://jlcpcb.com/
[pcbway]: https://www.pcbway.com/
[oshpark]: https://oshpark.com/
[oshpark_darling_top]: https://644db4de3505c40a0444-327723bce298e3ff5813fb42baeefbaa.ssl.cf1.rackcdn.com/4cdf6730748bda62907702a63351273b.png
[oshpark_darling_bottom]: https://644db4de3505c40a0444-327723bce298e3ff5813fb42baeefbaa.ssl.cf1.rackcdn.com/9d2aeb22657234e79337596994ee9007.png
[oshpark_darling]: https://oshpark.com/shared_projects/kPzv7Vwt
