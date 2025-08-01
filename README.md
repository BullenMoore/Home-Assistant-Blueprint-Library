# Home Assistant Blueprint Library (HABL)

A curated collection of Home Assistant ZHA blueprints, organized by **manufacturer** and **device model**.

- [Introduction](#introduction)
- [Who Is This For?](#who-is-this-for)
- [Finding the Right Blueprint](#finding-the-right-blueprint)
- [How to Use](#how-to-use)
- [Authors](#authors)
  
---

## Introduction

This project's goal is to feature a vast collection of blueprints for as many devices by as many manufacturers as possible, making finding fitting and flexible blueprints easier. The goal is also to feature different types of blueprints for the same device, for different user's skill level.
Hopefully this can be an alternative way of finding blueprints that fit the device the user want to use. 

---

## Who Is This For?

This project is made for two types of users.
- **Beginners** who want plug-and-play solutions for their devices
- **Advanced users** who want to contribute with their own blueprints, do custom blueprints for others or find more complex ones.

---

## Finding the Right Blueprint

For the library to have a functional structure it is split up by the model shown below: 

```bash
manufacturer/
├── IKEA/
│   └── SOMRIG shortcut button/
│       └── SOMRIG shortcut button (unlocked).yaml
├── PhilipsHUE/
│   ├── RDM002/
│   │   └── Philips Tap Dial Switch (lights only).yaml
│   └── RWL022/
│       ├── Philips Dim Switch v2 (native).yaml
│       └── Philips Dim Switch v2 (unlocked).yaml
...
```

This is to make finding something suitable for your device easier. Just follow your device's manufacturer and model to find blueprints that suit your device.

If you don't know the manufacturer or model name of your device, you can find it by going into your Home Assistant and go to **Settings > Devices & services > Zigbee Home Automation integration** and click the device you want a blueprint for. The manufacturer and model is displayed under "Device info".

<img width="421" alt="MM-github" src="https://github.com/user-attachments/assets/e1ed0545-afdd-45ab-ac53-8adf1178aaab" />

Note: Some devices might not have the name you'd expect.
- IKEA shows as expected, *"IKEA of Sweden"*
- Philips HUE shows as unexpected, *"Signify Netherlands B.V.".*

If unsure, check the physical device as it might give a hint to the manufacturer/model name.

<img width="700" alt="alternative-manufacturer" src="https://github.com/user-attachments/assets/201065ae-2e6d-4e43-ab08-76b7f2622c6d" />

### Native vs unlocked vs something else

All blueprints in a model folder start with the device name, followed by a short description in parentheses. Like in the [Philips Tap Dial Switch (lights only).yaml](https://github.com/BullenMoore/Home-Assistant-Blueprint-Library/tree/main/manufacturer/PhilipsHUE/RDM002)), where the only allowed entities are lights.

Other blueprints, feature the descriptors *unlocked* or *native*. These are special blueprints that hopefully will provide flexibility and/or an easy way of using certain devices.

- **Unlocked** blueprints are made with maximum freedom. These blueprints essentially just give each button (often both tap and hold) a building block so that the user can do whatever with a certain action. Some people might not want switches for lights only, so these blueprints offer a greater flexibility for more skilled users.

- **Native** blueprints are a little stricter. These types of blueprints aim to make blueprints that are as close to the manufacturers intended use-cases. For example, the Philips HUE RWL002 (or Philips Dim Switch v2) use case in its native app, is made for only a certain light or all lights in a certain room, where the dim buttons only dim the light(s). The fourth HUE buttons change the scene of the light(s). A native blueprint then aims to do the same but outside of its native app. An unlocked blueprint for this device would simply open all buttons to whatever service the user associates with it.

The goal is to provide both user-friendly and advanced-user options.

---

## How to Use

1. Find a blueprint you're interested in.
2. Copy the raw YAML URL.
3. In Home Assistant, go to **Settings > Automations & Scenes > Blueprints > Import Blueprint**.
4. Paste the URL and click **Preview**.
5. Enter the fields in the blueprint and customize to your desire.

---

## Authors

Made with ❤️ by Tim Svensson and the [Contributers](CONTRIBUTERS.md).

Speical thanks to Jeremy Fisher ([apollo1220](https://community.home-assistant.io/u/apollo1220)) for his Philips Hue Tap Dial Switch ZHA Blueprint that inspired this entire project.

Contributions welcome! See [`CONTRIBUTING.md`](CONTRIBUTING.md) for more info.
