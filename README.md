# SilviaEv6ModPCB
Ranzillio Silvia E v6 Mod PCB

# Umsetzung
Heizung -> triac mit Vollwellensteuerung (auch als Wellenpaketsteuerung oder Schwingungspaketsteuerung bezeichnet)
Pumpe -> triac mit phasenanschnitt
sd card für logging esp32

Aufteilung Heiße (mit 230V in Kontakt) seite und Kalteseite (berührsicher selv/pelv)

Tempsensor - z.B. PTFM101A1A0 + MAX31865ATP+ (rref 4k4-4k3 kleine Toleranz + niedriger Tempco)

Füllstand - capacitive water level sensor
Durchfluss? - https://www.bluestarcoffee.eu/en/Flow-Meter/c-291.aspx
Druck? - MIPAN2XX250PSAAX
Wage - ali

-> pid?https://chatgpt.com/c/68faa822-5314-832d-b250-4dfe659e43ed


# Parts
Triac T3035H-6x - heizung & pumpe (snuber,tsv, mov) Source 1 -> beschaltung ev fig 7

MPM-05-5 - AC/DC-Leistungsmodule 5W 5V 1A Medical Enclosed PS -4kV iso - class 2 doppel isoliert (Kalt)
IRM-01-5  - AC/DC-Leistungsmodule 1W 5V 200mA 85-305Vin PCB Encap - 3k iso (Heiß)

16.385 MHz quarz + 2 x 22pf

MUC PIC18F57K42 - hot und ?cold? +/ ?esp32? - cold rtc?

# Funktionen
230V spannungs und leistungsmessung
tempsensoren am board (hot side)  - safety
heizung Vollwellensteuerung
pumpe phasenanschnitt




´https://www.auberins.com/index.php?main_page=product_info&products_id=32
https://www.digikey.at/de/products/detail/honeywell-sensing-and-productivity-solutions/MIPAN2XX250PSAAX/21714602?srsltid=AfmBOoo4Ey67G2LzALe45ssn8JAZVsFlubCIujuodjsKur_KNoKfqMFf

# Sources
- 1 [Microchip Application Note AN521 – Interfacing to AC Power Lines (PDF)](https://ww1.microchip.com/downloads/en/AppNotes/00521c.pdf)
- 2 https://www.st.com/resource/en/application_note/an440-triac-control-with-a-microcontroller-powered-from-a-positive-supply-stmicroelectronics.pdf
- 3 AN937 Implementing a PID Controller Using a PIC18 MCU https://ww1.microchip.com/downloads/aemDocuments/documents/OTH/ApplicationNotes/ApplicationNotes/00937a.pdf

https://class.ece.iastate.edu/ee330/miscHandouts/AN_GOLDEN_RULES.pdf

https://ww1.microchip.com/downloads/en/Appnotes/90003138A.pdf

https://www.st.com/resource/en/application_note/an437-rc-snubber-circuit-design-for-triacs-stmicroelectronics.pdf
https://www.st.com/resource/en/application_note/an439-snubberless-and-logic-level-triac-behavior-at-turnoff-stmicroelectronics.pdf
https://www.mikrocontroller.net/attachment/29129/snubber_n1.pdf
https://learnabout-electronics.org/Downloads/HIQUEL_Snubber_AppNote_EN_0100.pdf
https://www.onsemi.cn/pub/Collateral/AN-3008JP.pdf
https://mediac.industry.panasonic.eu/p/2021-12/AN_030_Driving_Triacs_with_Phototriacs_211110.pdf
https://e2e.ti.com/cfs-file/__key/communityserver-discussions-components-files/234/Snubbing-methods-slup100.pdf
https://www.st.com/resource/en/application_note/an5114-controlling-a-triac-with-a-phototriac-stmicroelectronics.pdf
https://www.st.com/resource/en/application_note/an440-triac-control-with-a-microcontroller-powered-from-a-positive-supply-stmicroelectronics.pdf
https://www.vishay.com/docs/84780/appnote34.pdf
https://datasheet.datasheetarchive.com/originals/distributors/Datasheets-NXP/DSANXP0100024.pdf - 3Q / 4Q triac

https://www.infineon.com/assets/row/public/documents/60/42/infineon-triac-control-using-imotion-script-applicationnotes-en.pdf?fileId=8ac78c8c8e7ead30018ec6fcf8f04439


https://www.vishay.com/docs/92368/sihb24n80ae.pdf
T1635T-8G


https://www.amazon.com/Cooling-Techniques-Electronic-Equipment-2nd/dp/0471524514
