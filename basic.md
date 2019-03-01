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
![](https://i.imgur.com/EOHOjuw.png)
## BASYS 3 Configuration
The seven-segment LED display on the BASYS-3 board is already connected to several pins on the XC7A35T1CPG236C FPGA. The pin assignments are shown in Table 1. You will have to tell Xilinx Vivado that the seven outputs of your schematic ‘a’ through ‘g’ should be mapped to these pins. Similarly, the three inputs to your schematic will be mapped to Switches, which are connected to the FPGA pins as shown in Table 2.
## Assigning Pins
1. **Add Sources** under **Flow Navigator** pane. **Add Constraints**, then click **Next**. THen click on **create file** option. Under **File Name**, click **ok** and **finished**. Encounter **pins.xdc** file, 
2. In top level Verilog File under **sources** pane and click on **Run Synthesis**. In **Launch Runs**, keep default settings and click **cancel**
3. Click on **Open Elaborated Design**. A window appears, click **OK**. In **Layout -> I/O Plannin**. THis creates a new tab called **I/O Ports** next to Console Window. Expand Scalar ports and you will see all the inputs and outputs of your desifn. 
4. **Package Pin**. Assign pics. Hit **Enter** to save changes. Check next to that pin under colunn "Oin"
5. Under **I/O STD** change to **LVCMOS33**. 
6. Save as existing file. Close **Elaborated Design** window. 
7. **Generate Bitstream** to create the bitstream. Once the bitstream generated. Launch Runs Window, click on Ok. 
## Using Diligent 
1. Start -> Programs -> Digilent -> Adept 
2. Find the bit file and select **program*

![](https://i.imgur.com/vsHh0nj.png)
![](https://i.imgur.com/QpEVjc7.png)
![](https://i.imgur.com/Oahm1CI.png)
![](https://i.imgur.com/q1E4Ix9.png)
![](https://i.imgur.com/2svo4Ne.png)
![](https://i.imgur.com/1ciMEi9.png)
![](https://i.imgur.com/PWrv3gB.png)
![](https://i.imgur.com/hg1yWkB.png)
![](https://i.imgur.com/uu1VcXP.png)
