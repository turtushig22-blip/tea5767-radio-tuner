# Tea5767-based Radio Tuner
  An Arduino Uno FM radio tuner utilizing the TEA5767 module and a 16x2 LCD. Features POT and PRESET tuning modes. Evolving from a breadboard prototype into a custom PCB project.

### Initial Prototype

  The project built an FM radio device using the TEA5767 radio module and the Arduino UNO in January 2026. Phase 2 includes designing a compact, custom-designed PCB board with further improvements while keeping the design simple and reproducible. The steps will be documented in this repository as I work on the PCB design (so, hopefully, I can finish this project).

  Primary functions of the prototype Arduino circuit include manual and preset FM tuning, displaying the current frequency via a 16x2 LCD, and outputting the audio via wired headphones. We could not use speakers to output sound as the TEA5767 module does not have a built-in speaker smplifier, which required us to sodler directly onto the module. A photo of the prototype circuit can be seem from Figure 1 and Figure 2. 

<img width="50%" height="3073" alt="IMG_8481" src="https://github.com/user-attachments/assets/b35eaf25-04c4-40bf-98c2-4cec20e6fc4c" />   Figure 1.

<img width="80%" height="427" alt="Screenshot 2026-06-10 at 11 31 26" src="https://github.com/user-attachments/assets/b497ef54-2f2f-4c2c-9588-3f1615963869" />   Figure 2.

 To see a video demonstration of the prototype, please follow https://youtu.be/HQ7OcgIyThs, and for a detailed breakdown of the theory, component selection, and circuit design, you can read [PDF File](Producing_an_FM_Radio_Tuner.pdf).

## PCB Design
### Schematic 
To further improve the project, I decided to let it be my first PCB design while improving the radio device as well. The improvements that have been made include PAM8403 amplifier that will feed the audio into two 3-Watt, 4-Ohm speakers while working as a volume control, an ESP32 Development Board instead of the Arduino UNO to save space on the PCB, a 0.96 OLED display replacing the 16x2 Liquid Crystal Display for a similar reason, and a KY-040 rotary encoder that will serve as both the manual frequency and preset frequency control. 

I continued the project by drawing the circuit schematic in KiCad. The schematic can be seen in Figure 3. 
<img width="80%" height="668" alt="image" src="https://github.com/user-attachments/assets/55278728-316c-4677-8030-318b2a567f4f" />   Figure 3.

### Footprints.
As the project required modules whose footprints do not readily exist in KiCad, I used it to learn to create custom footprints as well. The footprints for the ESP32-DevKit-32E, TEA5767, PAM8403, KY-040, and the 0.96 OLED Display are included in the 'Custom_Footprints.pretty' folder. Photos of the custom footprints are attached below. 

<img width="30%" height="707" alt="image" src="https://github.com/user-attachments/assets/14ccbb63-4989-4220-851b-c2662130ea2f" /> <img width="30%" height="542" alt="image" src="https://github.com/user-attachments/assets/b04eda3b-b7d1-4b83-af2e-7bae6d7ef63d" />   ESP32-DevKit-32E Footprint


