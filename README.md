# Soc-Design-Planning
Repository for the workshop "Digital VLSI SoC Design and Planning"
## Lab Day 1 : Inception of open-source EDA, OpenLANE and Sky130 PDK
The objective is to perform the synthesis of the 'picorv32a' design and calculate the resulting flop ratio.

The first 5 steps are the following:
```bash
  # Step 1: Change directory to the OpenLANE flow directory within the OpenLANE working directory
  $ cd Desktop/work/tools/openlane_working_dir/openlane

  # Step 2: Execute the aliased 'docker' command to access the bash
  $ docker

  # Step 3: Start OpenLANE in interactive mode
  %./flow.tcl -interactive

 # Step 4: Load the required packages
  %package require openlane 0.9

 # Step 5: Prepare the 'picorv32a' design for synthesis
  %prep -design picorv32a
```
<img width="641" alt="1" src="https://github.com/user-attachments/assets/114aff47-677e-40ee-823a-1b462ed9c85e" />
```

<img width="631" alt="3" src="https://github.com/user-attachments/assets/caa2fde5-e1de-461a-84ba-ebf579719acf" />

At this point the synthesis can be started:
```bash
  # Step 6: Run the synthesis
  %run_synthesis
```
<img width="640" alt="yosys" src="https://github.com/user-attachments/assets/e3743ecc-a10f-4fc2-bf33-b3a07d39fb4a" />


<img width="629" alt="d filp flp" src="https://github.com/user-attachments/assets/0e4be3ce-c70c-4039-8274-379fb4bbf3fd" />

## Lab Day 2 : Good floorplan VS bad floorplan and introduction to library cells

The objectives are the following:

1) Define the floorplan using the floorplan utility from OpenLANE
2) Review the floorplan output files and calculate the die area
3) Review the floorplan in Magic
4) Perform congestion-aware placement using RePlAcE 
5) Review the placement in Magic

#### 1  Define the floorplan using the floorplan utility from OpenLANE

We run the floorplan utility from OpenLANE to define the floorplan of the picorv32a design:

```bash
  #Define the floorplan
  %run_floorplan
```
<img width="912" alt="floor plan" src="https://github.com/user-attachments/assets/2c99b411-af25-4a6a-b40f-c23a0729d0a6" />

#### 2  Review the floorplan output files and calculate the die area

<img width="634" alt="set env after" src="https://github.com/user-attachments/assets/f1bccc65-1dac-4f79-b0cd-32a53a12a6ff" />


