# RikAquaShield-Pro 🛡️💧
> An ultra-low-cost, battery-optimized tank overflow and dry-run protector built for extreme field endurance.

---

## 📊 Core Technical Specifications
* **Standby Current Floor:** < 20µA active consumption (via native watchdog gating)
* **Hardware Footprint:** Modified ATmega328P architecture (SMD power trace severed)
* **Energy Management:** Upcycled 18650 Li-Ion storage loop coupled with a 5V mini epoxy solar module
* **Sensor Logic:** Marine-grade stainless steel fluid continuity probes

---

## 🗺️ System Interconnect Matrix

 5V SOLAR PANEL ] ──► [ 18650 LI-ION CELL ]│┌──────────────────────┴──────────────────────┐▼ (VCC / RAW Pin)                             ▼┌───────────────────┐                         ┌───────────────────┐│ ARDUINO PRO MINI  │                         │ ALERT TRANSDUCER  ││   (3.3V / 8MHz)   │                         │  (5V Piezo Array) │└─┬───────────────┬─┘                         └─────────┬─────────┘│               │                                     │▼ (Digital 2)   ▼ (Digital 5)                         │[STAINLESS]     [BC547 NPN BASE] ◄── 1kΩ Resistor          │[ PROBES  ]          │                                     │▼ (Collector) ────────────────────────┘[ GND PLANE ] (Emitter)
---

## 🚀 Quick Start Deployment
1. **Hardware Hack:** Mechanically sever or desolder the onboard power indicator LED from the Arduino Pro Mini to lower the passive floor draw.
2. **Flash Firmware:** Compile and upload the `aquashield_sleep.ino` file via your native Arduino IDE environment.
3. **Enclosure Rig:** Drill acoustic projection escape holes strictly on the bottom face of the IP65 junction box to prevent moisture pooling.

---
## 💻 Open Source EULA
Engineered by **RikMakersHub**. Licensed completely free for public customization, localized optimization, and global resource conservation.

**Come Check It Out In:** [RikAquaShield-Pro](https://rikmakershub.github.io/RikAquaShield-Pro/)
