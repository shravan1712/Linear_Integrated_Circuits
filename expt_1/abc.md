# Experiment 1
## Design 1: Simulation of CS Amplifier
### Aim: Simulate the DC analysis, Transient, and AC analysis of a CS amplifier circuit using LTSpice.
### Circuit:
 ![image](https://github.com/user-attachments/assets/e775bd9c-21dd-45f0-97a3-7c2c30dc9d32)

### Procedure
1.	Design the CS amplifier circuit.
2.	Naming the NMOS as CMOSN.
3.	DC Analysis: Apply the DC voltage of VDD = 1.8 V and VGS = 0.9 V. In LTSpice, go to the Simulate option and select Edit Simulation Command. Click on DC Analysis, then press OK. Click on Run in the tab menu to obtain the DC operating point Vout. Set the Length as constant and determine the Width such that ID = 55.5 uA.
4.	Transient Analysis: Modify the VGS voltage source to a sine wave input with:
o	DC level= 0.9 V
o	Amplitude= 50 mV
o	Frequency= 1 kHz
In LTSpice, go to Edit Simulation Command, select Transient Analysis. Set the Stop Time as 5ms, then click OK.
5.	AC Analysis: In Edit Simulation Command, select AC Analysis. Set the Type of Sweep to Decade. Set Points per Decade to 10. Set the Frequency Range from 0.1 Hz to 1 THz. Click OK. Determine the gain and frequency response of the circuit.
#### Calculation
Power Calculation P = 100 uW
Drain Equation VDD = VDS + ID*RD
P = I*V
Given: ID = 55.5 uA, VDD = 1.8 V
Thus VDS = Vout
Rd=32.4Kohm, but used 22 Kohm
Length= 180 nm
Width=18 um(Found by keeping the Length constant).
VDS=0.467 V
Q point is (0.467 V,55.55 uA)
### Results:
#### 1. DC Analysis:
 ![image](https://github.com/user-attachments/assets/1db0371c-b568-4750-abb2-515a0d3e231d)

Drain current Id=55.55 uA Vout=0.467 V
Width=18 um for length=180 nm
#### 2. Transient Analysis:
 ![image](https://github.com/user-attachments/assets/10451bdf-afdd-412a-8352-c9d3d458f864)

There is a 180-degree phase shift between the input and output
#### 3. AC Analysis: 
![image](https://github.com/user-attachments/assets/606eb559-99f4-43a6-81d8-d99f13b4bed3)

Gain=20 dB.
### Inference:
1. The Width of the MOSFET directly affects the Drain current.
2. By changing the dimensions of the MOSFET we can directly control the amount of Drain current.
3. 180-degree phase shift between the input and output waveform.
4. The CS amplifier has a larger gain =20 dB. (i.e, the output signal is 20 times larger than the input signal)
### Design 2: Simulation of CMOS Amplifier
### Aim: Simulate the DC analysis, Transient, and AC analysis of a CMOS amplifier circuit using LTSpice.
### Circuit:
 ![image](https://github.com/user-attachments/assets/defc3938-4bd6-4304-88de-c025f0b0d102)

### Procedure
1.	Design the CMOS amplifier circuit.
2.	Naming the NMOS as CMOSN and PMOS as CMOSP.
3.	Apply the DC voltage of VDD = 1.8 V
4.	DC sweep Analysis: Go to the edit simulation command select the DC sweep option and choose: -Source name= Vin. -type of Sweep Linear. -start value=0, -stop value =VDD=1.8 V. -increment=0.1.
find the Vin from the VTC curve
5. DC Analysis: Put the appropriate Vin value. go to the Simulate option and select Edit Simulation Command. Click on DC Analysis, then press OK. Click on Run in the tab menu to obtain the DC operating point Vout. Set the Length as constant and determine the Width such that ID = 55.5 uA.
6.	Transient Analysis: Modify the Vin voltage source to a sine wave input with:
o	DC level= 0.9 V
o	Amplitude= 50 mV
o	Frequency= 1 kHz
In LTSpice, go to Edit Simulation Command, select Transient Analysis. Set the Stop Time as 5ms, then click OK.
7.	AC Analysis: In Edit Simulation Command, select AC Analysis. Set the Type of Sweep to Decade. Set Points per Decade to 10. Set the Frequency Range from 0.1 Hz to 1 THz. Click OK. Determine the gain and frequency response of the circuit.
#### Calculation
ID = 55.5 uA, VDD = 1.8 V
Length M1= 180 nm
Width=190 nm(found by keeping the Length of M1 constant)
Length M2= 180 nm
Width=449 um(found by keeping the Length of M2 constant)
### Results:
#### 1. DC Sweep Analysis:
 ![image](https://github.com/user-attachments/assets/672a0e36-bcb0-4e3b-bc0d-c36824be1aca)
 
The value of the Vin is selected as 0.8V as it is present in the middle of the saturation region of the VTC Curve.

#### 2. DC Analysis:
 ![image](https://github.com/user-attachments/assets/672d197c-60b1-4507-8d0b-364aaaee52d1)
 
drain current Id=55.55 uA Vout=1.22 V
Length M1= 180 nm, Width=190 nm for M1.
Length M2= 180 nm, Width=449 um for M2.
#### 3. Transient Analysis:
 ![image](https://github.com/user-attachments/assets/e9546a7e-0a57-4f80-9ffb-268635a7d8fc)
 
There is a 180-degree phase shift between the input and output
#### 4. AC Analysis:
 ![image](https://github.com/user-attachments/assets/6bc8cd6f-8f4b-4710-b3bd-3215cd1ec76d)
 
Gain=5.5 dB
### Inference:
1. The Width of the MOSFET directly affects the Drain current.
2. By changing the dimensions of the MOSFET -M1 -when varying the width of PMOS there is not a lot of change in the drain current(i.e., Id doesn't get affected much).
-M2 -when varying the width of NMOS there is a drastic change in the drain current.
3. If width is increased it leads to a higher gain 4.180 degree phase shift between the input and output waveform.
5. The CMOS amplifier has a gain =5.5 dB. (i.e, the output signal is almost 6 times larger than the input signal)
