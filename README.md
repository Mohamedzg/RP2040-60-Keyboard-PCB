# ⌨️ RP2040 60% Keyboard PCB

My first custom mechanical keyboard PCB design, built with RP2040, hot-swap sockets, and a full matrix.

---

## ⚠️ Important Disclaimer

> 🚧 **This PCB has NOT been physically tested yet.**
> It has only been designed and verified in KiCad (DRC + ERC), but:
> * No real-world prototype has been assembled
> * There may be design mistakes
> * Use at your own risk if you decide to manufacture it

👉 *This project is shared for learning, experimentation, and community feedback.*

---

## 📸 Preview

*(You can add your renders or photos here later!)*

---

## 📌 Project Overview

This is a 60% mechanical keyboard PCB designed as a learning project.

I’m a systems & network student, and this is my first experience with:
* PCB design
* Electronics
* Hardware prototyping

Instead of starting small, I challenged myself with a full keyboard to learn faster.

---

## ⚙️ Features

* 🧠 **RP2040 MCU**
* 🔌 **USB-C connectivity**
* ⌨️ **60% layout**
* 🔁 **Kailh hot-swap sockets**
* 🔲 **Cherry MX compatible**
* 🔌 **Matrix scanning** (row/column)
* ➕ **Per-key diodes**
* 💡 **LED support** (basic implementation)
* 📦 **2-layer PCB** (JLCPCB / PCBWay ready)

---

## 📂 Repository Structure

```text
├── hardware
│   ├── kicad              → KiCad project files
│   ├── gerbers            → Ready-to-manufacture files
│   ├── schematic          → PDF + images
│   └── pcb                → Layout exports
├── bom
│   └── bom.csv            → Components list
└── docs
    └── images             → Renders, diagrams
├── README.md
└── LICENSE
