# Ezlo - Switch Box
Relay switch box is an ESP32-S3 based universal relay switch box. The purpose of this product is to offer a solution that can be installed tucked away inside an electrical distribution panel (DIN rail mount) or in a basement, to be able to switch a set of dry contact relays remotely with the user interface being handled somewhere else: on a tablet/computer, Mios app for example.

**The thermostat switch box should be offered as a single SKU, with external antenna, based on the U version of the ESP32-S3 WROOM module with IPEX connector for antenna.**

## Requirements
* PCB: should be designed on a 2 layer 1.6mm thick PCB with rectangular shape.  
* Processor: ESP32-S3 WROOM U module with ipex connector.  
* Sensors: Temp/humidity GXHTC3 JLCPCB Part #C2837688.  
* Power: USB Type-C input 5V 2A rated.  
* Output: 10 x dry contact NO/NC relays via screw connector. Relays should be rated for 240VAC 10A (final product rating derated to 5A). Relays should be connected to the logic side via optocouplers.  
* Enclosure: made from flame retarding materials, rectangular shape with the possibility for direct wall mounting or to DIN rail.  
* LEDs: status LEDs for each of the outputs should be visible from the front panel of the enclosure. LEDs power rail should be FET switched, under the control of the ESP32 to be able to turn all on/off via software option.  
* External SMA antenna connected via IPEX>SMA pigtail to the ESP32 module. Antenna Part Number BWIPX1-SMA-1.13L100 LCSC# C784403. Pigtail Part Number TX2400-JKD-20 LCSC# C454911.
* Expansion: I2C (4pin 3V3, SCL, SDA, GND) and 1Wire 3pin (3V3, DATA, GND) should be exposed via screw terminal so the user can connect external sensors.  

## Additional information

Each output channel should feature 3 connections IN/NO/NC.

**USB-C Power: power supply circuit should be adequately designed and relay coil voltage/current should be adequately designed such as to avoid any brown-out happening while all relays are switched on at the same time.**

![image](https://user-images.githubusercontent.com/76909080/208593593-0c351666-3968-4b45-98d7-daa0a0f1b897.png)

### TO DO 
1. Design Schematic v1 RevA
2. Design PCB v1 RevA
3. PCB Fabrication; Order prototypes
4. Test Prototype PCB v1 RevA 
