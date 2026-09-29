# Solar Panel Wash Controller

An automated, hardware-timed electronic controller PCB designed to schedule and actuate solar panel washing cycles to mitigate dust accumulation, soiling losses, and photovoltaic efficiency degradation.

Designed in KiCad with integrated Real-Time Clock (RTC) scheduling, high-current pump relay/driver stages, and industrial terminal interfaces.

---

## Features

- **Automated Cleaning Schedule**:
  - Precision timekeeping via dedicated I2C Real-Time Clock (RTC) module (DS3231/DS1307 battery-backed) for reliable daily or weekly dawn/dusk wash cycles.
- **Robust Pump & Solenoid Drive Stage**:
  - High-current relay and switching stage engineered to drive 12V/24V high-pressure water booster pumps and solenoid valves.
  - Flyback diode suppression and optocoupled logic isolation to prevent inductive transient resets.
- **Aesthetic Rounded-Track PCB Design**:
  - Custom PCB routing featuring smooth curved/teardrop trace geometry for improved signal integrity and solder-mask resilience.
  - Multi-layer power routing with broad copper pours to handle high inrush pump currents.
- **Modular Sub-System Layout**:
  - Dedicated sub-module architecture separating the low-voltage control/logic plane from the high-voltage actuator switching plane.

---

## Hardware Specification

- **RTC Module**: I2C Real-Time Clock with CR2032 backup battery holder (`RTC Module.kicad_sym`).
- **Control Interface**: Multi-pin microcontroller interface header with analog and digital telemetry pins.
- **Output Actuators**: SPDT Power Relays / High-Side Power Switching stages.
- **PCB Stackup**: 2-layer FR4 (1.6 mm core, 1 oz copper).
- **Renders & Manufacturing**:
  - 3D photorealistic board renders: `Front.png` and `Back.png`.
  - Manufacturing schematic: `Schematic.pdf`.

---

## Project Structure

```text
Solar-Panel-Wash-Controller/
├── Front.png                         # 3D PCB front render
├── Back.png                          # 3D PCB back render
├── Schematic.pdf                     # Complete schematic documentation
├── Solar_pannel_wash_controller.kicad_sch # Main KiCad schematic
├── Solar_pannel_wash_controller.kicad_pcb # Main KiCad PCB layout
├── Solar_pannel_wash_controller.kicad_pro # KiCad project configuration
├── RTC Module.kicad_sym              # Custom RTC schematic symbol
├── Solar_pannel_wash_controller_sub-modules/ # Modular breakout & rounded PCB files
│   ├── Solar_pannel_wash_controller_sub-modules.kicad_sch
│   ├── Solar_pannel_wash_controller_sub-modules.kicad_pcb
│   └── Solar_pannel_wash_controller_sub-modules-rounded.kicad_pcb
├── .gitignore                        # Git ignore rules
└── README.md                         # Project documentation
```

---

## EDA & Design Files

Designed using **KiCad 7 / 8**:
- Open `Solar_pannel_wash_controller.kicad_pro` to inspect or modify the full system schematic and board layout.
- Review `Schematic.pdf` for circuit wiring, power distribution networks, and connector assignments.

---

## License

Hardware design. All rights reserved by the author.
