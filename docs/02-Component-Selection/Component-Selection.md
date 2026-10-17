---
title: Component Selection
---

## Component Selections

**1.Temperature / Heat Sensors x2**

1. TMP36GT9Z Analog Temperature Sensor
<img width="200" height="200" alt="505~T-3-1~N,T~3_sml(200x200)" src="https://github.com/user-attachments/assets/e6525c47-a084-449c-8da8-58c3f7febbc1" />
    * $1.85/each
    * [link to product](https://www.digikey.com/en/products/detail/analog-devices-inc/TMP36GT9Z/820404)

    | Pros                                      | Cons                                                             |
    | ----------------------------------------- | ---------------------------------------------------------------- |
    | Active RoHS-compliant                     | Most expensive                                                   |
    | Outputs 10 mV/°C analog voltage (500 mV at 0°C) that sums in the AD824 op-amp                | Accuracy is wider than the others
   |TO-92-3 through-hole package operating from 2.7V to 5.5V|  |                                      |

2. Microchip MCP9700A-E/TO Linear Active Thermistor IC
<img width="200" height="200" alt="150~C04-101~TO,ZB~3_sml" src="https://github.com/user-attachments/assets/9a0344cd-94f4-4c26-b300-52b64391e9c2" />
    * $0.61/each
    * [Link to product](https://www.digikey.com/en/products/detail/microchip-technology/MCP9700A-E-TO/1212508)

    | Pros                                                              | Cons                |
    | ----------------------------------------------------------------- | ------------------- |
    | inexpensive and Most units available | wider maximum error band at ±2°C from 0°C to +70°C, up to ±4°C  |
    | 10 mV/°C linear slope and 500 mV offset at 0°C in a through-hole TO-92-3 package  |Output impedance requires a high-impedance buffer or op-amp input ||
   |6 µA typical operating current prevents self-heating |

   3. Vishay NTCLE100E3103GB0 10kΩ NTC Thermistor
  <img width="200" height="200" alt="NTCLE100E3103GB0_sml" src="https://github.com/user-attachments/assets/73a9cf71-761a-42d2-9417-1f93f442b2f7" />
    * $0.95/each
    * [Link to product](https://www.digikey.com/en/products/detail/vishay-beyschlag-draloric-bc-components/NTCLE100E3103GB0/773869)

    | Pros                                                              | Cons                |
    | ----------------------------------------------------------------- | ------------------- |
    | passive two-lead radial through-hole                               |resistance curve is non-linear      |
    | rapid temperature change detection       | suffers from continuous current self-heating |
    | Compact |                     |

**Choice:** Option 1: Analog Devices TMP36GT9Z Analog Temperature Sensor
**Rationale:** the TMP36GT9Z is calibrated at a 10 mV/°C linear voltage in an easy-to-solder TO-92-3 package with no external calibration components required


**2. Ambient Light Sensor**

1. Advanced Photonix PDV-P8103 CdS Photoresistor
<img width="200" height="200" alt="MFG_PDV-P8103_sml(200x200)" src="https://github.com/user-attachments/assets/06c4fe64-f0c3-4da0-a85a-9c3cec274f08" />
    * $0.72/each
    * [link to product](https://www.digikey.com/en/products/detail/advanced-photonix/PDV-P8103/480610)

    | Pros                                      | Cons                                                             |
    | ----------------------------------------- | ---------------------------------------------------------------- |
    | easy to solder                               | Slower response time |
    | communicates with ADC pin using a pull-down resistor          | Contains cadmium sulfide     |
    | Spectral response peaks at 520 nm |

2. Vishay TEPT4400 Ambient Light Phototransistor
<img width="200" height="200" alt="VISHAY^SEMICONDUCTORS-TEPT4400_sml(200x200)" src="https://github.com/user-attachments/assets/09c0ceac-12de-4fa4-a260-7de4ffd32034" />
    * $0.50/each
    * [Link to product](https://www.digikey.com/en/products/detail/vishay-semiconductor-opto-division/TEPT4400/1681191)

    | Pros                                                              | Cons                |
    | ----------------------------------------------------------------- | ------------------- |
    | Inexpensive,and RoHS-compliant through-hole | leads require correct orientation on the PCB|
    | photocurrent output relative to ambient illuminance | more directional than a flat photoresistor |
    | microsecond switching response |                     |

   3. Everlight ALS-PT19-315C/L177/TR8 SMD Light Sensor
<img width="200" height="200" alt="ALS-PT19_sml" src="https://github.com/user-attachments/assets/af60b5c8-5484-4bf3-94a4-8a78031cb5c2" />
    * $0.37/each
    * [Link to product](https://www.digikey.com/en/products/detail/everlight-electronics-co-ltd/ALS-PT19-315C-L177-TR8/2675735)

    | Pros                                                              | Cons                |
    | ----------------------------------------------------------------- | ------------------- |
    | Very inexpensive                                         | very difficult to hand-solder  |
    | Optical filter matches human eye spectral response (630 nm peak) Slow shipping speed |
    | Operates up to 5.5V |                     |

**Choice:** 1: Advanced Photonix PDV-P8103

**Rationale:** measuring light levels , a radial through-hole sensor makes it easy to assemble and solder. It works off our 5V rail using a series resistor to go straight into the microcontroller's ADC pin.

**3. Humidity Sensor**

1. Adafruit 5183 (DHT20 / AHT20 4-Pin SIP Humidity Sensor)
<img width="200" height="200" alt="MFG_1528_5183_sml" src="https://github.com/user-attachments/assets/74097f18-cced-4794-9b0b-f97c83c07848" />
    * $4.50/each
    * [link to product](https://www.digikey.com/en/products/detail/adafruit-industries-llc/5183/15204087)

    | Pros                                      | Cons                                                             |
    | ----------------------------------------- | ---------------------------------------------------------------- |
    | Actively produced                            | Larger plastic housing |
    | Standard 4-pin 2.54 mm pitch through-hole footprint  | Requires I2C driver code in firmware |
    | Operates from 2.5V to 5.5V |

2. Sensirion SHT31-ARP-B Analog Humidity & Temp Sensor
<img width="200" height="200" alt="1649~8DFN-1-2 5X2 5~~8_sml(200x200)" src="https://github.com/user-attachments/assets/3ab75e1e-829c-47e2-91f5-f64d23d51ef1" />
    * $5.00/each
    * [Link to product](https://www.digikey.com/en/products/detail/sensirion-ag/SHT31-ARP-B/5872251)

    | Pros                                                              | Cons                |
    | ----------------------------------------------------------------- | ------------------- |
    | connects directly to a microcontroller ADC pin   | Sensitive to flux residue      |
    | High ±2% RH accuracy | very difficult to hand-solder |

   3. Honeywell HIH6130-021-001 8-SOIC Humidity Sensor IC
<img width="200" height="200" alt="HIH-6130-021-001_sml(200x200)" src="https://github.com/user-attachments/assets/c247c208-7828-45e1-89e7-35273fcdad66" />
    * $29.07/each
    * [Link to product](https://www.digikey.com/en/products/detail/honeywell-sensing-and-productivity-solutions/HIH6130-021-001/2704701)

    | Pros                                                              | Cons                |
    | ----------------------------------------------------------------- | ------------------- |
    | Very easy to hand-solder                                          | Most expensive      |
    | Operates directly on 5V supply rail                                 | accuracy is slightly wider than Sensirion |
    | Outputs factory-calibrated digital|
**Choice:** 3.Honeywell HIH6130-021-001 8-SOIC Humidity Sensor IC

**Rationale:** the 4-pin SIP DHT20 mounts into through-hole pads on our board, runsoff our 5V rail, and provides calibrated digital humidity readings

**4. Operational Amplifier** 

1. Analog Devices AD824ARZ-14 Quad JFET Op-Amp
<img width="200" height="200" alt="505~R-14~R,S~14_sml" src="https://github.com/user-attachments/assets/82c4233a-66a6-4430-ad72-268e262037ff" />
    * $20.24/each
    * [link to product](http://www.digikey.com/product-detail/en/ECS-40.3-S-5PX-TR/XC1259TR-ND/827366)

    | Pros                                      | Cons                                                             |
    | ----------------------------------------- | ---------------------------------------------------------------- |
    | Operates on a single 5V supply | Very expensive per unit |
    | JFET inputs draw ultra-low bias current   | four op-amp channels, we only need 2  |
    | 14-SOIC package |

2. Microchip MCP6004-I/SL Quad CMOS Op-Amp
<img width="200" height="200" alt="150~C04-065~OD,-SL~14_sml" src="https://github.com/user-attachments/assets/6cdaac2c-9736-4b5d-bed9-3718815a4828" />
    * $0.44/each but need to buy 57 minimum
    * [Link to product](http://www.digikey.com/product-detail/en/636L3I001M84320/CTX936TR-ND/2292940)

    | Pros                                                              | Cons                |
    | ----------------------------------------------------------------- | ------------------- |
    | Very inexpensive                                            | need to buy 57 minumum|
    | Rail-to-rail input and output                                 |  Lower bandwidth and slew rate |
    | Low 1 pA input bias current|

   3. Texas Instruments LM324N Quad BJT Op-Amp
<img width="200" height="200" alt="Mfg_296~4040049~N~14_sml(200x200)" src="https://github.com/user-attachments/assets/2fb9d5ff-e20e-4952-b1ba-fb8b3f2dc786" />
    * $.58/each
    * [Link to product](http://www.digikey.com/product-detail/en/636L3I001M84320/CTX936TR-ND/2292940)

    | Pros                                                              | Cons                |
    | ----------------------------------------------------------------- | ------------------- |
    | Very inexpensive                                            | Output is not rail-to-rail      |
    |Through-hole 14-DIP package is simple to solder | Higher BJT input bias |
    | Wide 3V to 32V supply voltage rating |                     |

**Choice:** Option 3: Texas Instruments LM324N Quad BJT Op-Amp

**Rationale:** inexpenseive, widly avalible, and easy to solder with through hole
