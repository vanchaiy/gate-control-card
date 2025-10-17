# Gate Control Card

A custom Home Assistant Lovelace card for controlling smart gates with realistic visuals and intuitive feedback. Designed for clarity, minimalism, and immersive UI experience.

## 🌟 Features

- 🖼️ **Realistic status graphics**: Wide-perspective visuals with grass, road, and gate elements for immersive feedback.
- 🎮 **Control buttons**: Open, Close, and Stop actions with smooth animations.
- 📡 **Live camera stream integration**: Supports fallback images and animated loading states for slow or unavailable streams.
- 🧼 **Clean design**: No branding or logos—just pure user-focused interface.
- ⚙️ **Fully customizable**: YAML-driven configuration for maximum flexibility.

## 📸 Sample Screenshots

Screenshots are located in the `screen sample` folder. Here's a preview:

![Gate Screen](./screen%20sample/Screen_Recording_20251017_205921_Chrome.gif)
![Gate Screen](./screen%20sample/Screen_Recording_20251017_205921_Chrome.gif)


## 🛠️ Installation

### Manual

1. Download `gate-control-card.js` from the `dist` folder.
2. Place it in your Home Assistant `www` directory.
3. Add the following to your `configuration.yaml` or Lovelace resources:

```yaml
resources:
  - url: /local/gate-control-card.js
    type: module

