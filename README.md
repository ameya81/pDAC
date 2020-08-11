# 10-Bit Potentiometric Digital-to-Analog Converter 
The projects intends to develop a 10-bit Potentiometric DAC using opensource tools like ngspice, magic to achieve specifications provided.

# Digital-to-Analog Converter
A Digital-to-Analog converter(DAC) is a system that converts digital values to analog signals. The output resolution of the DAC depends upon the no. of bits given as input to the system. DACs are essential in interfacing a digital domain to analog domain.

# A Glance at Potentiometric DAC IP
The introduction to PDAC can be found [here](resources/PDAC_introduction.pdf)

The specifications for the IP can be found [here](resources/pdac_ip.pdf)

# About the Device

Pin Functions
| Pins | Description |
| :--- | :--- |
| VREFL | Reference Voltage Low |
| VREFH | Reference Voltage High |
| D0-D9 | Digital Input |
| EN | Enable Device |
| VDD | Digital Supply |
| VSS | Digital Ground |
| VDDA | Analog Supply |
| VSSA | Analog Ground |
| OUT | Analog Out |

Device Parameters
| Parameter | Description | Min | Typ | Max | Unit |
| :--- | :--- | :--- | :--- | :--- | :--- |
| VDDA | Analog Supply | - | 3.3 | - | V |
| VDD | Digital Supply | - | 1.8 | - | V |
| VREFH | Reference Voltage High | - | - | 3.3 | V|
| VREFL | Reference Voltage Low | 0 | - | - | V |
| Resolution | - | - | 10 | - | Bit |
| INL | Integral Non Linearity | - | - | - | LSB |
| DNL | Differntial Non Linearity | - | - | - | LSB |

Description of INL and DNL

# Open-Source EDA Tools used
### `Ngspice`
[Ngspice](http://ngspice.sourceforge.net/) is a open source circuit simulator for electronic circuits. It is a command line tool and does not offer schematic entry.

###### Steps to Install 

Go to ngspice [installation](http://ngspice.sourceforge.net/download.html)

### `Magic VLSI`
[Magic](http://opencircuitdesign.com/magic/) VLSI is a open source VLSI layout tool written at Berkeley by John Ousterhout. 

###### Steps to Install 

Go to Magic [installation](http://opencircuitdesign.com/magic/)

# Pre-layout Simulations

# Future Work
Here goes the future work
