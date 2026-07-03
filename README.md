# Tea5767-based Radio Tuner
  An Arduino Uno FM radio tuner utilizing the TEA5767 module and a 16x2 LCD. Features POT and PRESET tuning modes. Evolving from a breadboard prototype into a custom PCB project.

### Initial Prototype

  The project built an FM radio device using the TEA5767 radio module and the Arduino UNO in January 2026. Phase 2 includes designing a compact, custom-designed PCB board with further improvements while keeping the design simple and reproducible. The steps will be documented in this repository as I work on the PCB design (so, hopefully, I can finish this project).

  Primary functions of the prototype Arduino circuit include manual and preset FM tuning, displaying the current frequency via a 16x2 LCD, and outputting the audio via wired headphones. We could not use speakers to output sound as the TEA5767 module does not have a built-in speaker smplifier, which required us to sodler directly onto the module. A photo of the prototype circuit can be seen from Figure 1 and Figure 2. 

<img width="30%" height="3073" alt="IMG_8481" src="https://github.com/user-attachments/assets/b35eaf25-04c4-40bf-98c2-4cec20e6fc4c" />   Figure 1 [Photo of the prototype that used Arduino UNO].

<img width="70%" height="427" alt="Screenshot 2026-06-10 at 11 31 26" src="https://github.com/user-attachments/assets/b497ef54-2f2f-4c2c-9588-3f1615963869" />   Figure 2 [Circuit Diagram of the prototype].

 To see a video demonstration of the prototype, please follow https://youtu.be/HQ7OcgIyThs, and for a detailed breakdown of the theory, component selection, and circuit design, you can read this [PDF File](Producing_an_FM_Radio_Tuner.pdf).

## PCB Design
### Schematic 
To further improve the project, I decided to let it be my first PCB design while improving the radio device as well. The improvements that have been made include PAM8403 amplifier that will feed the audio into two 3-Watt, 4-Ohm speakers while working as a volume control, an ESP32 Development Board instead of the Arduino UNO to save space on the PCB, a 0.96 OLED display replacing the 16x2 Liquid Crystal Display for a similar reason, and a KY-040 rotary encoder that will serve as both the manual frequency and preset frequency control. 

I continued the project by drawing the circuit schematic in KiCad. The schematic can be seen in Figure 3. 
<img width="70%" height="668" alt="image" src="https://github.com/user-attachments/assets/55278728-316c-4677-8030-318b2a567f4f" />   Figure 3 [Schematic of the ESP32-based Circuit]. 

(To feed the audio signal from the TEA5767 module to the PAM8403 amplifier, I used a 3.5mm jack with a bare wire end, which was then connected to the L, G, and B pins on the amplifier. Note that these connections are not reflected in the schematic of the circuit as KiCad does not allow the schematic symbol of a device to have more pins than the device's footprint, which becomes a bit complicated for the TEA5767 module as it does not have designated pins for the L, G, R. One way to solve this is to draw the 3.5mm jack in the schematic editor; however, as the jack and the connection between the two modules will never actually touch the PCB, I decided to simply leave the pins on the amplifier not connected and draw the TEA5767 with only its physical pins).

### Footprints.
As the project required modules whose footprints do not readily exist in KiCad, I used it to learn to create custom footprints as well. The footprints for the ESP32-DevKit-32E, TEA5767, PAM8403, KY-040, and the 0.96 OLED Display are included in the 'Custom_Footprints.pretty' folder. Photos of the custom footprints are attached below. 

<img width="30%" height="707" alt="image" src="https://github.com/user-attachments/assets/14ccbb63-4989-4220-851b-c2662130ea2f" /> <img width="30%" height="542" alt="image" src="https://github.com/user-attachments/assets/b04eda3b-b7d1-4b83-af2e-7bae6d7ef63d" />   Figure 4 [ESP32-DevKit-32E Footprint]. 

<img width="30%" height="253" alt="image" src="https://github.com/user-attachments/assets/a7dc9170-27c6-4f8e-bbdf-2d84467356b1" /> <img width="30%" height="190" alt="image" src="https://github.com/user-attachments/assets/36c975ba-17b6-4889-b303-6f582b961239" />   Figure 5 [TEA5767 footprint]. 

<img width="30%" height="608" alt="image" src="https://github.com/user-attachments/assets/465225b9-9ee4-4e5d-9032-816f5299d809" /> <img width="30%" height="544" alt="image" src="https://github.com/user-attachments/assets/a31eb647-fcd1-42c8-9416-5337d2216461" />   Figure 6 [PAM8403 footprint]. (Note that the PAM8403 used in this project is the "knobby" version of the PAM8403 amplifier board, which allows it to work as the volume control. Furthermore, note that the knobs on the PAM8403 and KY-040 modules are not included in their corresponding footprints for the ease of drawing the footprint and because the boards will not physically touch the PCB).

<img width="30%" height="601" alt="image" src="https://github.com/user-attachments/assets/386cddac-ef01-4aad-add5-2574a7bbf171" /> <img width="30%" height="545" alt="image" src="https://github.com/user-attachments/assets/c96b6515-2261-4d32-993f-d02bc1ebba25" />    Figure 7 [KY-040 footprint]. 

<img width="30%" height="603" alt="image" src="https://github.com/user-attachments/assets/e0f12dd3-e6d5-4338-a470-11bb316b93d5" /> <img width="30%" height="541" alt="image" src="https://github.com/user-attachments/assets/527405b2-6622-4d6a-a290-f59a3dcfd3b5" />   Figure 8 [0.96 OLED Display footprint].

### PCB Layout
After creating the custom footprints, I created the PCB design inside KiCad's PCB editor. A picture of the PCB layout from KiCad's PCB editor is shown in Figure 9. 

<img width="70%" height="796" alt="image" src="https://github.com/user-attachments/assets/853ca83b-9713-4130-ac22-ee88a3b29b99" /> Figure 9 [PCB Layout of the Radio Module]. 





