# FreeRTOS SMP Demo - Dual Core Example

## Description

This is a demo program using FreeRTOS SMP (Symmetric Multiprocessing) on both cores of the Raspberry Pi Pico. It includes:

- A **Blink task** running on **Core 0** to blink an LED connected to GPIO 0.
- A **Blink task** running on **Core 1** to blink an LED connected to GPIO 25.
- A **Counter task** running on **Core 1** that drives 4 LEDs connected to GPIO 2, 3, 4, and 5.
- The **Main task** running on **Core 0** sends instructions to the Counter task every 3 seconds, and also prints runtime statistics.

### Modifications

1. **GPIO Change for LED**:
   - The `LED5_PAD` pin was changed from **GPIO 15** to **GPIO 25** in the second version of the code. This affects the blinking behavior of the second LED connected to the GPIO pin.
   
   **Old code:**

   #define LED5_PAD 15
   
   **New code:**
   
   #define LED5_PAD 25

2. **Added Debug Print Statement**:
   - A new print statement was added to display the message **"DELOBELLE Jules F14218805"** during the main loop in the mainTask function
  
   **New code:**
   
   printf("DELOBELLE Jules F14218805");
