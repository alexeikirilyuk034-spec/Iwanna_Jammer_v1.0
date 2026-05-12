HI!
I made a PCB board for the jammer.
The components include four standard NRF24 PA LNAs, an AMS1117 3.3v, and an ESP32 devkitc (original).
For stable operation of the four nRF24L01+PA+LNA modules, you will need the following capacitors: a 100 µF electrolytic capacitor at the AMS1117 input (VIN), a 100 µF electrolytic capacitor at the AMS1117 output (VOUT), and a 0.1 µF ceramic capacitor (104) in parallel—this is critical for the stability of the regulator itself. For each of the four nRF24 modules, install a pair directly at the VCC and GND pins: a 100–220 µF electrolytic capacitor (to reserve energy when starting transmission) and a 0.1 µF ceramic capacitor (to filter high-frequency interference). The ceramic capacitors should be soldered using the shortest possible wires or directly to the module's board. In total, you need 5 electrolytic capacitors of 100–220 μF and 5 ceramic capacitors of 0.1 μF (one set for the stabilizer and one for each of the 4 radio modules).

IMPORTANT! There is an ESP32 devkitc, but with different pins. It's important to find the exact version I used!
<img width="1020" height="1005" alt="Снимок экрана 2026-05-11 195434" src="https://github.com/user-attachments/assets/ebef1a16-1614-44e7-897b-a030c76a4733" />
<img width="1066" height="1040" alt="Снимок экрана 2026-05-11 195423" src="https://github.com/user-attachments/assets/fd9a1275-a134-46aa-8588-f9a7ccfcd0c6" />
<img width="2560" height="1441" alt="photo_2026-05-12_20-42-18" src="https://github.com/user-attachments/assets/4f3c1d37-25b5-450a-bacb-3dc6ab1b863f" />
<img width="2560" height="1441" alt="photo_2026-05-12_20-42-15" src="https://github.com/user-attachments/assets/8b6b5f43-a34f-482a-8abc-3a3683df5fbf" />
