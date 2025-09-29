# Sequential Lamp Control Using Toggle

This project controls four lamps based on a push button sequence:

- 1st press: 1st lamp ON  
- 2nd press: All lamps OFF  
- 3rd press: 2nd lamp ON  
- 4th press: All lamps OFF  
- 5th press: 3rd lamp ON  
- 6th press: All lamps OFF  
- 7th press: 4th lamp ON  
- 8th press: All lamps OFF  

Implemented in TIA Portal v18 for S7-1200 and simulated with PLCSIM.

---

## Implementation Details

The project uses **3 toggles** to create a 3-bit binary counter (values 0 to 7):

- The **1st toggle** is triggered on the **positive edge** of the push button.  
- The **2nd toggle** is triggered on the **negative edge** of the 1st toggle’s output.  
- The **3rd toggle** is triggered on the **negative edge** of the 2nd toggle’s output.

This forms a binary count from `000` to `111` (0 to 7 in decimal). The count value is then used in a case (switch) statement to control which lamp is ON or if all lamps are OFF, achieving the desired sequence.
