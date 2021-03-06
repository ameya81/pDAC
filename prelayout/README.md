## Circuit Description

At the core of the ciruit is a simple switching circuit which, depending on the input bit provided selects one of the two voltage references. Using this switching circuit a 2-Bit DAC is created. The final circuit is built using many subcircuits in a hierarchical manner as:

#### 1. Switching Circuit is created to select one of the two reference voltages.

Here two inverters are created using transistors (M6,M2) and (M8,M4). The input is provided using label *d* in 1.8V domain and the inverted output is obtained from *d_inv* in 3.3V domain. The *d_inv* output is given as a input to the inverter(M8, M4) which bumps the output to 3.3V domain from 1.8V *d*. Thus *d_inv* is inverted to obtain *d* in 3.3V domain. These two signals control 2 transmission gates (M1,M7) and (M3,M5) to select one of the input voltage from *in_1* and *in_2*. The output is obtained at *Vout*.

![switch](https://user-images.githubusercontent.com/62995893/89989268-59eeff00-dc9e-11ea-9be0-05877ce28a05.jpg)

#### 2. A 2 bit dac is created using 3 switching circuits.

![2bitblock](https://user-images.githubusercontent.com/62995893/89989089-0da3bf00-dc9e-11ea-8b8f-09d9cbddabf3.png)

#### 3. A 3-Bit DAC is created using 2 2-Bit DACs

#### 4. A 4-Bit DAC is created using 2 3-Bit DACs

#### 5. A 5-Bit DAC is created using 2 4-Bit DACs

The points from 3 to 5 are shown in this block diagram

![circuitblock](https://user-images.githubusercontent.com/62995893/89987046-03cc8c80-dc9b-11ea-8440-7fac0c5e8edd.png)

#### 6. Finally following the same method a 10-Bit DAC is created with 2 9-Bit DACs

![8bitblock](https://user-images.githubusercontent.com/62995893/89987035-016a3280-dc9b-11ea-861d-b71c6f960476.png)

![10bitblock](https://user-images.githubusercontent.com/62995893/89987048-04652300-dc9b-11ea-82da-4bd60157a814.png)

![10bitDAC](https://user-images.githubusercontent.com/62995893/89992524-00d59a00-dca3-11ea-89ec-94b71ea70818.jpg)
