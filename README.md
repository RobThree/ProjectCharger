*Testing and comparing 21 cheap USB chargers*

## Description

I ordered 21 (ultra) cheap USB chargers from AliExpress and will test them to see if they:

* can provide the power they claim to be able to deliver
* are safe to use (will they catch on fire 🔥 or even explode 💥)?
* aren't just overpriced fire hazards (provide bang-for-buck 💶💵)

## Status

### 2025-03-06
The project was started today and will take some time to complete. Currently the project is in the setup phase so this project is still 🚧 under construction 🚧. I have ordered and received ~~12~~ 21 chargers and have taken some 📷 [pictures](https://github.com/RobThree/ProjectCharger/tree/main/images). Basic data has been entered in a 📝 [Google sheet](https://docs.google.com/spreadsheets/d/1MLatioRcDbH1atz-dB_jMyGtM_djYzLRvWk6to6tpT4/edit?usp=sharing) (which will also be used to record measurements etc. during this project) for the first 12 chargers.

### 2025-03-15
All chargers have been received, all basic data has been entered into the 📝 [Google sheet](https://docs.google.com/spreadsheets/d/1MLatioRcDbH1atz-dB_jMyGtM_djYzLRvWk6to6tpT4/edit?usp=sharing). A test-protocol, to ensure all chargers undergo the same tests under the same conditions, has been written and is nearly finished. A [viewer to visualize the test results](/measurements/?data=example) has been created. Software to run the tests automated on the DL24-P has been written. After a few finishing touches, testing will commence sometime soon in the upcoming days 🎉 🚀

### 2025-03-26
Today the second DL24-P came in. Unfortunately this did present a [small issue](https://github.com/RobThree/LibAtorch/issues/1) but I'm confident I'll be able to fix it and worst case this isn't even a showstopper anyway. In other news: under [A word on software (and a bit of hardware)](#a-word-on-software-and-a-bit-of-hardware) you'll find more about a [Custom ambient sensor](https://github.com/RobThree/TemperatureDisplay) I made to reliably and consistently measure ... well, ambient temperature for this project. The people over at PCBWay picked up on this project and were kind enough to reach out to me and sponsor the PCB for that project. I'm looking forward to team up with them and see what else we can do! Thank you PCBWay!

<p align="center"><a href="https://www.pcbway.com/"><img src="images/pcbway-logo.svg" width="200"></a></p>

### 2025-04-06
\*sigh* I can't get the second DL24-P to work with my previous implementation. However, all is not lost. All we have to do is reverse engineer the "native" protocol. Which, I'm happy to say, seems to be not _that_ hard. I'm expecting this to take a few days at most. Up until now I had implemented the ["PX100" protocol](https://github.com/misdoro/Electronic_load_px100/blob/be917afdaf9b361c7a3b5b8457e706a63e4c65c8/protocol_PX-100_2_70.md) but that appears to only work on the older model. I am currently well on my way to supporting the "native" protocol though. And that should be the last "major hurdle". I'll be back! **Update**: Dangit 😒 This protocol doesn't allow to set values like current or the timer. It only allows to control the 'cursor' and send 'up' / 'down' commands. That's like controlling the device blindfolded. I have contacted Atorch but hope on any useful response is low. I'm looking for alternatives (flashing the firmware to a newer or older version, extracting the firmware of the older device, ... not sure yet).

### 2025-04-21
**Let's goooo!** 🚀 I [contacted Atorch](http://en.atorch.cn/Contact.aspx?ClassID=5), honestly not even expecting a reply, but after a little back-and-forth I got them to send me a firmware update that seems to support the "PX100" protocol. Details can be found [here](https://github.com/RobThree/LibAtorch/issues/1#issuecomment-2817383225). I have asked Atorch politely if I can share the firmware file online and am waiting for their reply. Keep watching [this issue](https://github.com/RobThree/LibAtorch/issues/1#issuecomment-2817383225) for updates on that. I will be testing the firmware soon and then there's just one hurdle left: getting the data files to 'align' and put them into a nice interactive graph. But once I have my testsetup working (reliably) I will start doing the tests and dump the data in the repository. Aligning the data, making the graphs is a tomorrow problem. Any day now! 🎉🥳

**Update**: We got [the green light](https://github.com/RobThree/LibAtorch/issues/1#issuecomment-2818287076)!

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
- [ ] 📐 Measuring output in several combinations, setups (e.g. single / dual load) and durations, each test producing:
    - [ ] ⚡ Measurements (Voltage, current, temperature, ...) at:
        - [ ] No load for 1 minute
        - [ ] Rampup over 5 minutes from 0.2A to 150% of rated load with 100mA increments
        - [ ] 50% of load for 5 minutes
        - [ ] 90% of load for 5 minutes
        - [ ] Rated load for 30 minutes
        - [ ] 110% of load for 20 minutes
        - [ ] 125% of load for 20 minutes
        - [ ] 150% of load for 20 minutes
    - [x] ⚖️ Weight
    - [ ] 🌡️ Infrared image
    - [ ] 📉 Voltage / current / ripple / power graphs
- [ ] Teardown pictures

Measurements will be done using two [Atorch DL24-P](http://en.atorch.cn/ProDetail.aspx?ProID=13)s, a [FNIRSI FNB58](https://www.fnirsi.com/products/fnb58), [Geti PM001](https://www.geti.eu/en/products/energy/power-consumption-meters/digital-energy-meter-geti-pm001), [Kaiweets KTI-W01](https://kaiweets.com/products/kti-w01-handheld-thermal-camera), [Hanmatek DOS1102](https://www.aliexpress.com/item/4000768225718.html), [OWON XDM1241](https://www.owon.com.hk/products_owon_4_1%7C2_digits_xdm1000_series_bench-type_digital_multimeter), [Imtex precision scale](https://www.bol.com/nl/nl/p/imtex-precisie-digitale-weegschaal-500-gram-x-001-gram/9300000074911968/), [UGREEN 240W USB-C to USB-C cable (0.5m)](https://www.amazon.com/UGREEN-Charging-Charger-Compatible-MacBook/dp/B0D1VMZQY4/ref=sr_1_1), [UGREEN 18W USB-A to USB-C cable (0.5m)](https://www.amazon.com/UGREEN-Braided-Charger-Compatible-Nintendo/dp/B07PP2RB25/ref=sr_1_2) and [UGREEN 18W USB-A to USB-C Adapter](https://www.amazon.com/UGREEN-Adapter-Charger-Connector-AirPods/dp/B0CZDQ8RMX/ref=sr_1_3). Not the most expensive or best test equipment, but will do fine for this project. Non-affiliate links.

The actual, latest, checklist used during each test can be found [here](https://docs.google.com/document/d/16yQ9Ut7cN_zhgGhayaSNGSPf_FatyJ9KrqO3Fal7ofQ/edit?usp=sharing).

## A word on software (and a bit of hardware)

I've tried to automate a lot of this project. Mostly because testing these chargers is pretty repetitive, but more importantly I want to make sure every test is as identical as possible.

Some of my test equipment can be controlled over (USB virtual) serial port or comes with software that can export data to some file format. If this project amounts to nothing then at least I will have made my mark in the test and measurement devices .Net codespace 😅 Most of the software I had to develop for this project is open source and whatever is released is released, as always, as MIT.

The following application or packages were developed during, or before, this project:

* [OwonBinfileReader](https://github.com/RobThree/OwonBinfileReader): Reads OWON (and Hanmatek) oscilloscope `.bin` files. I had to reverse engineer the file format mostly myself. Information is very scarce on the web on this file format. It turns out my oscilloscope (the Hanmatek DSO1102, which is a rebranded version of the OWON SDS1102 as far as I know) also supports [SCPI](https://en.wikipedia.org/wiki/Standard_Commands_for_Programmable_Instruments). I had done an SCPI implementation a couple of months before for my OWON XDM1241 and I briefly considered implementing a 'client' for the oscilloscope too but that rabbit hole went a little too far off road for this project. I may still do so in the future...
* [CFNReader](https://github.com/RobThree/CFNReader) - Provides a simple way to read FNIRSI's CFN files (*.cfn) produced by the FNIRSI USB meter tool. I haven't been able to communicate directly with the USB meter yet, but am interested in any information about this. For now, reading a `.cfn` file will have to do.
* [LibAtorch](https://github.com/RobThree/LibAtorch): A library for reading and commanding Atorch devices. With this package you can control your Atorch load. This is the main one; it controls the electronic load (or: plural in a later stage..) that is hooked up to the chargers to test them at different levels of power demand.
* **OWON XDM1000 series SCPI client**: This project is not yet publicly available but will be released as FOSS with MIT licence eventually. This contains a fork of [klasyc](https://github.com/klasyc)'s excellent [ScpiNet](https://github.com/klasyc/ScpiNet). This package can be used to control my OWON XDM1241 and read measurements (in this project I use it to read a temperature probe on the <abbr title="Device under Test">DuT</abbr>).
* [Custom ambient sensor](https://github.com/RobThree/TemperatureDisplay): this was a simple hardware + software one-off that combines a Wemos D1 Mini with a GXHT30 temperature and humidity sensor and a 0.96" SSD1306 OLED display to do ambient temperature readings. This [monstrosity](https://raw.githubusercontent.com/RobThree/TemperatureDisplay/refs/heads/main/example.jpg) outputs the temperature to the serial port and offers an HTTP endpoint as well so that I could easily integrate ambient temperature readings in my test runner.
* **Test runner**: This is a very specific and unique mudball of a project that integrates all of the above and does the actual testing. Code for this project is not likely to be released. Because.

## Atribution

Icon by [Payungkead](https://www.freepik.com/icon/usb_1664704)