⚠️ Important Disclaimer

🚧 This PCB has NOT been physically tested yet.
It has only been designed and verified in KiCad (DRC + ERC), but:

No real-world prototype has been assembled
There may be design mistakes
Use at your own risk if you decide to manufacture it

👉 This project is shared for learning, experimentation, and community feedback

📸 Preview

(you can add your renders here later)

📌 Project Overview

This is a 60% mechanical keyboard PCB designed as a learning project.

I’m a systems & network student, and this is my first experience with:

PCB design
Electronics
Hardware prototyping

Instead of starting small, I challenged myself with a full keyboard to learn faster.

⚙️ Features
🧠 RP2040 MCU
🔌 USB-C connectivity
⌨️ 60% layout
🔁 Kailh hot-swap sockets
🔲 Cherry MX compatible
🔌 Matrix scanning (row/column)
➕ Per-key diodes
💡 LED support (basic implementation)
📦 2-layer PCB (JLCPCB / PCBWay ready)
📂 Repository Structure
/hardware
  /kicad              → KiCad project files
  /gerbers            → Ready-to-manufacture files
  /schematic          → PDF + images
  /pcb                → Layout exports
/bom
  bom.csv             → Components list
/docs
  images              → Renders, diagrams
README.md
LICENSE
🧩 How the Keyboard Works
Matrix Design

The keyboard uses a row/column matrix:

Each key = switch + diode
Rows → outputs
Columns → inputs (or vice versa)

👉 This reduces GPIO usage on the RP2040.

🔄 Example Flow
MCU activates a row
Reads all columns
Detects which switch is pressed
Moves to next row
➕ Why Diodes?

Each switch includes a diode to prevent:

❌ Ghosting
❌ Key conflicts
🔌 USB & Power
USB-C connector
5V input → regulated to 3.3V
ESD protection included (basic)
Decoupling capacitors near MCU

⚠️ This section is one of the areas I’m least confident about

💡 LEDs
Basic per-key LED footprint included
No advanced RGB controller
No firmware implementation yet

👉 This will likely be improved in V2

🛠️ How to Manufacture
1. Export Gerbers

Already included in /gerbers

2. Order PCB

You can use:

JLCPCB
PCBWay

Recommended settings:

Layers: 2
Thickness: 1.6mm
Copper: 1oz
Finish: HASL or ENIG
3. Order Components

Use /bom/bom.csv

Main parts:

RP2040
USB-C connector
Diodes (SMD)
Resistors / capacitors
Kailh hot-swap sockets
4. Assembly

Steps:

Solder MCU + passive components
Solder USB section
Add diodes
Install hot-swap sockets
Plug switches
💻 Firmware

Planned support:

QMK
KMK (Python, RP2040 friendly)

⚠️ Firmware not fully tested yet

🧱 Mounting Style

Currently:

PCB includes mounting holes
Designed to be compatible with tray mount (most likely)
🧠 Future consideration:
Gasket mount support
Plate integration
Case compatibility
🚧 Known Uncertainties / Risks

Things I’m not fully confident about:

❓ USB power section
❓ LED wiring
❓ Some routing choices
❓ Trace widths in certain areas
❓ Mounting hole placement
❓ Noise / signal integrity
🔄 V2 (In Progress)

Already planned improvements:

✅ Design fixes after first prototype
🔌 Improved USB + power circuit
💡 Better LED implementation (possibly RGB)
📐 Cleaner routing
🧱 Case compatibility improvements
🧊 Keyboard Case (Fusion 360)

🛠️ A custom keyboard case is currently being designed in Fusion 360

👉 Not ready yet — stay tuned

🤝 Contributing

Feedback is highly appreciated 🙌

If you notice:

Design mistakes
Better routing ideas
Power improvements
General suggestions

👉 Open an issue or PR

📖 Learning Resources

This project was inspired by:

RP2040 design guides
Open-source keyboard PCBs
Community projects
📜 License

Open-source (choose one):

MIT
CERN OHL (recommended for hardware)
🙌 Final Note

This is my first PCB ever, so expect imperfections.

The goal is:

Learn
Share
Improve publicly

If this helps you or you build it → that’s already a win.

⭐ Support

If you like the project:

⭐ Star the repo
🍴 Fork it
🧠 Suggest improvements
