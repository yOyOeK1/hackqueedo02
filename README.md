# hackqueedo 02

**status of project** - start is in progress

---

Alternative solution to use torqueedo outboard when you have only bear 3f motor.

In this cane it is more using body but electronic section is out and different is in ...

## situation

* I got a trased torqueedo t503 trave. Current status of it controller release the smoke. So I have body / brackets column motor in motor unit planetary gear and org. motor. Original controller lets say part of it escape. So remaining out. So in under water section is now only motor and planetary gear box. Cables are connected directly to the motor and going up. I swap them to have 3x same gauge of cable

* battery only case and cells this is rearrange ...

* controller / tiller case and 360 magnetic hall sensor

### plan is to have

- [ ] **main motor unit** - with new controller [RC HELI 80A 3F ESC] on it permanently mounted. Plug (original plug tiller to battery) and wires with two alligator clips (+), (-) So plug to talk to motor is now next to controller not on the battery box
- [ ] **battery box** - with cells and cables hot out all the time
  - [x] **cells 4s10p** so not 12 not 24 :P 
  - [x] **plug** - original battery to motor. Power connectors are + and - in case to pack. Signal wires are use to put out cells cell0+, cell1+, cell2+ so there is a way to ballance it from outside 
  - [x] posts (+) and (-) - scrues connected all the time to pack    
- [ ] **tiller** [with custom 4 pin 2.54 pich] - to motor unit / controller
- [x] **charging system** in my case will be done by RC model proglamoble / smart charger and original batery to motor wire / plug with option of ballancing cells


## project structure

```bash
tree .
.
├── LICENSE
├── README.md
├── src                          # reference files
│   ├── arduino Pinout- nano.png
│   ├── AS5045_DS000101_2-00.pdf
│   └── oled_ssd1306_i2c.jpg
└── torqueedo02                   # arduino src 
    └── torqueedo02.ino           # not working now !
```


## hardware use

- aligator clips - starter clamps ?
- arduino nano
- dc to dc back converter
- oled SSD1306 128x32 i2c
  
  ![](./src/oled_ssd1306_i2c.jpg)
- resistors to make voltage divider (for battery voltage ADC)
- rc helicopter brush-less controller [RC HELI 80A 3F ESC] can by any 
- original parts:
  - plug motor battery
  - wire motor battery
  - tiller box
  - tiller `AS5045 360` magneto sensor [docs - pdf](./src/AS5045_DS000101_2-00.pdf)
  - wires from tiller to battery
  - battery tiller plug


## pins on uno

![arduino nano pinout](./src/arduino%20Pinout-%20nano.png)

- **A0** as INPUT to `ADC` to read voltage on battery

- **8, 9** as RX TX to `rs 485` if you use it to talk to still `working original ecu` in your unit then you need converter rs485

- **2, 3, 4** as CS, CLK, D0 to talk to `AS5045` 



## TODO

- main motor unit
- battery box
- tiller
  - rewire old
  - new firmware for ppm on torquedo can protocal 
- tests :)

---

If you see that this makes sense [ send me a ☕ ](https://ko-fi.com/B0B0DFYGS) | [Master repository](https://github.com/yOyOeK1/oiyshTerminal) | [About SvOiysh](https://www.youtube.com/@svoiysh)
