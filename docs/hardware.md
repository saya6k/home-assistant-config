---
title: Hardware
---

# 🏠 Smart Home Hardware

Welcome to the comprehensive list of hardware in my smart home setup. Some links are affiliate links, which means I may earn a small commission at no extra cost to you if you purchase through them.

## 📚 Table of Contents

- [🏠 Home Assistant](#home-assistant)
- [🔗 Hubs](#hubs)
- [🌡️ Climate](#climate)
- [🪟 Windows/Curtains](#windowscurtains)
- [💡 Lights](#lights)
- [🔌 Wall Switches](#wall-switches)
- [🔋 Power Plugs](#power-plugs)
- [🎙️ Voice Control](#voice-control)
- [🔒 Security](#security)
- [📡 Other Sensors](#other-sensors)
- [🎵 Media](#media)
- [🛠️ Other Hardware](#other-hardware)

## 🏠 Home Assistant

|                                     Device                                     | Quantity | Connection |                               Home Assistant                               |                               Notes                                |
| :----------------------------------------------------------------------------: | :------: | :--------: | :------------------------------------------------------------------------: | :----------------------------------------------------------------: |
|     [Raspberry Pi 5](https://www.raspberrypi.com/products/raspberry-pi-5/)     |    -     |     -      |  [Raspberry Pi](https://www.home-assistant.io/installation/raspberrypi/)   | Current HAOS host (HAOS 18.4, 128GB NVMe data disk). Supports PoE. |
| [OpenKNX RasPi HAT](https://github.com/OpenKNX/OpenKNX/wiki/OpenKNX-RasPi-HAT) |    -     |     -      |                                     -                                      |                              KNX HAT                               |
|                               [Piesia AD742A]()                                |    -     |     -      | Generic x86-64(https://www.home-assistant.io/installation/generic-x86-64/) |   Intel N150 pico-itx Motherboard with 16GB RAM and PoE support    |

|

## 🔗 Hubs

|                          Device                          | Quantity | Connection |                        Home Assistant                        |                                                            Notes                                                             |
| :------------------------------------------------------: | :------: | :--------: | :----------------------------------------------------------: | :--------------------------------------------------------------------------------------------------------------------------: |
| [AppleTV 4K 3rd](https://www.apple.com/lae/apple-tv-4k/) |    1     |    LAN     | [Thread](https://www.home-assistant.io/integrations/thread/) | Used as the main Thread Border Router. The SONOFF ZBDongle-E dongle with OTBR addon serves as a backup Thread Border Router. |
|                   SinuxSoft BritzyHub                    |    1     |     -      | [Matter](https://www.home-assistant.io/integrations/matter/) |        Matter bridge that exposes the apartment's built-in ceiling lights, boiler thermostat, outlets, and gas valve.        |

## 🌡️ Climate

|                                                 Device                                                 | Quantity | Connection |                          Home Assistant                          |           Notes            |
| :----------------------------------------------------------------------------------------------------: | :------: | :--------: | :--------------------------------------------------------------: | :------------------------: |
| [LG System Air Conditioner](https://www.lge.co.kr/kr/business/product/cooling/single-multi-v-s-living) |    1     |   Wi-Fi    | [LG ThinQ](https://www.home-assistant.io/integrations/lg_thinq/) | LG system air conditioner. |

## 🪟 Windows/Curtains

|                                        Device                                         | Quantity | Connection |                        Home Assistant                        |                     Notes                      |
| :-----------------------------------------------------------------------------------: | :------: | :--------: | :----------------------------------------------------------: | :--------------------------------------------: |
| [Zemismart Matter over Thread Curtain Motor](https://www.zemismart.com/products/mt82) |    2     |   Thread   | [Matter](https://www.home-assistant.io/integrations/matter/) | Using this for Main curtain and sheer curtain. |

## 💡 Lights

|                                     Device                                     | Quantity | Connection |                        Home Assistant                        |                                                                 Notes                                                                  |
| :----------------------------------------------------------------------------: | :------: | :--------: | :----------------------------------------------------------: | :------------------------------------------------------------------------------------------------------------------------------------: |
| [Aqara LED Bulb T2 GU10](https://us.aqara.com/products/aqara-led-bulb-t2-gu10) |    1     |   Thread   | [Matter](https://www.home-assistant.io/integrations/matter/) |                                       Supports Matter over Thread and offers good light quality.                                       |
|           [IKEA KAJPLATS E14 WS globe 806lm](https://www.ikea.com/)            |    5     |   Thread   | [Matter](https://www.home-assistant.io/integrations/matter/) |                                             Tunable white. Controlled by the Flux switch.                                              |
|           [IKEA KAJPLATS E26 WS globe 1521lm](https://www.ikea.com/)           |    1     |   Thread   | [Matter](https://www.home-assistant.io/integrations/matter/) |                                                 Tunable white. Living room floor lamp.                                                 |
| [Auxmer LED CCT Strip](https://www.aliexpress.com/item/1005005645881199.html)  |    1     |     -      |                              -                               |       38.4W/m (240 LEDs). Highly desirable but four times more expensive than the one below. I use this strip for main lighting.       |
|  [COXO LED CCT Strip](https://www.aliexpress.com/item/1005005791196110.html)   |    1     |     -      |                              -                               | 14W/m (608 LEDs). While Auxmer is better in performance, the price difference is significant. However, it's good for ambient lighting. |

## 🔌 Wall Switches

|                                                                          Device                                                                           | Quantity | Connection |                         Home Assistant                         |                                                       Notes                                                       |
| :-------------------------------------------------------------------------------------------------------------------------------------------------------: | :------: | :--------: | :------------------------------------------------------------: | :---------------------------------------------------------------------------------------------------------------: |
| [SPEEL TouchNet T2R All-Off + Gas Cut-Off Switch](http://speel.co.kr/project/%ec%9d%bc%ea%b4%84%ec%86%8c%eb%93%b1%ea%b0%80%ec%8a%a4%ec%b0%a8%eb%8b%a8-2/) |    1     |     -      | [ESPHome](https://www.home-assistant.io/integrations/esphome/) | Features all-off and gas cut-off functions. However, I don't use the all-off function as it cuts off electricity. |
|                                                          HAOJAI 6-button switch (HJMT-6B0S0D-B)                                                           |    1     |     -      |  [Matter](https://www.home-assistant.io/integrations/matter/)  |                   Bedroom scene switch, mapped with the `saya6k/haojai_6button.yaml` blueprint.                   |
|                                                                 IKEA BILRESA dual button                                                                  |    1     |   Thread   |  [Matter](https://www.home-assistant.io/integrations/matter/)  |     Living room light button, mapped with the `censay/ikea-bilresa-e2489-matter-smart-button.yaml` blueprint.     |

## 🔋 Power Plugs

|                        Device                        | Quantity | Connection |                                                       Home Assistant                                                        |                   Notes                    |
| :--------------------------------------------------: | :------: | :--------: | :-------------------------------------------------------------------------------------------------------------------------: | :----------------------------------------: |
|    [Shelly EM Mini Gen4](https://www.shelly.com/)    |    2     |   Wi-Fi    | [Shelly](https://www.home-assistant.io/integrations/shelly/) + [Matter](https://www.home-assistant.io/integrations/matter/) |    Energy meter used as an inline plug.    |
| [Shelly Power Strip 4 Gen4](https://www.shelly.com/) |    1     |   Wi-Fi    | [Shelly](https://www.home-assistant.io/integrations/shelly/) + [Matter](https://www.home-assistant.io/integrations/matter/) | Four switched outlets with power metering. |
|                 IKEA GRILLPLATS Plug                 |    1     |   Thread   |                                [Matter](https://www.home-assistant.io/integrations/matter/)                                 |               Kitchen plug.                |

## 🎙️ Voice Control

The default Assist pipeline uses [OpenAI](https://www.home-assistant.io/integrations/openai_conversation/) for conversation, Home Assistant Cloud for speech-to-text, and the local Supertonic add-on for text-to-speech. See [Voice & AI](./voice-and-ai.md).

|                                     Device                                      | Quantity | Connection |                         Home Assistant                         |                                                     Notes                                                      |
| :-----------------------------------------------------------------------------: | :------: | :--------: | :------------------------------------------------------------: | :------------------------------------------------------------------------------------------------------------: |
| [Home Assistant Voice Preview Edition](https://www.home-assistant.io/voice-pe/) |    1     |   Wi-Fi    | [ESPHome](https://www.home-assistant.io/integrations/esphome/) | Official hardware from Home Assistant. Functionally similar to ReSpeaker Lite but more aesthetically pleasing. |
|                   Amazon Echo Show 5 / Echo Show 8 (1st gen)                    |    2     |   Wi-Fi    | [ESPHome](https://www.home-assistant.io/integrations/esphome/) |                              Running TECHO5 custom firmware as Assist satellites.                              |
|                          YUPP smart mirror (BM-S-21E1)                          |    1     |   Wi-Fi    | [ESPHome](https://www.home-assistant.io/integrations/esphome/) |                                               Assist satellite.                                                |

## 🔒 Security

|                          Device                           | Quantity | Connection |                        Home Assistant                        |                                        Notes                                        |
| :-------------------------------------------------------: | :------: | :--------: | :----------------------------------------------------------: | :---------------------------------------------------------------------------------: |
|    [Eve Motion](https://www.evehome.com/en/eve-motion)    |    1     |   Thread   | [Matter](https://www.home-assistant.io/integrations/matter/) |                         Works well but is quite expensive.                          |
| [IKEA MYGGBETT door/window sensor](https://www.ikea.com/) |    10    |   Thread   | [Matter](https://www.home-assistant.io/integrations/matter/) | Doors, windows, shower booth, wardrobes, shoe cabinet, fridge/freezer, drying rack. |
|                 HEIMAN Smart door sensor                  |    1     |     -      | [Matter](https://www.home-assistant.io/integrations/matter/) |                                   Bedroom window.                                   |
|                  HEIMAN Smart CO sensor                   |    1     |     -      | [Matter](https://www.home-assistant.io/integrations/matter/) |                          Bedroom carbon monoxide detector.                          |

## 📡 Other Sensors

|                        Device                        | Quantity | Connection |                            Home Assistant                            |                      Notes                      |
| :--------------------------------------------------: | :------: | :--------: | :------------------------------------------------------------------: | :---------------------------------------------: |
| [Awair Omni](https://www.getawair.com/products/omni) |    1     |   Wi-Fi    |      [Awair](https://www.home-assistant.io/integrations/awair/)      | Local Wi-Fi. It measures air quality in detail. |
|               Withings Aura Sensor V2                |    1     |   Wi-Fi    |   [Withings](https://www.home-assistant.io/integrations/withings/)   |          Under-mattress sleep sensor.           |
|        Xiaomi Mi Smart Scale / Smart Band 10         |    2     | Bluetooth  | [Xiaomi BLE](https://www.home-assistant.io/integrations/xiaomi_ble/) |              Passive BLE readings.              |

## 🎵 Media

I use Music Assistant and Apple Music for music streaming.

|                                     Device                                      | Quantity | Connection |                         Home Assistant                          |                               Notes                                |
| :-----------------------------------------------------------------------------: | :------: | :--------: | :-------------------------------------------------------------: | :----------------------------------------------------------------: |
|            [Apple TV 4K 3rd](https://www.apple.com/lae/apple-tv-4k/)            |    1     |    LAN     | [Apple TV](https://www.home-assistant.io/integrations/apple_tv) |         The 3rd version is used as the main media station.         |
| [Home Assistant Voice Preview Edition](https://www.home-assistant.io/voice-pe/) |    1     |   Wi-Fi    | [ESPHome](https://www.home-assistant.io/integrations/esphome/)  |                Used as a Music Assistant streamer.                 |
|     [Edifier MR5](https://www.edifier.com/int/global/p/studio-monitors/mr5)     |    1     |     -      | [ESPHome](https://www.home-assistant.io/integrations/esphome/)  |                  Connected to the above Voice PE.                  |
|                [JBL Flip 4](https://kr.jbl.com/JBL+Flip+4.html)                 |    1     |     -      | [ESPHome](https://www.home-assistant.io/integrations/esphome/)  | Connected to the Voice PE. Waterproof, used as a bathroom speaker. |

## 🛠️ Other Hardware

### Network Devices

I use Ubiquiti equipment. They are not exactly enterprise-grade devices, but they do the job in my home lab. Plus, they look nice.

|         Site          |                                         Device                                          | Quantity | Connection |                           Home Assistant                           | Notes                                                                                |
| :-------------------: | :-------------------------------------------------------------------------------------: | :------: | :--------: | :----------------------------------------------------------------: | :----------------------------------------------------------------------------------- |
|         Local         |                      [UniFi Gateway Fiber](https://store.ui.com/)                       |    1     |    LAN     | [Unifi Network](https://www.home-assistant.io/integrations/unifi/) | Main router, fiber line termination.                                                 |
|         Local         |             [UniFi US-8-60W](https://techspecs.ui.com/unifi/wired/us-8-60w)             |    1     |    LAN     | [Unifi Network](https://www.home-assistant.io/integrations/unifi/) | 8-port PoE switch (60W budget).                                                      |
|         Local         |          [UniFi UAP-AC-Lite](https://techspecs.ui.com/unifi/wifi/uap-ac-lite)           |    1     |    LAN     | [Unifi Network](https://www.home-assistant.io/integrations/unifi/) | Wi-Fi AP.                                                                            |
| Remote (TrueNAS site) |                   [UniFi NextGen Gateway Pro](https://store.ui.com/)                    |    1     |    LAN     | [Unifi Network](https://www.home-assistant.io/integrations/unifi/) | Router at the remote TrueNAS site (>10 km away), site-to-site VPN to the local site. |
| Remote (TrueNAS site) | [UniFi CloudKey 2 Plus](https://techspecs.ui.com/unifi/cloud-keys-gateways/uck-g2-plus) |    1     |    LAN     | [Unifi Network](https://www.home-assistant.io/integrations/unifi/) | Single controller managing both sites locally.                                       |

### Appliances

|                                                                   Device                                                                    | Quantity | Connection |                          Home Assistant                          |                    Notes                     |
| :-----------------------------------------------------------------------------------------------------------------------------------------: | :------: | :--------: | :--------------------------------------------------------------: | :------------------------------------------: |
|          [HNF-I2101](https://www.hyundaiht.co.kr/product/smart_home/view.php?returnURL=%2Fproduct%2Fsmart_home%2Flist.php&idx=22)           |    1     |   Wi-Fi    |  [ESPHome](https://www.home-assistant.io/integrations/esphome/)  |          Hyundai Telecom wall pad.           |
| [Samsung BESPOKE Microwave 23L (Grill Fry)](https://www.samsung.com/sec/micro-wave-ovens/microwave-oven-grill-MG23T5018CC-d2c/MG23T5018CP/) |    1     |   Wi-Fi    |  [LocalThings](https://github.com/mbillow/localthings) (custom)  | Local control; can check the remaining time. |
|                                           [xBloom Studio](https://xbloom.com/pages/xbloom-studio)                                           |    1     | Bluetooth  |     [xBloom](https://saya6k.github.io/hacs-xbloom/) (custom)     |            Extremely convenient.             |
|                           [LG Object Collection Dehumidifier](https://www.lge.co.kr/dehumidifiers/dq134mwec-akor)                           |    1     |   Wi-Fi    | [LG ThinQ](https://www.home-assistant.io/integrations/lg_thinq/) |       LG Dehumidifier model DQ134MWEC.       |
|                                                                  LG Styler                                                                  |    1     |   Wi-Fi    | [LG ThinQ](https://www.home-assistant.io/integrations/lg_thinq/) |            Clothing care cabinet.            |
|                                                         Dyson purifier (model 438K)                                                         |    1     |   Wi-Fi    | [Dyson Local](https://github.com/libdyson-wg/ha-dyson) (custom)  |                Local control.                |

### Other Devices

|                                              Device                                              | Quantity | Connection |                       Home Assistant                        |                      Notes                       |
| :----------------------------------------------------------------------------------------------: | :------: | :--------: | :---------------------------------------------------------: | :----------------------------------------------: |
| [Oral-B Smart Series](https://www.oral-b.co.kr/ko-kr/products/electric-toothbrushes/smart7-7000) |    1     | Bluetooth  | [Oral-B](https://www.home-assistant.io/integrations/oralb/) | Electric toothbrush. Can monitor brushing times. |
