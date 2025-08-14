---
title: Hardware
---

# Hardware

This is the list of the hardware that is present in my smart home.

이 페이지의 일부 링크는 제휴 링크입니다. 제휴 링크를 통해 무언가를 구매하면 제가 소량의 협찬을 받을 수 있으나, 여러분께는 추가 비용이 들지 않습니다.


## Table of Content

[Home Assistant](##home-assistant)
[Hubs](##hubs) |
[Climate](##climate) |
[Windows/Curtains](##windowscurtains) |
[Lights](##lights) |
[Wall Switches](##wall-switches) |
[Power Plugs](##power-plugs) |
[Voice Control](##voice-control) |
[Security](##security) |
[Other Sensors](##other-sensors) |
[Media](##media) |
[Other Hardware](##other-hardware) |


## Home Assistant
Device | Quantity | Connection | HomeAssistant | Notes
:--: | :--: | :--: | :-: | :-:
![Raspberry Pi 5](images/raspberry-pi-5.png)[Raspberry Pi 5](https://www.raspberrypi.com/products/raspberry-pi-5/) | - | - | [Raspberry Pi](https://www.home-assistant.io/installation/raspberrypi/) | HAOS로 사용 중이며 PoE를 지원합니다.
![OpenKNX RasPi HAT](images/DualKNX_MicroBCU_RaspiHat.png)[OpenKNX RasPi HAT](https://github.com/OpenKNX/OpenKNX/wiki/OpenKNX-RasPi-HAT) | - | - | - | HAT
![Xinjian AX650n AI Accelerator](images/O1CN01OxHXgQ25It5nRTtiw_!!2217327727504.jpg_q50.jpg_.webp)[Xinjian AX650n AI Accelerator](https://item.taobao.com/item.htm?id=831650560883) | - | - | - | HAT

## Hubs

Device | Quantity | Connection | HomeAssistant | Notes
:--: | :--: | :--: | :-: | :-:
[AppleTV 4K 3rd](https://www.apple.com/lae/apple-tv-4k/) | 1 | LAN | [Thread](https://www.home-assistant.io/integrations/thread/) | Apple TV 4K 3세대를 메인 Thread Border Router로 사용합니다. NRF52840 동글에 연결된 OTBR 애드온을 백업 Thread Border Router로 사용합니다.
[Amazon Fire 10 HD(2019)](https://www.amazon.com/Fire-HD-10/dp/B07KD58DQS) | 1 | Wi-Fi | [Fully Kiosk Browser](https://www.home-assistant.io/integrations/fully_kiosk/) | Core 2024.7.1. 버전부터 월패드로 사용하고 있는 태블릿입니다.

## Climate

Device | Quantity | Connection | HomeAssistant | Notes
:--: | :--: | :--: | :-: | :-:
[LG 시스템 에어컨](https://www.lge.co.kr/kr/business/product/cooling/single-multi-v-s-living) | 1 | Wi-Fi | [LG ThinQ](https://www.home-assistant.io/integrations/lg_thinq/) | LG 시스템 에어컨입니다.
[LG 코드제로 오브제컬렉션 R5](https://www.lge.co.kr/vacuum-cleaners/r585wka1) | 1 | Wi-Fi | [LG ThinQ](https://www.home-assistant.io/integrations/lg_thinq/) | LG 로봇 청소기 입니다.

## Windows/Curtains

블라인드를 기존에 사용하다가 커튼으로 옮긴 후로 아직 커튼 모터를 구매하지 않았습니다.
Device | Quantity | Connection | HomeAssistant | Notes
:--: | :--: | :--: | :-: | :-:
. | - | - | - | -

## Lights

Device | Quantity | Connection | HomeAssistant | Notes
:--: | :--: | :--: | :-: | :-:
[Nanoleaf Essentials Matter E27](https://nanoleaf.me/en-KR/products/essentials/bulbs/?category=A60-E27&standard=matter&size=each) | 0 | Thread | [Matter (BETA)](https://www.home-assistant.io/integrations/matter/) | 최신 펌웨어로 사용하면 추천할 만 합니다. 가격이 저렴합니다.
[Nanoleaf Essentials Matter GU10](https://nanoleaf.me/en-KR/products/essentials/bulbs/?category=GU10&standard=matter&size=each) | 1 | Thread | [Matter (BETA)](https://www.home-assistant.io/integrations/matter/) | 위와 동일
[Auxmer LED CCT Strip](https://www.aliexpress.com/item/1005005645881199.html) | 1 | - | - | 38.4W/m(240 LEDs). 매우 바람직하지만 아래 것보다 4배 더 비쌉니다. 나는 이 스트립을 주 조명에만 사용합니다.
[COXO LED CCT Strip](https://www.aliexpress.com/item/1005005791196110.html) | 1 | - | - | 14W/m(608 LEDs). 성능적으로는 Auxmer가 더 낫다고 생각하지만 가격이 매우 차이납니다. 하지만 주변 조명에는 좋습니다.

## Wall Switches

Device | Quantity | Connection | HomeAssistant | Notes
:--: | :--: | :--: | :-: | :-:
[SPEEL 터치넷 T2R 일괄소등+가스차단 스위치](http://speel.co.kr/project/%ec%9d%bc%ea%b4%84%ec%86%8c%eb%93%b1%ea%b0%80%ec%8a%a4%ec%b0%a8%eb%8b%a8-2/) | 1 | - |ESPHome | 일괄소등 + 가스차단 기능. 하지만 가스는 하이라이트고 일괄소등은 전기를 끊는지라 사용하지 않습니다.
[Aqara H2 US](https://www.aqara.com/en/product/light-switch-h2-us/) | 1 | Thread | [Matter (BETA)](https://www.home-assistant.io/integrations/matter/) | 집에 있는 유일한 물리 스위치입니다. 각각 화장실, 샤워부스, 환풍기를 제어합니다. 마지막 버튼은 일괄 소등 scene switch로 사용 중입니다.

## Power Plugs

현재는 스마트 플러그 류를 사용하지 않습니다.
Device | Quantity | Connection | HomeAssistant | Notes
:--: | :--: | :--: | :-: | :-:

## Voice Control
기존에는 [OpenAI Conversation](https://www.home-assistant.io/integrations/openai_conversation/)에서 GPT-4o 모델을 사용했지만, 현재는 [Google Generative AI](https://www.home-assistant.io/integrations/google_generative_ai_conversation/)에서 Gemini 2.0 Flash 모델을 사용하고 있습니다. 사용하는 이유는 무료여서입니다.

Device | Quantity | Connection | HomeAssistant | Notes
:--: | :--: | :--: | :-: | :-:
[Home Assistant Voice Preview Edition](https://www.home-assistant.io/voice-pe/) | 2 | Wi-Fi | [ESPHome](https://www.home-assistant.io/integrations/esphome/) | Home Assistant의 공식 하드웨어입니다. 기능적으로는 ReSpeaker Lite와 같지만 더 아름답습니다.

## Security
물체 감지를 위해 Doods 애드온을 사용하고 있습니다. 10개 이상의 FHD 스트림을 처리하고 움직임을 감지하며 물체를 인식할 수 있습니다.

Device | Quantity | Connection | HomeAssistant | Notes
:--: | :--: | :--: | :-: | :-:
[TP-link Tapo C110](https://www.tp-link.com/kr/home-networking/cloud-camera/tapo-c110/) | 1 | Wi-Fi | [Frigate Home Assistant Integration](https://github.com/blakeblackshear/frigate-hass-integration) | -
[Eve Motion](https://www.evehome.com/en/eve-motion) | 1 | Thread | [Matter (BETA)](https://www.home-assistant.io/integrations/matter/) | 잘 작동하지만 가격은 쉽게 받아 들일 수 없는 것 같습니다.
[Aqara Door and Windows Sensor P2](https://www.aqara.com/en/product/door-and-window-sensor-p2/) | 2 | Thread |[Matter (BETA)](https://www.home-assistant.io/integrations/matter/) | 훌륭하지만 이전 Zigbee 모델보다 약간 비쌉니다. 배터리 규격이 특이합니다.

## Other Sensors

Device | Quantity | Connection | HomeAssistant | Notes
:--: | :--: | :--: | :-: | :-:
[Netatomo Home Coach](https://shop.netatmo.com/en-eu/aircare/home-coach) | 1 | Wi-Fi | [Netatmo](https://www.home-assistant.io/integrations/netatmo/) | 클라우드 방식. 공기 질을 세부적으로 측정하지 않는 것이 아쉽습니다.

## Media
음악 스트리밍을 위해 Music Assistant와 Apple Music을 사용합니다.

Device | Quantity | Connection | HomeAssistant | Notes
:--: | :--: | :--: | :-: | :-:
[Apple TV 4K 3rd](https://www.apple.com/lae/apple-tv-4k/) | 1 | LAN | [Apple TV](https://www.home-assistant.io/integrations/apple_tv) | 3rd 버전을 기본 미디어 스테이션으로 사용합니다.
[Home Assistant Voice Preview Edition](https://www.home-assistant.io/voice-pe/) | 2 | Wi-Fi | [ESPHome](https://www.home-assistant.io/integrations/esphome/) | Music Assistant streamer로 사용합니다.
[Edifier MR3](https://www.edifier.com/int/global/p/studio-monitors/mr3) | 1 | - | [ESPHome](https://www.home-assistant.io/integrations/esphome/) | 위 Voice PE에 연결됩니다.
[JBL Flip 4](https://kr.jbl.com/JBL+Flip+4.html) | 1 | - | [ESPHome]((https://www.home-assistant.io/integrations/esphome/)) | Voice PE에 연결됩니다. 방수 기능이 있어 화장실 스피커로 사용합니다.

## Other Hardware

### Network Devices
Ubiquiti 장비를 사용합니다. 그들은 확실히 엔터프라이즈급 장치는 아니지만 내 홈랩에서 작업을 수행합니다. 그건 그렇고, 예쁩니다.

Device | Quantity | Connection | HomeAssistant | Notes
:--: | :--: | :--: | :-: | :-:
[Unifi Gateway Lite](https://techspecs.ui.com/unifi/cloud-keys-gateways/uxg-lite) | 1 | LAN | [Unifi Network](https://www.home-assistant.io/integrations/unifi/) | 작고 제 역할을 합니다. 혼자 사는 방이기에 이 이상은 필요하지 않습니다.
[UniFi Switch 8 60W](https://techspecs.ui.com/unifi/wifi/uap-iw-hd) | 1 | LAN | [Unifi Network](https://www.home-assistant.io/integrations/unifi/) | 구세대 PoE 스위치입니다.
![](images/unifi_ap_lite.png)[UniFi AC lite](https://techspecs.ui.com/unifi/wifi/uap-ac-lite) | 1 | LAN | [Unifi Network](https://www.home-assistant.io/integrations/unifi/) | 역시 혼자 사는 방에 충분합니다.
[Unifi Gateway Pro](https://techspecs.ui.com/unifi/cloud-keys-gateways/uxg-pro) | 1 | LAN | [Unifi Network](https://www.home-assistant.io/integrations/unifi/) | 이베이에서 200 달러에 구입했습니다. 이것은 나로부터 10km 이상 떨어진 NAS의 라우터입니다. Site-to-Site VPN을 사용하여 홈 네트워크에서 연결합니다.
[Cloudkey+](https://techspecs.ui.com/unifi/cloud-keys-gateways/uck-g2-plus) | 1 | LAN | [Unifi Network](https://www.home-assistant.io/integrations/unifi/) | Cloudkey를 사용한 이유는 완전히 로컬을 유지하고 다른 사이트에 원격으로 액세스할 수 있는 기능을 원했기 때문입니다.

### Appliances

Device | Quantity | Connection | HomeAssistant | Notes
:--: | :--: | :--: | :-: | :-:
![](images/wall-pad.jpg)[HNF-I2101](https://www.hyundaiht.co.kr/product/smart_home/view.php?returnURL=%2Fproduct%2Fsmart_home%2Flist.php&idx=22) | 1 | Wi-Fi | [ESPHome](https://www.home-assistant.io/integrations/esphome/) | 현대통신 월패드. 
[삼성 BESPOKE 전자레인지 23L(그릴 프라이)](https://www.samsung.com/sec/micro-wave-ovens/microwave-oven-grill-MG23T5018CC-d2c/MG23T5018CP/) | 1 | Wi-Fi | [Smartthings](https://www.home-assistant.io/integrations/smartthings/) | 남은 시간을 확인할 수 있습니다.
[Brewista Artisan Electric Gooseneck Kettle](https://brewista.co/products/artisan-electric-gooseneck-kettle) | 1 | - |- | 스마트 기기가 아니지만 예쁩니다. 나는 커피를 추출할 때 이것을 사용합니다.
[ITOP 03 Coffee Grinder](https://ko.aliexpress.com/item/1005006170009173.html) | 1 | - | - | Varia VS3 그라인더의 중국 클론입니다.

### Other Devices

Device | Quantity | Connection | HomeAssistant | Notes
:--: | :--: | :--: | :-: | :-:
[Oral-B smart series 6000] | 1 | Bluetooth | [Oral-B](https://www.home-assistant.io/integrations/oralb/) | 전동칫솔. 양치한 시각을 모니터링할 수 있습니다.
