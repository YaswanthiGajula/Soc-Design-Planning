# Soc-Design-Planning
Repository for the workshop "Digital VLSI SoC Design and Planning"
## Lab Day 1 : Inception of open-source EDA, OpenLANE and Sky130 PDK
```bash

  $ cd Desktop/work/tools/openlane_working_dir/openlane

  
  $ docker

  
  %./flow.tcl -interactive

   %package require openlane 0.9

 
  %prep -design picorv32a
```
<img width="641" alt="1" src="https://github.com/user-attachments/assets/114aff47-677e-40ee-823a-1b462ed9c85e" />
```

<img width="631" alt="3" src="https://github.com/user-attachments/assets/caa2fde5-e1de-461a-84ba-ebf579719acf" />



  %run_synthesis





###Lab Day 2 : Good floorplan VS bad floorplan and introduction to library cells

### opening the terminal

<img width="641" alt="1" src="https://github.com/user-attachments/assets/26633c27-465c-4f77-9d16-56e53cff6c57" />

<img width="631" alt="3" src="https://github.com/user-attachments/assets/dba71224-14b1-43f3-8d9e-e12a01dced94" />

###picorv32a

<img width="634" alt="5" src="https://github.com/user-attachments/assets/136971d0-9bed-4b33-b054-87f7b5b09218" />


<img width="631" alt="6" src="https://github.com/user-attachments/assets/4d127aab-cde0-4d72-8052-6ff4b2af9187" />


<img width="601" alt="7" src="https://github.com/user-attachments/assets/866137e0-bb39-48cd-b9fd-5bb71afe982a" />

<img width="638" alt="9" src="https://github.com/user-attachments/assets/789cde9b-db5d-43da-83c5-6c9c286db19d" />

<img width="776" alt="10" src="https://github.com/user-attachments/assets/60be40ae-4e35-41fa-9f5d-813e892f1980" />





  %run_floorplan

```
<img width="912" alt="floor plan" src="https://github.com/user-attachments/assets/2c99b411-af25-4a6a-b40f-c23a0729d0a6" />



<img width="634" alt="set env after" src="https://github.com/user-attachments/assets/f1bccc65-1dac-4f79-b0cd-32a53a12a6ff" />

<img width="644" alt="di area" src="https://github.com/user-attachments/assets/659e1464-ab8b-4250-8dda-6b2a3f3e5210" />




```bash 
  $ magic -T /home/vsduser/Desktop/work/tools/openlane_working_dir/pdks/sky130A/libs.tech/magic/sky130A.tech lef read ../../tmp/merged.lef def read picorv32a.floorplan.def &
```

<img width="932" alt="magict floor cmd" src="https://github.com/user-attachments/assets/bdff98a2-238c-4093-a188-8df12a579eb2" />

<img width="639" alt="io pins placed" src="https://github.com/user-attachments/assets/f1af7d91-de04-4dfd-b3c9-f9112b754116" />

<img width="636" alt="nmos what" src="https://github.com/user-attachments/assets/574b3075-36c0-4713-bf81-7ab747450f49" />


```bash
 
  %run_placement
```
<img width="928" alt="placement report" src="https://github.com/user-attachments/assets/c0aa76ca-0276-4b7c-9374-40e62abf84d0" />

####  Magic


```bash 
  $ magic -T /home/vsduser/Desktop/work/tools/openlane_working_dir/pdks/sky130A/libs.tech/magic/sky130A.tech lef read ../../tmp/merged.lef def read picorv32a.placement.def &
```
<img width="923" alt="placement pic" src="https://github.com/user-attachments/assets/6b5a7c5f-2802-4e09-8b23-40833e57b278" />

<img width="926" alt="placement zoom pic" src="https://github.com/user-attachments/assets/2887f496-aac5-4142-89ee-a8bb6503cba2" />

## Lab Day 3 : Design library cell using Magic Layout and ngspice characterization

<img width="928" alt="placement report" src="https://github.com/user-attachments/assets/6f47dad0-5e5e-48e6-a210-e5c9185f319c" />

<img width="722" alt="magic t floorplan" src="https://github.com/user-attachments/assets/6fb665b8-180a-46b7-bc33-3536b6ffcf32" />

#### 2 Clone CMOS inverter standard cell design from repository

The necessary steps and commands are the following:

```bash
  #Step 1: Change directory to the OpenLANE flow directory within the OpenLANE working directory
  $ cd Desktop/work/tools/openlane_working_dir/openlane

  #Step 2: Clone the repository with the inverter cell design
  $ git clone https://github.com/nickson-jose/vsdstdcelldesign.git

  #Step 3: Check that the cloned files are in the intended destination
  $ ls -ltr
```
<img width="776" alt="10" src="https://github.com/user-attachments/assets/7e63258a-b5a5-4d0b-8752-3524d9bde226" />

<img width="632" alt="source ofthe pmos to vdd line" src="https://github.com/user-attachments/assets/43fd9079-2473-4c2c-a60e-ab13c88e9063" />



<img width="646" alt="12" src="https://github.com/user-attachments/assets/9cb9fc9e-d176-4e6e-9d7d-da5a42e3b480" />



<img width="641" alt="18" src="https://github.com/user-attachments/assets/3bfaafba-1d8d-4df4-b66e-d1b91fc25d7d" />

<img width="637" alt="corrected inverter op" src="https://github.com/user-attachments/assets/c6a2aba3-934f-4eb4-be09-c1de05fa622a" />

<img width="651" alt="two lines" src="https://github.com/user-attachments/assets/b99212f5-b498-408f-aca0-6a830bd75302" />

















