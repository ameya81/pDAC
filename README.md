*Note the project is understandby*

# 10-Bit Potentiometric Digital-to-Analog Converter 
The projects intends to develop a 10-bit Potentiometric DAC using opensource tools like ngspice, magic to achieve specifications provided.

# Digital-to-Analog Converter
A Digital-to-Analog converter(DAC) is a system that converts digital values to analog signals. The output resolution of the DAC depends upon the no. of bits given as input to the system. DACs are essential in interfacing a digital domain to analog domain.

# A Glance at Potentiometric DAC IP
The introduction to PDAC can be found [here](resources/PDAC_introduction.pdf)

The specifications for the IP can be found [here](resources/pdac_ip.pdf)

# About the Device

###### Block Diagram

![DACblockdiagram](https://user-images.githubusercontent.com/62995893/89901548-de8c3f80-dc02-11ea-9f6c-9e57c9825c60.jpg)

###### Pin Functions
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

###### Device Parameters
| Parameter | Description | Min | Typ | Max | Unit |
| :--- | :--- | :--- | :--- | :--- | :--- |
| VDDA | Analog Supply | - | 3.3 | - | V |
| VDD | Digital Supply | - | 1.8 | - | V |
| VREFH | Reference Voltage High | - | - | 3.3 | V |
| VREFL | Reference Voltage Low | 0 | - | - | V |
| Resolution | - | - | 10 | - | Bit |
| INL | Integral Non Linearity | - | - | - | LSB |
| DNL | Differntial Non Linearity | - | - | - | LSB |

Intergral Non-linearity(INL): INL is the deviation of the input-output characteristic from the ideal transfer characteristic. It is the deviation form the line connecting zero voltage and full scale voltage. The INL for the IP is shown below and can be found [here](https://github.com/nvshinde/pDAC/tree/master/prelayout) in linearity.ods spreadsheet.

Differential Non-Linearity(DNL): DNL is the deviation between two adjacent output voltage levels that a DAC outputs. It is the maximum deviation of the output steps from the ideal output step value. The DNL for the IP is shown below and can be found [here](https://github.com/nvshinde/pDAC/tree/master/prelayout) in in linearity.ods spreadsheet.

# Open-Source EDA Tools used
### `Ngspice`
[Ngspice](http://ngspice.sourceforge.net/) is a open source circuit simulator for electronic circuits. It is a command line tool and does not offer schematic entry.

###### Steps to Install 

Go to ngspice [installation](http://ngspice.sourceforge.net/download.html)

### `Magic VLSI`
[Magic](http://opencircuitdesign.com/magic/) VLSI is a open source VLSI layout tool written at Berkeley by John Ousterhout. 

###### Steps to Install 

Go to Magic [installation](http://opencircuitdesign.com/magic/)

# Steps to clone the IP into LINUX 

Clonig a repository creates a local clone into the user's system. The files in the repository can be accessed locally. To clone follow the following steps:


`sudo apt install -y git`

`git clone https://github.com/nvshinde/pDAC.git`


# Pre-layout Simulations

The .cir files and the osu018nm tech files are available at [prelayout](https://github.com/nvshinde/pDAC/tree/master/prelayout).
Change the working directory to the directory having the IP. 

Follow the steps to run the prelayout simulations in ngspice. All the commands should be executed in terminal.

1. Change the directory to the prelayout directory location in the cloned repository `cd <repository location>`

2. Run ngspice by typing the following `ngspice` 

3. To simulate, run the netlist file `source <filename.cir>`

###### V(Out) vs time graph

![dacop](https://user-images.githubusercontent.com/62995893/90005104-5f574400-dcb4-11ea-86b8-5d5da85ccfeb.jpg)


###### V(Out) vs Digital code graph

![DACcodeoutput](https://user-images.githubusercontent.com/62995893/89973670-898e0f00-dc7e-11ea-944c-c92932b81c96.jpg)

###### INL Graph

![inlgraph](https://user-images.githubusercontent.com/62995893/89973985-70399280-dc7f-11ea-89d7-38a8c52c77a7.jpg)

###### DNL Graph

![dnlgraph](https://user-images.githubusercontent.com/62995893/89973982-6d3ea200-dc7f-11ea-83e7-28cd5f5ae088.jpg)

# Post-layout Simulations

To be added after completion of postlayout simulations

# Future Work

To be added after completion of the project

# Contact Information

Nikhil Shinde, B.E., KJSIEIT, Mumbai, shinde.nv@somaiya.edu
