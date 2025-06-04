
# Low Power Carry Select Adder (CSA) using CMOS Hybrid Full Adder

Design, simulation, and analysis of an optimized Carry Select Adder (CSA) using CMOS hybrid full adder logic. The project focuses on power efficiency, propagation delay, and area optimization by following the design using 180nm CMOS technology in Cadence Virtuoso Studio.


## Introduction

Fast and efficient addition operations are fundamental to numerous digital systems, from microprocessors to DSPs. The Carry Select Adder (CSA) is a high-performance arithmetic circuit designed to speed up addition compared to conventional designs like Ripple Carry Adders.
To address power and area inefficiencies of traditional CSAs, our implementation leverages:
- Pass transistor logic and transmission gates for full adder design
- Two 4-bit adders running in parallel for sum computation
- 2:1 Multiplexers to select the final output based on the carry
This design balances power, delay, and layout efficiency — ideal for low-power and high-speed applications in VLSI systems.

## Tools Used

### Software
- Cadence Virtuoso Studio
- Schematic design, simulation, layout generation, and performance analysis
### Technology
- 180nm CMOS process
- Targeted for low power and compact transistor-level implementation

## Setting Up the Tools

To implement and simulate the CSA in Cadence Virtuoso:
1.	Open Virtuoso Schematic Editor and create libraries for:
- Transmission Gate
- Full Adder
- 4-bit Ripple Carry Adder
- 2:1 Multiplexer
- CSA (8-bit)
2.	Use Composer to build transistor-level schematics.
3.	Run functional simulations using Analog Design Environment (ADE).
4.	Validate layout using:
- DRC (Design Rule Check)
- LVS (Layout Versus Schematic)

## Design Flow

The CSA is composed of several key building blocks:
- Transmission Gate (Reduces switching noise and leakage current).
- Hybrid Full Adder (Designed using XOR logic and multiplexers).
- 4-bit Ripple Carry Adder (Used in both lower and upper computation blocks).
- 2:1 Multiplexer (Used to select final outputs based on intermediate carry).
- 8-bit CSA (Combines the above modules. Two 4-bit adders (U0 and U1) compute assuming carry=0 and carry=1 respectively, and a MUX selects the correct sum).

### Block diagram of 8-bit Carry Select Adder
![8-bit Carry Select Adder](https://github.com/Deepthi-S-G/Implementation-of-Low-Power-and-Efficient-Carry-Select-Adder-using-CMOS-Hybrid-Full-Adder-/blob/main/CSA_Diagrams/Block%20diagram%20of%208-bit%20Carry%20Select%20Adder.png)
### Block Diagram of 4-bit Full Adder
![4-bit Full Adder](https://github.com/Deepthi-S-G/Implementation-of-Low-Power-and-Efficient-Carry-Select-Adder-using-CMOS-Hybrid-Full-Adder-/blob/main/CSA_Diagrams/Block%20Diagram%20of%204-bit%20Full%20Adder.png)
### Schematic of Full Adder
![Schematic of Full Adder](https://github.com/Deepthi-S-G/Implementation-of-Low-Power-and-Efficient-Carry-Select-Adder-using-CMOS-Hybrid-Full-Adder-/blob/main/CSA_Diagrams/Schematic%20of%20Full%20Adder.png)
### 2:1 Multiplexer
![2:1 Multiplexer](https://github.com/Deepthi-S-G/Implementation-of-Low-Power-and-Efficient-Carry-Select-Adder-using-CMOS-Hybrid-Full-Adder-/blob/main/CSA_Diagrams/21%20Multiplexer.png)

## Methodology

it represents the flow chart that explains the workflow of our project where we have implemented the Carry Select Adder in the cadence virtuoso tool and transistor-level design (Schematic diagrams). Then verification is done and the simulation results in different blocks of CSA.
![methodology block diagram](https://github.com/Deepthi-S-G/Implementation-of-Low-Power-and-Efficient-Carry-Select-Adder-using-CMOS-Hybrid-Full-Adder-/blob/main/CSA_Diagrams/Methodology.png)


## Simulation

All simulations were performed in Cadence Virtuoso. Key highlights:
### Transmission Gate
- Simulated with pulse input.
- Output closely follows input indicating correct switching behavior.
![Transmission Gate Waveform](https://github.com/Deepthi-S-G/Implementation-of-Low-Power-and-Efficient-Carry-Select-Adder-using-CMOS-Hybrid-Full-Adder-/blob/main/CSA_Diagrams/Transmission%20Gate%20Waveform.png)
![Transmission Gate Layout](https://github.com/Deepthi-S-G/Implementation-of-Low-Power-and-Efficient-Carry-Select-Adder-using-CMOS-Hybrid-Full-Adder-/blob/main/CSA_Diagrams/Transmission%20Gate%20layout.png)

### Full Adder
- Verified with waveform outputs matching truth table.
- Layout verified with DRC and LVS.

![Full Adder Waveform](https://github.com/Deepthi-S-G/Implementation-of-Low-Power-and-Efficient-Carry-Select-Adder-using-CMOS-Hybrid-Full-Adder-/blob/main/CSA_Diagrams/Full%20Adder%20Waveform.png)
![Full Adder Layout](https://github.com/Deepthi-S-G/Implementation-of-Low-Power-and-Efficient-Carry-Select-Adder-using-CMOS-Hybrid-Full-Adder-/blob/main/CSA_Diagrams/Full%20Adder%20layout.png)

### 4-bit Ripple Carry Adder

- Functional waveform confirms expected output.
- Transient simulations validate signal transitions. 

![4-bit Ripple Carry Adder Waveform](https://github.com/Deepthi-S-G/Implementation-of-Low-Power-and-Efficient-Carry-Select-Adder-using-CMOS-Hybrid-Full-Adder-/blob/main/CSA_Diagrams/4-bit%20Ripple%20Carry%20Adder%20Waveform.png)
![4-bit Ripple Carry Adder Layout](https://github.com/Deepthi-S-G/Implementation-of-Low-Power-and-Efficient-Carry-Select-Adder-using-CMOS-Hybrid-Full-Adder-/blob/main/CSA_Diagrams/4-bit%20Ripple%20Carry%20Adder%20%20layout.png)

### 2:1 MUX
- Validated using control line to switch inputs.
- Layout successful. 
![2:1 MUX Waveform](https://github.com/Deepthi-S-G/Implementation-of-Low-Power-and-Efficient-Carry-Select-Adder-using-CMOS-Hybrid-Full-Adder-/blob/main/CSA_Diagrams/21%20MUX%20schematic.png)
![2:1 MUX Layout](https://github.com/Deepthi-S-G/Implementation-of-Low-Power-and-Efficient-Carry-Select-Adder-using-CMOS-Hybrid-Full-Adder-/blob/main/CSA_Diagrams/21%20MUX%20layout.png)
#### 8-bit CSA
- Layout passed DRC and LVS.
- Final waveform shows accurate sum and carry generation.
![8-bit CSA Waveform](https://github.com/Deepthi-S-G/Implementation-of-Low-Power-and-Efficient-Carry-Select-Adder-using-CMOS-Hybrid-Full-Adder-/blob/main/CSA_Diagrams/CSA%20Waveform.png)
![8-bit CSA Waveform](https://github.com/Deepthi-S-G/Implementation-of-Low-Power-and-Efficient-Carry-Select-Adder-using-CMOS-Hybrid-Full-Adder-/blob/main/CSA_Diagrams/CSA%20Waveform%202.png)
![8-bit CSA Layout](https://github.com/Deepthi-S-G/Implementation-of-Low-Power-and-Efficient-Carry-Select-Adder-using-CMOS-Hybrid-Full-Adder-/blob/main/CSA_Diagrams/CSA%20%20layout.png)

## Performance Metrics
#### Module	Reference Power (mW) | Implemented Power (µW)
Full Adder : 24	| 92.8

CSA (8-bit) : 122 | 769.4
#### Summary
- Power: Reduced compared to standard CMOS implementations
- Area: Optimized layout using transmission gates
- Delay: Lower propagation delay due to parallelism in CSA design
## Conclusion
This project successfully implements a low-power and high-performance Carry Select Adder using CMOS hybrid full adder logic. The integration of transmission gates, efficient layout design, and Cadence-based analysis ensures this CSA is suitable for next-generation digital systems.
