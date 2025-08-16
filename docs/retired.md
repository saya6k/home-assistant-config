---
title: Retired
---

# 🗃️ Retired

This section documents the hardware and software that I have retired from my smart home setup. Each item listed here has been used for more than a month, providing insights into why they were eventually retired.

## 🛠️ Retired Hardware

| Device | Connection | Home Assistant | Notes |
|:------:|:----------:|:--------------:|:-----:|
| Nanoleaf Essentials Matter Lightstrip | [Matter (BETA)](https://www.home-assistant.io/integrations/matter/) | Surprisingly, I found this device preferable to bulbs due to its stability and fewer connectivity issues. However, I switched to a Matter over Thread CCT Driver, leading to its retirement. |
| Amazon Fire 10 HD (2017) | [Fully Kiosk Browser](https://www.home-assistant.io/integrations/fully_kiosk/) | This was my main 10-inch kitchen kiosk for two years until it suddenly lost power and never recovered. Rest in peace. |
| Sonos Era 100 | [Sonos](https://www.home-assistant.io/integrations/sonos/) | I used Sonos for multi-room music but eventually sold them at a flea market. They are excellent devices, though. |
| Sonos Symfonisk Lamp Gen 2 | [Sonos](https://www.home-assistant.io/integrations/sonos/) | - |
| Sonos Symfonisk Gen 1 | [Sonos](https://www.home-assistant.io/integrations/sonos/) | - |
| [Onju Voice](https://github.com/justLV/onju-voice) | [ESPHome](https://www.home-assistant.io/integrations/esphome/) | A beautiful device, but I couldn't tolerate the false positives from the microwake word. |
| Navien NR-40D | [navien_boiler](https://github.com/jjang750/navien_boiler) | A smart thermostat from the manufacturer that performs poorly with Home Assistant. I do not recommend purchasing this. |
| Lenovo Thinksmart View | [Fully Kiosk Browser](https://www.home-assistant.io/integrations/fully_kiosk/) | [Is this the perfect standalone tablet for HA?](https://community.home-assistant.io/t/is-this-the-perfect-standalone-tablet-for-ha/658422/302) |
| [SONOFF Zigbee 3.0 USB Dongle Plus](https://sonoff.tech/product/gateway-and-sensors/sonoff-zigbee-3-0-usb-dongle-plus-e/) | [Zigbee Home Automation](https://www.home-assistant.io/integrations/zha/) | I still use this dongle because of irreplaceable Zigbee devices. |
| [Zemismart Matter over Thread Built-in Battery Blind Motor (20/28mm)](https://www.zemismart.com/products/mt15b) | [Matter (BETA)](https://www.home-assistant.io/integrations/matter/) | In Korea, 28mm tube blinds are commonly used. |
| [Neo Coolcam Zigbee 3.0 Power Plug](https://www.aliexpress.com/item/1005005486450704.html) | [Zigbee Home Automation](https://www.home-assistant.io/integrations/zha) | Connects via Z2M or ZHA. Highly reliable and can monitor power usage up to 16A. Very affordable with a slim profile, available for under $10 on Aliexpress. Recommended if you use Zigbee. |
| [Eve Energy](https://www.evehome.com/en/eve-energy) | [Matter (BETA)](https://www.home-assistant.io/integrations/matter/) | Supports up to 11A. Currently not recommended due to its large size, which can physically interfere with nearby plugs. |
| [HejHome Smart Plug Air](https://hej.life/product/detail.html?product_no=212&cate_no=42&display_group=1) | [Matter (BETA)](https://www.home-assistant.io/integrations/matter/) | Supports up to 10A. Very slim and supports power measurement, but its Matter-over-WiFi feature is a drawback. |
| [Aqara Door and Windows Sensor P2](https://www.aqara.com/en/product/door-and-window-sensor-p2/) | [Matter (BETA)](https://www.home-assistant.io/integrations/matter/) | Excellent but slightly more expensive than the previous Zigbee model. The battery specification is unique. |
| [Elfin EW11](http://www.hi-flying.com/elfin-ew10-elfin-ew11) | [HomeAssistant Addon for Hillstate (Hyundai HT Wallpad + RS-485)](https://github.com/YOGYUI/homeassistant-addons/tree/main/homenet-hillstate) | An RS485 to WIFI dongle that connects the installed wall pad (HNF-I2101) with HA. |
| [Amazon Fire 10 HD (2019)](https://www.amazon.com/Fire-HD-10/dp/B07KD58DQS) | [Fully Kiosk Browser](https://www.home-assistant.io/integrations/fully_kiosk/) | I no longer use tablets for wall pads. |
| [Brewista Artisan Electric Gooseneck Kettle](https://brewista.co/products/artisan-electric-gooseneck-kettle) | - | Not a smart device, but aesthetically pleasing. I use it for brewing coffee. |
| [ITOP 03 Coffee Grinder](https://ko.aliexpress.com/item/1005006170009173.html) | - | A Chinese clone of the Varia VS3 grinder. |

## 💾 Retired Software

| Software | Home Assistant Integration | Notes |
|:--------:|:--------------------------:|:-----:|
| browser_mod 2 | [browser_mod 2](https://github.com/thomasloven/hass-browser_mod) | I now use Bubble Card for pop-up features. |
| InfluxDB | [InfluxDB](https://www.home-assistant.io/integrations/influxdb/) | I switched to TimescaleDB and LTSS custom components. |
| Battery Notes | [Battery Notes for Home Assistant](https://github.com/andrew-codechimp/HA-Battery-Notes) | It's annoying having so many entities about when I replaced my battery, etc. |
| JWT Cookie | [JWT Cookie](https://github.com/BigBoot/hass-jwt_cookie) | - |
