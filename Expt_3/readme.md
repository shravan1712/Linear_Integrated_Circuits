**Aim:**

**Design and analyse the differential amplifier for the following
specifications:**

**V<sub>DD</sub>=1.8V, P\<=2.2Mv, V<sub>ICM</sub>=0.95V,
V<sub>OCM</sub>=1.1V, V<sub>P</sub>=0.4V**

**Perform DC Analysis , Transient Analysis, Frequency response and
extract the paramaters.**

**Differential Amplifier:**

Differential amplifiers consist of two transistors M1 and M2, whose
sources are joined together. If the two transistors are connected to
different voltage inputs, then the current across M1 and M2 are
different due to the gate voltage. If the voltage supply at the gate
terminal is the same, then the current through M1 and M2 is also the
same. This configuration is called "Common-Mode Input Voltage
Differential Amplifier". Whatever may be the load resistor, the MOSFET
M1 and M2 should not enter the Triode region. It should be verified that
the MOSFETs remain in the Saturation Region for proper operation.

<img src="./media/image1.png" style="width:6.2in;height:5.49167in"
alt="image" />

Procedure : Make the circuit connection as given above. connect the
resister at the source terminal of both Mosfet now calculate the value
of I<sub>SS</sub> as power and V<sub>DD</sub> is given and calculate the
I<sub>D1</sub> and I<sub>D2</sub> now calculate the R<sub>SS</sub> and
R<sub>D</sub>

To find the all the values of resistor and current value. we need solve
the given question specification.

I<sub>SS</sub> =P/ V<sub>DD</sub> =2.2/1.8=1.22mA

I<sub>D1</sub>=I<sub>D2</sub> = I<sub>SS</sub>/2=0.61mA

R<sub>D</sub> = V<sub>DD</sub>
-V<sub>OCM</sub>/I<sub>D1</sub>=1.8-1.1/0.61=1.145kΩ

R<sub>SS</sub> =Vp/ I<sub>SS</sub> =0.4/1.22=0.327kΩ

Finally by solving we get

I<sub>SS</sub> =0.909mA

I<sub>D1</sub>=I<sub>D2</sub>=0.61mA

R<sub>D</sub> =3.55kΩ

R<sub>SS</sub> =0.327kΩ

**Circuit-1**

<img src="./media/image2.png"
style="width:5.62662in;height:3.46225in" />

Now to get the desired values of output voltage and current we have to
vary the width and length of both the Mosfet we got Length=180nm and
width=108.5um

<img src="./media/image3.png"
style="width:2.10029in;height:1.64537in" />

**DC analysis:**

To perform the DC analysis we have to select the {DC op pnt} in the edit
simulation command and run the simulation the figure below is the values
obtained from the DC analysis 

<img src="./media/image4.png" style="width:4.7197in;height:3.47467in" />

Here in dc analysis we got the V<sub>OUT</sub> as expected and
I<sub>D1</sub> and I<sub>D2</sub> we got the same

**Transient analysis:**

To perform transient analysis we have to select the transient analysis
in the edit simulation and give the stop time as 5ms and run the
simulation . and the graph below shows the transient response of the
design. 

<img src="./media/image5.png"
style="width:6.26806in;height:3.32986in" />

Voltage Gain A<sub>V</sub>=V<sub>OUTP-P</sub> /V<sub>INP-P</sub>

A<sub>V</sub>=(0.269V/50mV)

A<sub>V</sub> =5.38

**AC analysis:**

TO perform AC analysis we have to select the ac analysis in the edit
simulation command given the values as shown below ;

<img src="./media/image6.png"
style="width:6.26806in;height:3.32986in" />

Gain in db= 20log(AV)

=20log(5.38)

=14.616

**Circuit-2:**

Now replace the R<sub>SS</sub> resister with a current source : connect
a current source of 1.22mA

<img src="./media/image7.png"
style="width:4.66853in;height:2.93418in" />

**DC analysis:**

To perform the DC analysis we have to select the {DC op pnt} in the edit
simulation command and run the simulation the figure below is the values
obtained from the DC analysis

<img src="./media/image8.png" style="width:5.31677in;height:3.9596in" />

**Trasient analysis:**

To perform transient analysis we have to select the transient analysis
in the edit simulation and give the stop time as 5ms and run the
simulation . and the graph below shows the transient response of the
design

we have to give degree of 180deg to one Mosfet and 0deg to the other
Mosfet and ac amplitude 1 for one Mosfet and 0 for other Mosfet

<img src="./media/image9.png"
style="width:6.17082in;height:3.27821in" />

Voltage Gain A<sub>V</sub>=V<sub>OUTP-P</sub> /V<sub>INP-P</sub>

A<sub>V</sub>=(1.33-0.870)/(0.999-0.900)

A<sub>V</sub> =4.64

**AC analysis:**

<img src="./media/image10.jpeg" style="width:6.26806in;height:3.32986in"
alt="WhatsApp Image 2025-03-02 at 23 23 18_44d7f151" />

Gain in db= 20log(AV)

=20log(4.64)

=13.33

**Circuit-3:**<img src="./media/image11.png" style="width:6.26806in;height:4.09167in"
alt="image" />

**DC analysis:**

<img src="./media/image12.png"
style="width:6.26806in;height:4.31389in" />

Next, we need to calculate power, to make sure that the power is within
2.2 mW, to satisfy our power budget.

P = V<sub>DD</sub>.I<sub>SS</sub> = 1.8 V x 1.22226 mA = **2.200068
mW** *≈* 2.2 mW

Therefore, this fits our power budget, and we can proceed further. Next,
we can perform transient analysis, by applying ac input to any one of
the MOSFETs, and then calculating V/V gain, dB gain.

**Transient Analysis**

Apply a sinusoidal signal with DC offset = V<sub>G</sub> = 0.95 V,
Amplitude = 50 mV, Frequency = 1 kHz. In transient analysis, set stop
time to 5 ms. Place the .tran 5m directive anywhere on the schematic and
run the simulation.

<img src="./media/image13.png"
style="width:6.26806in;height:5.34653in" />

We can calculate the V/V gain by dividing
V<sub>out</sub>/V<sub>in</sub>. Also, the output voltage curve (green)
appears inverted compared to the input voltage curve (blue) due to a
180° phase shift.

A<sub>v</sub> = V<sub>out</sub>/V<sub>in</sub> = 0.285/50 mV = **5.7
V/V**

Converting this to dB, we get A’<sub>v</sub> =
20log<sub>10</sub>(A<sub>v</sub>) = 20log<sub>10</sub>(5.7) = **15.117
dB**

Now, let us perform AC analysis and then verify our calculated results.

**AC analysis:**

<img src="./media/image14.png"
style="width:6.26806in;height:3.32986in" />

As we can see, we get a midband gain of around **15.4 dB**, which is
close to the calculated value. We can also the 3 dB bandwidth at
around **2 GHz**. From the figure, we can see that the curve is not the
standard frequency response we are used to seeing. This may be due to
the effects of the NMOS behaving as a current source, which could
explain why a current source is used since it provides stability, and
prevents noise and fluctuation.

**INFERENCE:**

After performing this experiment, we learnt how the differential
amplifier operates, and how to build it in LTSpice. We see how the
differential amplifier rejects common mode signals, but amplifies
differential mode signals, making it the ideal building block for the
operational amplifier or the op-amp.

We also observed the three different configurations for the differential
amplifier, i.e., with resistance R<sub>SS</sub>, current source
I<sub>SS</sub>, the NMOS biased as a current source operating in
saturation region.

The highest gain we observed was in the NMOS configuration, which
provided a dB gain of 15.4 dB, compared to the other two configurations.
However, the frequency response for this configuration seems very
unstable, with constant fluctuations before the midband (possibly due to
the effects of the NMOS).

The advantage of the current source configuration is that we obtained
almost exact parameters that we had calculated for. It also provides a
more stable current I<sub>SS</sub>, since there won’t be any
fluctuations due to temperature, or any other reason. Lastly the
R<sub>SS</sub> configuration also seems reliable, but with increase in
temperature and tolerance errors, we may not get exact value of
resistance we calculated, which may decrease or increase our current
values, causing issue in power budget.

Overall, the differential amplifier is a very useful configuration,
since it measures the difference between the two drain voltages, thereby
preventing the effects of any noise. Another point to note is that the
differential amplifiers require two exactly matched N-channel MOSFETs,
making it easier to implement the circuit in LTSpice, using the 180 nm
TSMC .lib technology file.
