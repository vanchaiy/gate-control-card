# 🚪 Gate Control Card

A custom Lovelace card for Home Assistant that provides a visually immersive and intuitive interface for controlling smart gates. Designed with realism, responsiveness, and customization in mind—no branding, just pure user experience.

## 🚀If you need ready-to-use Hardware
Buy now -> https://github.com/vanchaiy/smart-gate-module


## ✨ Features

- 🖼️ **Realistic gate status visuals** — Wide-perspective images with grass, road, and gate elements.
- 🎞️ **Live stream support** — Refreshes every 15 seconds with fallback image logic.
- 🧼 **Minimalist design** — No logos or branding; clean and user-focused.
- 🎮 **Interactive controls** — OPEN, STOP, and CLOSE buttons with ripple animation and status feedback.
- ⚙️ **Flexible configuration** — Customize icons, labels, and image paths via YAML.
- 🧠 **Smart entity handling** — Buttons auto-disable if entities are unavailable.

## 📸 Sample Screenshots

Located in the `screen sample` folder:

![Gate Screen](./screen%20sample/Screen_Recording_20251017_210023_Chrome.gif)
![Gate Screen](./screen%20sample/Screen_Recording_20251017_205921_Chrome.gif)


## 🛠️ Installation

### Manual

1. Download `gate-control-card.js` from the `dist` folder.
2. Place it in your Home Assistant `www` directory.
3. Add the following to your `configuration.yaml` or Lovelace resources:
4. Download and Copy the  `images ` in the image folder to  `www/image/gate `

```yaml
resources:
  - url: /local/gate-control-card.js
    type: module
```


### HACS Installation instructions for users:

1. Open HACS in Home Assistant.
2. Go to "Frontend" → Three-dot menu → "Custom repositories."
3. Enter the repo URL: https://github.com/vanchaiy/gate-control-card
4. Select the type: Dashboard.
5. Press "Add" → a card will appear in the list → Press "Install."
6. Add the resource to Lovelace:
7. Download and Copy the  `images ` in the image folder to  `www/image/gate `

```yaml
resources:
  - url: /hacsfiles/gate-control-card/gate-control-card.js
    type: module
```




🧾 Configuration Example

```yaml
type: custom:gate-control-card
status_entity: sensor.ha_sgm_2026_status
open_entity: button.ha_sgm_2026_open
close_entity: button.ha_sgm_2026_close
stop_entity: button.ha_sgm_2026_stop

#<--- Options --->

# Hide the animation to show only the buttons for use with the camera.
image_hide: ( true or false ) 

# If you want to change the animation image, you can add and edit it in the section.
image_state:
  open: ( url or local )
  closed: ( url or local )
  stop: ( url or local )
  opening: ( url or local )
  closing: ( url or local )
  offline: ( url or local )

# Edit the button text and icon
buttons:
  open:
    name: เปิด
    icon: mdi:arrow-expand-horizontal
  stop:
    name: หยุด
    icon: mdi:stop
  close:
    name: ปิด
    icon: mdi:arrow-collapse-horizontal
```




📷 Example of using with Picture entity card to pull images from your camera.

```yaml
type: grid
cards:
  - show_state: true
    show_name: true
    camera_view: auto
    fit_mode: cover
    name: Gate Status
    type: picture-entity
    image: https://demo.home-assistant.io/stub_config/bedroom.png
    camera_image: camera.c3tn_bb0839328
    entity: sensor.ha_sgm_2026_status
  - type: custom:gate-control-card
    status_entity: sensor.ha_sgm_2026_status
    open_entity: button.ha_sgm_2026_open
    close_entity: button.ha_sgm_2026_close
    stop_entity: button.ha_sgm_2026_stop
    image_hide: true
```


🔧 Options
|  |  |  | 
| status_entity |  | sensor.gate_status | 
| open_entity |  | switch.gate_open | 
| close_entity |  | switch.gate_close | 
| stop_entity |  | switch.gate_stop | 
| image_hide |  | false | 
| image_state |  |  | 
| buttons |  |  | 


📦 Version
Current version: v1.0.1
Last updated: October 2025

🧑‍💻 Developer Notes
- Written in TypeScript using LitElement.
- Uses custom-card-helpers for Home Assistant integration.
- Refreshes stream key every 15 seconds to prevent frozen images.
- Ripple animation and button styling inspired by Material Design.
- 
🙌 Credits
Created by wanchaiy
Crafted for smart home enthusiasts who value realism, responsiveness, and clean design.


## 🔎 แฮชแท็ก
- #SmartHomeThailand
- #TuyaSmartModule
- #ESP8266Automation
- #HomeAssistantTH
- #SmartGateController
- #เปิดปิดประตูอัตโนมัติ
- #ประตูบ้านอัจฉริยะ
- #ควบคุมผ่านมือถือ
- #แจ้งเตือนเข้าออกบ้าน
- #ระบบรักษาความปลอดภัยบ้าน
- #อุปกรณ์สมาร์ทโฮม
- #ขายอุปกรณ์สมาร์ทโฮม
- #สมาร์ทโฮมราคาถูก
- #SmartGateModule
- #TuyaGateSwitch
- #DIYSmartHome
- #SmartHomeMadeEasy
- #ThaiMaker
- #IoTThailand
- #บ้านอัจฉริยะ
- #ประตูรีโมต


