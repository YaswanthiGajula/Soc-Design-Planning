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

<img width="644" alt="di area" src="https://github.com/user-attachments/assets/659e1464-ab8b-4250-8dda-6b2a3f3e5210" />

#### 3 Review the floorplan in Magic

In the same location as in the previous point, we run the following command to execute Magic, providing the paths to the .tech, .lef and .def files:

```bash 
  $ magic -T /home/vsduser/Desktop/work/tools/openlane_working_dir/pdks/sky130A/libs.tech/magic/sky130A.tech lef read ../../tmp/merged.lef def read picorv32a.floorplan.def &
```

<img width="932" alt="magict floor cmd" src="https://github.com/user-attachments/assets/bdff98a2-238c-4093-a188-8df12a579eb2" />

<img width="639" alt="io pins placed" src="https://github.com/user-attachments/assets/f1af7d91-de04-4dfd-b3c9-f9112b754116" />

Once Magic opens, hitting S allows to select and inspect cells at different zoom levels:

<img width="636" alt="nmos what" src="https://github.com/user-attachments/assets/574b3075-36c0-4713-bf81-7ab747450f49" />

#### 4 Perform congestion-aware placement using RePlAcE

We run the placement utility from OpenLANE with the following command:

```bash
  #Perform congestion-aware placement
  %run_placement
```
<img width="928" alt="placement report" src="https://github.com/user-attachments/assets/c0aa76ca-0276-4b7c-9374-40e62abf84d0" />

#### 5 Review the placement in Magic

To review the placement we navigate to the results folder of this specific run (28-01_20-56) and execute the command to launch Magic, 

```bash 
  $ magic -T /home/vsduser/Desktop/work/tools/openlane_working_dir/pdks/sky130A/libs.tech/magic/sky130A.tech lef read ../../tmp/merged.lef def read picorv32a.placement.def &
```
<img width="923" alt="placement pic" src="https://github.com/user-attachments/assets/6b5a7c5f-2802-4e09-8b23-40833e57b278" />

