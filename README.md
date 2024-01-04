![maintenance](https://img.shields.io/maintenance/yes/2024)

![pcb][pcb]
![3d model front][3d-front]
![3d model back][3d-back]

darling
=======

FTDI helper for the future. With FT230X, blinky lights and USB-C! Also potentially the tinyest USB-C to Serial adapter in the world. :smiley:

__Got a smaller USB-C to serial adapter? Please send me a link!__


BOM
---

| Part                 | Qty | Pkg   | Ref    | Description       | Mouser | LCSC |
| -------------------- | -   | ----- | ------ | ----------------- | ------ | ---- |
| Hirose CX70M-24P1    | 1   | -     | J1     | USB-C Receptacle  | [798-CX70M-24P1](https://eu.mouser.com/ProductDetail/Hirose-Connector/CX70M-24P1?qs=NniTrqY%252BJ%252BUR9QssvRGPwA%3D%3D) | [C778726](https://www.lcsc.com/product-detail/C778726.html) |
| -                    | 1   | -     | J2     | Pin Header        | [571-826947-5](https://eu.mouser.com/ProductDetail/TE-Connectivity/826947-5?qs=xF5SkmKSM76JMcUnQ8djKQ%3D%3D) | [C6332198](https://www.lcsc.com/product-detail/C6332198) |
| FTDI FT230XQ-R       | 1   | QFN16 | U1     | USB-Serial IC     | [895-FT230XQ-R](https://eu.mouser.com/ProductDetail/FTDI/FT230XQ-R?qs=Gp1Yz1mis3VvmXwyDmIHOg%3D%3D) | [C128629](https://www.lcsc.com/product-detail/C128629) |
| -                    | 1   | 0603  | D1     | Red RX LED        | [710-150060GS75000](https://eu.mouser.com/ProductDetail/Wurth-Elektronik/150060GS75000?qs=LlUlMxKIyB0UYkq5lDO8nA%3D%3D) | [C965804](https://www.lcsc.com/product-detail/C965804) |
| -                    | 1   | 0603  | D2     | Green TX LED      | [710-150060RS75000](https://eu.mouser.com/ProductDetail/Wurth-Elektronik/150060RS75000?qs=LlUlMxKIyB3QnmZ3fw%2FVCA%3D%3D) | [C965799](https://www.lcsc.com/product-detail/C965799) |
| -                    | 2   | 0402  | R1, R2 | 27 Ohm Resistor   | [652-CR0402FX-27R0GLF](https://eu.mouser.com/ProductDetail/Bourns/CR0402-FX-27R0GLF?qs=SFHnMgm9IsxG%252BvpJZf0h2g%3D%3D) | [C138021](https://www.lcsc.com/product-detail/C138021) |
| -                    | 2   | 0402  | R3, R4 | 270 Ohm Resistor  | [652-CR0402FX-2700GLF](https://eu.mouser.com/ProductDetail/Bourns/CR0402-FX-2700GLF?qs=SFHnMgm9IsyXrY3JqhOnHQ%3D%3D) | [C163474](https://www.lcsc.com/product-detail/C163474) |
| -                    | 2   | 0402  | R5, R6 | 5.1 kOhm Resistor | [652-CR0402FX-5101GLF](https://eu.mouser.com/ProductDetail/Bourns/CR0402-FX-5101GLF?qs=ePR1ZvdkOKImkuXR%2F%2FtvtA%3D%3D) | [C105873](https://www.lcsc.com/product-detail/C105873) |
| -                    | 1   | 0402  | C1     | 10 nF Capacitor   | [80-C0402C103K3R7867](https://eu.mouser.com/ProductDetail/KEMET/C0402C103K3RAC7867?qs=2QcrrtqkWlmbWpEppaNgjw%3D%3D) | [C272878](https://www.lcsc.com/product-detail/C272878) |
| -                    | 2   | 0402  | C2, C4 | 100 nF Capacitor  | [81-GRM155C71H104JE9J](https://eu.mouser.com/ProductDetail/Murata-Electronics/GRM155C71H104JE19J?qs=QzBtWTOodeUR0Y4f0k0Zww%3D%3D) | [C541464](https://www.lcsc.com/product-detail/C541464) |
| -                    | 1   | 0402  | C3     | 4.7 uF Capacitor  | [81-GRM15C61E475ME15J](https://eu.mouser.com/ProductDetail/Murata-Electronics/GRM155C61E475ME15J?qs=By6Nw2ByBD02p8xq06vhEQ%3D%3D) | [C368809](https://www.lcsc.com/product-detail/C368809) |
| -                    | 2   | 0402  | C5, C6 | 47 pF Capacitor   | [81-GRT1555C1H470FA2D](https://eu.mouser.com/ProductDetail/Murata-Electronics/GRT1555C1H470FA02D?qs=RcG8xmE7yp3he2Sm3%2FOw%252Bg%3D%3D) | [C527009](https://www.lcsc.com/product-detail/C527009) |
| Laird MI0805K601R-10 | 1   | 0805  | FB1    | Ferrite Bead      | [875-MI0805K601R-10](https://eu.mouser.com/ProductDetail/Laird-Performance-Materials/MI0805K601R-10?qs=bbdZqDPQhEXXIHxc191aOg%3D%3D) | [C21286](https://www.lcsc.com/product-detail/C21286) |

See [Octopart][octopart] for a detailed list with links.
With current prices this totals to ~4.50€ just for parts excluding costs for the PCB manufacturing. If you need a PCB, just ask. I have lots of them. :)


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
If you want it faster and you're in Germany/EU I uploaded it to [Aisler][aisler] to.

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
[aisler]: https://aisler.net/p/NFTQABKA
