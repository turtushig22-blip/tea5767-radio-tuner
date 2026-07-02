
## This is the continuation of my Arduino Radio Module project, completed in January 2026. 

To further improve the project, I decided to let it be my first PCB design while improving the radio device as well. The improvements that have been made include PAM8403 amplifier that will feed the audio into two 3-Watt, 4-Ohm speakers while working as a volume control, an ESP32 Development Board instead of the Arduino UNO to save space on the PCB, a 0.96 OLED display replacing the 16x2 Liquid Crystal Display for a similar reason, and a KY-040 rotary encoder that will serve as both the manual frequency and preset frequency control. 

I continued the project by drawing the circuit schematic in KiCad. The schematic can be seen in Figure 3. 
<img width="70%" height="668" alt="image" src="https://github.com/user-attachments/assets/55278728-316c-4677-8030-318b2a567f4f" /> Figure 3.

As the project required modules whose footprints do not readily exist in KiCad, I used it to learn to create custom footprints as well. The footprints for the ESP32-DevKit-32E, TEA5767, PAM8403, KY-040, and the 0.96 OLED Display are included in the Custom Footprints branch. 
