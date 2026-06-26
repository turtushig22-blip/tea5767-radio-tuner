# tea5767-radio-tuner
An Arduino Uno FM radio tuner utilizing the TEA5767 module and a 16x2 LCD. Features POT and PRESET tuning modes. Currently evolving from a breadboard prototype into a custom PCB project.

### Initial Prototype

The project built an FM radio device using the TEA5767 radio module and the Arduino UNO in January 2026. Phase 2 includes designing a compact, custom-designed PCB board with further improvements while keeping the design simple and reproducible. The steps will be documented in this repository as I work on the PCB design (so, hopefully, I can finish this project).

Primary functions of the prototype Arduino circuit include manual and preset FM tuning, displaying the current frequency via a 16x2 LCD, and outputting the audio via wired headphones. A photo of the prototype circuit can be seem from Figure 1 and Figure 2. 

<img width="30%" height="3073" alt="IMG_8481" src="https://github.com/user-attachments/assets/b35eaf25-04c4-40bf-98c2-4cec20e6fc4c" /> Figure 1.

<img width="70%" height="427" alt="Screenshot 2026-06-10 at 11 31 26" src="https://github.com/user-attachments/assets/b497ef54-2f2f-4c2c-9588-3f1615963869" /> Figure 2.

If you wish to see a video demonstration of the prototype, please follow https://youtu.be/HQ7OcgIyThs, and for a detailed breakdown of the theory, component selection, and circuit design, you can read [Producing_an_FM_Radio_Tuner.pdf](https://github.com/user-attachments/files/28803972/Producing_an_FM_Radio_Tuner.pdf).


### This is the continuation of my Arduino Radio Module project, completed in January 2026. 

To further improve the project, I decided to let it be my first PCB design while improving the module as well. The improvements made include a PAM8403 amplifier that will feed the audio into two 3-Watt, 4-Ohm speakers and work as a volume control, an ESP32 Development Board instead of the Arduino UNO to save space on the PCB, a 0.96 OLED display replacing the 16x2 Liquid Crystal Display, and a KY-040 rotary encoder that will serve as the frequency control. 
