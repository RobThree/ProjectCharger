*Testing and comparing 21 cheap USB chargers*

## Description

I ordered 21 (ultra) cheap USB chargers from AliExpress and will test them to see if they:

* can provide the power they claim to be able to deliver
* are safe to use (will they catch on fire 🔥 or even explode 💥)?
* aren't just overpriced fire hazards (provide bang-for-buck 💶💵)

## Status

**2025-03-06**: The project was started today and will take some time to complete. Currently the project is in the setup phase so this project is still 🚧 under construction 🚧. I have ordered and received ~~12~~ 21 chargers and have taken some 📷 [pictures](https://github.com/RobThree/ProjectCharger/tree/main/images). Basic data has been entered in a 📝 [Google sheet](https://docs.google.com/spreadsheets/d/1MLatioRcDbH1atz-dB_jMyGtM_djYzLRvWk6to6tpT4/edit?usp=sharing) (which will also be used to record measurements etc. during this project) for the first 12 chargers.

**2025-03-15**: All chargers have been received, all basic data has been entered into the 📝 [Google sheet](https://docs.google.com/spreadsheets/d/1MLatioRcDbH1atz-dB_jMyGtM_djYzLRvWk6to6tpT4/edit?usp=sharing). A test-protocol, to ensure all chargers undergo the same tests under the same conditions, has been written and is nearly finished. A [viewer to visualize the test results](/measurements/?data=example) has been created. Software to run the tests automated on the DL24-P has been written. After a few finishing touches, testing will commence sometime soon in the upcoming days 🎉 🚀

## Chargers

The following chargers are in this test:

1. [GUSEYEE AR-890](https://www.aliexpress.com/item/1005006205253362.html) (€1.94 / $1.79)
2. [{noname} TRG-044P](https://www.aliexpress.com/item/1005006690280370.html) (€1.39 / $1.28)
3. [GUSEYEE {nomodel}](https://www.aliexpress.com/item/1005007817217545.html) (€2.16 / $1.99)
4. [NNBILI {nomodel}](https://www.aliexpress.com/item/1005007076973487.html) (€1.55 / $1.43)
5. [GUSEYEE LYK-881](https://www.aliexpress.com/item/1005006117746435.html) (€2.45 / $2.26)
6. [Maerknon AR-893](https://www.aliexpress.com/item/1005007540830401.html) (€2.19 / $2.02)
7. [{noname} BK385B](https://www.aliexpress.com/item/1005006359348866.html) (€2.49 / $2.30)
8. [Byleen KeKe-PD002](https://www.aliexpress.com/item/1005005029886272.html) (€4.29 / $3.96)*
9. [Maerknon AD-64](https://www.aliexpress.com/item/1005006968895855.html) (€2.19 / $2.02)
10. [Maerknon KeKe-F002](https://www.aliexpress.com/item/1005008273390175.html) (€3.30 / $3.05)*
11. [WALKESEN AR-896](https://www.aliexpress.com/item/1005008390068513.html) (€3.35 / $3.09)*
12. [Maerknon NC-22](https://www.aliexpress.com/item/1005007368774221.html) (€2.51 / $2.32)
13. [Henruisi TRG-182](https://www.aliexpress.com/item/1005007713351327.html) (€1.99 / $1.84)
14. [olaf TRG-157](https://www.aliexpress.com/item/1005005447292671.html) (€1.99 / $1.84)
15. [Maerknon  61-A2C2](https://www.aliexpress.com/item/1005006294291283.html) (€1.99 / $1.84)
16. [FANBEDA BK329-4A4C](https://www.aliexpress.com/item/1005007798517528.html) (€4.39 / $4.05)
17. [{noname} BH-L01](https://www.aliexpress.com/item/1005006603699489.html) (€1.19 / $1.10)
18. [{noname} A2347 EMC 3621](https://www.aliexpress.com/item/1005006469372442.html) (€1.59 / $1.47)
19. [GUSEYEE TE-023](https://www.aliexpress.com/item/1005007370796821.html) (€1.59 / $1.47)
20. [GUSEYEE BK319](https://www.aliexpress.com/item/1005007487685097.html) (€3.99 / $3.68)
21. [{noname} 62-CCA](https://www.aliexpress.com/item/1005005586923234.html) (€1.59 / $1.47)

<sup>* Ordered in US version by (my) mistake. Other than the plug standard / format there shouldn't be any difference. These chargers will be tested with a simple adapter plug.</sup>

As a 'control' group (to prove the USB cables are good, the USB tester detects all protocols etc.) we have the following "expensive" or "brand" chargers:

1. [UGREEN Nexode 100W USB C GaN Charger CD226](https://www.aliexpress.com/item/1005002529458406.html) (€54.99 / $59.55)
2. [UGREEN Nexode 200W USB C GaN Charger CD271](https://www.aliexpress.com/item/1005008473171077.html) (€117.39 / $127.11)
3. [Xiaomi Power Bank 3 Pro PLM07ZM](https://www.aliexpress.com/item/1005007232373605.html) (€45.39 / $49.15)
4. [Shenzhen GOOD-SHE Technology Co., Ltd. GS-W65A0927](http://www.good-she.com/web/index.php/product/index/g/e/id/278.html) (€25.00 / $27.07)

## Test protocol

The test protocol is currently being determined but will include:

- [ ] 🔌 Measuring current draw from outlet
- [x] 📱 Determining supported USB protocols
- [ ] 📐 Measuring output in several combinations, setups and durations, each test producing:
    - [ ] ⚡ Measurements (Voltage, current, temperature, ...) at:
        - [ ] No load for 1 minute
        - [ ] Rampup over 5 minutes from 0.2A to 150% of rated load
        - [ ] 50% of load for 5 minutes
        - [ ] 90% of load for 5 minutes
        - [ ] Rated load for 30 minutes
        - [ ] 110% of load for 20 minutes
        - [ ] 125% of load for 20 minutes
        - [ ] 150% of load for 20 minutes
        - [ ] 200% of load for 20 minutes
    - [x] ⚖️ Weight
    - [ ] 🌡️ Infrared image
    - [ ] 📉 Voltage / current graphs
    - [ ] 📈 Ripple
- [ ] Teardown pictures

Measurements will be done using an [Atorch DL24-P](http://en.atorch.cn/ProDetail.aspx?ProID=13), [FNIRSI FNB58](https://www.fnirsi.com/products/fnb58), [Geti PM001](https://www.geti.eu/en/products/energy/power-consumption-meters/digital-energy-meter-geti-pm001), [Kaiweets KTI-W01](https://kaiweets.com/products/kti-w01-handheld-thermal-camera), [Hanmatek DOS1102](https://www.aliexpress.com/item/4000768225718.html), [OWON XDM1241](https://www.owon.com.hk/products_owon_4_1%7C2_digits_xdm1000_series_bench-type_digital_multimeter), [Imtex precision scale](https://www.bol.com/nl/nl/p/imtex-precisie-digitale-weegschaal-500-gram-x-001-gram/9300000074911968/), [UGREEN 240W USB-C to USB-C cable (0.5m)](https://www.amazon.com/UGREEN-Charging-Charger-Compatible-MacBook/dp/B0D1VMZQY4/ref=sr_1_1), [UGREEN 18W USB-A to USB-C cable (0.5m)](https://www.amazon.com/UGREEN-Braided-Charger-Compatible-Nintendo/dp/B07PP2RB25/ref=sr_1_2) and [UGREEN 18W USB-A to USB-C Adapter](https://www.amazon.com/UGREEN-Adapter-Charger-Connector-AirPods/dp/B0CZDQ8RMX/ref=sr_1_3). Not the most expensive or best test equipment, but will do fine for this project. Non-affiliate links.

## Atribution

Icon by [Payungkead](https://www.freepik.com/icon/usb_1664704)