# Chemical Reactor Control - TIA Portal Mini Project

## Overview

This mini project simulates the control logic of a **chemical reactor vessel** operating under specific temperature and pressure conditions. Implemented in **TIA Portal**, the system monitors and controls various components to ensure safe and efficient operation.

## System Components and Logic

- **Relief Valve**  
  → Opens **if high pressure** is detected.

- **Cold Water Inlet**  
  → Activates **if high temperature** is detected.

- **Heater**  
  → Turns on if:  
  &nbsp;&nbsp;&nbsp;&nbsp;• Temperature is **low**, or  
  &nbsp;&nbsp;&nbsp;&nbsp;• Pressure is **low** and temperature is **normal**.

- **Mixer**  
  → Runs when either the **cold water inlet** or the **heater** is active.

- **Start Indıcator**  
  → System starts when **temperature is low**.

- **Normal Operation Indicator**  
  → Turns on when **pressure is normal**.

- **Alarm Indicator**  
  → Activates in case of **high pressure**.

## Notes

- All control logic is implemented in ladder logic using basic instructions.
- Outputs are used to simulate valves, heater, and indicators.
