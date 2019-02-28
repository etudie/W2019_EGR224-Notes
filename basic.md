[Creating a new project](#vivado-introduction)

[Adding schematic comp lib](#vivado-introduction)

[Create Block Design Schematic ](#vivado-introduction)

[Create HDL Wrapper ](#vivado-introduction)

[Compile Project via Sythesis](#vivado-introduction)

[Simulation of Stimulus (TestBench)](#vivado-introduction)


## Vivado Introduction 
**Vivado 2017.2** is a program from Xilinx that supports digital circuit design and simulation.
- Basic steps of creating a digital circuit schematic
- Create digital waveform stimulus for the circuit
- Simulate circuit operations using digital waveform stimulus

## Creating a new project 
![](https://i.imgur.com/HIodvFO.png)
#### 1. Select Vivado 2018.2 and create new project.
- Create subdirectory 
- Select RTL
- Select **Basys3** as Board 

## Adding schematic comp lib 
![](https://i.imgur.com/pVib84V.png)
1. Add **Xilinx/XUP_LIB**

## Create Block Design Schematic 
![](https://i.imgur.com/gVVRXuV.png)
1. Create Block Design, add blocks, save 
2. Make **External** vs **Port**
3. Set Propogation to Zero

## Create HDL Wrapper 
![](https://i.imgur.com/fydGjdR.png)
1. In sources, right click on design file and **create HDL wrapper**. 
* This instantiates the modules and generates a 'read-only' file of the blocks used. 

## Compile Project via Sythesis
![](https://i.imgur.com/NDBTiIF.png)

1. Click **cancel** when sythesis complete

## Simulation of Stimulus (TestBench)
In the **Design Module** Window, we list the inputs and outputs
1. Select **Add or Create Simulation**
2. **Define Module**
![](https://i.imgur.com/S52gvZs.png)

## Add simulation sources 
1. Edit the testbench file

| code | explanation |
|----------|:-------------:|
| 'timescale | set time increments |
| reg | input variable |
| wire | output variable | 
| #20 | hold command for 20 time steps | 
| initial begin | begins | 
| end | ends the block since initial begin | 
| always | doesn't rely on initial begin | 
| initial #1000 $finish | ends after 1000 cycles | 
| endmodule | end of testbench file | 

![](https://i.imgur.com/7BPSKwS.png)
![](https://i.imgur.com/Oahm1CI.png)
## Troubleshooting
