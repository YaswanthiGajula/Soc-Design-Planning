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





### Lab Day 2 : Good floorplan VS bad floorplan and introduction to library cells

### opening the terminal

<img width="641" alt="1" src="https://github.com/user-attachments/assets/26633c27-465c-4f77-9d16-56e53cff6c57" />

<img width="631" alt="3" src="https://github.com/user-attachments/assets/dba71224-14b1-43f3-8d9e-e12a01dced94" />


### picorv32a


<img width="634" alt="5" src="https://github.com/user-attachments/assets/136971d0-9bed-4b33-b054-87f7b5b09218" />


<img width="631" alt="6" src="https://github.com/user-attachments/assets/4d127aab-cde0-4d72-8052-6ff4b2af9187" />


<img width="601" alt="7" src="https://github.com/user-attachments/assets/866137e0-bb39-48cd-b9fd-5bb71afe982a" />

<img width="638" alt="9" src="https://github.com/user-attachments/assets/789cde9b-db5d-43da-83c5-6c9c286db19d" />

<img width="776" alt="10" src="https://github.com/user-attachments/assets/60be40ae-4e35-41fa-9f5d-813e892f1980" />





  %run_floorplan


<img width="912" alt="floor plan" src="https://github.com/user-attachments/assets/c5c16278-52ce-4cb7-b1e4-a3aeb2b02646" />




<img width="634" alt="set env after" src="https://github.com/user-attachments/assets/f1bccc65-1dac-4f79-b0cd-32a53a12a6ff" />

<img width="644" alt="di area" src="https://github.com/user-attachments/assets/659e1464-ab8b-4250-8dda-6b2a3f3e5210" />




```bash 
  $ magic -T /home/vsduser/Desktop/work/tools/openlane_working_dir/pdks/sky130A/libs.tech/magic/sky130A.tech lef read ../../tmp/merged.lef def read picorv32a.floorplan.def &
```

<img width="932" alt="magict floor cmd" src="https://github.com/user-attachments/assets/bdff98a2-238c-4093-a188-8df12a579eb2" />

<img width="639" alt="io pins placed" src="https://github.com/user-attachments/assets/f1af7d91-de04-4dfd-b3c9-f9112b754116" />



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
<img width="637" alt="git clone" src="https://github.com/user-attachments/assets/cb7e89c4-cf5b-497e-b5b8-78cc7e2e7d0d" />

<img width="637" alt="vsd path" src="https://github.com/user-attachments/assets/edd50f2c-bb80-4035-beaf-951d85a501be" />

<img width="637" alt="pmos what" src="https://github.com/user-attachments/assets/6b276b22-b048-48ad-bbae-4e80a37e50ae" />

<img width="631" alt="extracting spice" src="https://github.com/user-attachments/assets/6b7d5dec-3a46-4d18-81f5-ef21490cb032" />

<img width="632" alt="source ofthe pmos to vdd line" src="https://github.com/user-attachments/assets/43fd9079-2473-4c2c-a60e-ab13c88e9063" />

<img width="639" alt="spice extraction in cmd prompt" src="https://github.com/user-attachments/assets/1a256993-aadc-47f2-b389-738270b35cf2" />

<img width="644" alt="sky130_inv_spice" src="https://github.com/user-attachments/assets/2fa81b08-035a-4e0e-848b-86dbf235a642" />

<img width="633" alt="spice file" src="https://github.com/user-attachments/assets/077eb990-8b80-4264-8e2c-174680e479d1" />


<img width="646" alt="12" src="https://github.com/user-attachments/assets/9cb9fc9e-d176-4e6e-9d7d-da5a42e3b480" />

<img width="641" alt="18" src="https://github.com/user-attachments/assets/3bfaafba-1d8d-4df4-b66e-d1b91fc25d7d" />

<img width="637" alt="corrected inverter op" src="https://github.com/user-attachments/assets/c6a2aba3-934f-4eb4-be09-c1de05fa622a" />

<img width="651" alt="two lines" src="https://github.com/user-attachments/assets/b99212f5-b498-408f-aca0-6a830bd75302" />

### Tech lab
<img width="633" alt="spice file" src="https://github.com/user-attachments/assets/57517388-564e-4752-8041-e67ba68281fe" />

<img width="643" alt="2" src="https://github.com/user-attachments/assets/c286c754-561f-46aa-986e-f2626810ee7f" />

<img width="649" alt="3" src="https://github.com/user-attachments/assets/82269f30-c4a9-40b3-b921-7444ac3fc5d0" />

<img width="646" alt="4" src="https://github.com/user-attachments/assets/e1511557-e119-415b-8eea-87f7ec4bf6e9" />

<img width="642" alt="5" src="https://github.com/user-attachments/assets/a838a46b-8ae9-418f-9086-23e795f895c9" />

<img width="637" alt="6" src="https://github.com/user-attachments/assets/bb7d3942-7dd7-49f4-ace5-6ec4c84ebf49" />

<img width="634" alt="8" src="https://github.com/user-attachments/assets/57bce72f-4286-4a8f-94e8-6bcc01961627" />

<img width="638" alt="9" src="https://github.com/user-attachments/assets/533c9cd7-bc46-4e0b-ae82-791fea3026ae" />

<img width="637" alt="10" src="https://github.com/user-attachments/assets/146e1345-8e67-44b0-a26a-54dd2dc433c9" />

<img width="644" alt="11" src="https://github.com/user-attachments/assets/283ca7f4-3d12-40b0-85e5-3efbaf77c382" />

<img width="638" alt="12" src="https://github.com/user-attachments/assets/e9126e85-01c8-4d2c-a00f-fdfeb195b608" />

<img width="638" alt="13" src="https://github.com/user-attachments/assets/87290ef5-901a-4cfd-8d5f-bc4b0a7d6892" />

<img width="626" alt="14" src="https://github.com/user-attachments/assets/d7b10956-9230-4326-9278-ea65c08ed83c" />

<img width="641" alt="15" src="https://github.com/user-attachments/assets/36ba6f51-5b1a-4393-b2ac-e324f152cca8" />

<img width="637" alt="16" src="https://github.com/user-attachments/assets/ae83f8f8-2a5b-4123-8237-cdc984484bba" />

### Day 4

<img width="637" alt="1" src="https://github.com/user-attachments/assets/3bad19bd-701d-455a-8de8-6b16d2665d3e" />

<img width="637" alt="2" src="https://github.com/user-attachments/assets/0ba0c814-6bc4-43e6-ae00-1f8f9e796713" />

 <img width="633" alt="3" src="https://github.com/user-attachments/assets/dca6b0cf-6a57-4797-8c37-c0df6b591803" />

<img width="644" alt="4" src="https://github.com/user-attachments/assets/4fa3f08e-c8a4-476d-81e5-53863214abc7" />

<img width="631" alt="5" src="https://github.com/user-attachments/assets/db1757f3-a00d-419f-ba4a-0c8a2e7d0623" />

<img width="638" alt="6" src="https://github.com/user-attachments/assets/06617341-8963-4dcb-8b00-9c834ca4fa44" />

<img width="656" alt="7" src="https://github.com/user-attachments/assets/da7092bf-7248-401f-847b-f0bdf06e1b53" />

<img width="639" alt="8" src="https://github.com/user-attachments/assets/51161460-7094-4dab-82e3-14f953747265" />

<img width="650" alt="9" src="https://github.com/user-attachments/assets/ce7c0ff7-7439-45a7-ad5f-34b768756e60" />

<img width="638" alt="10" src="https://github.com/user-attachments/assets/7b7244bb-fbba-4915-b021-95a013d455a3" />

<img width="639" alt="11" src="https://github.com/user-attachments/assets/0fa12fa1-c8a3-48ea-ba3f-0513b7472b69" />

<img width="638" alt="12" src="https://github.com/user-attachments/assets/f39ff29b-63e9-4716-9f96-aff2596a1ca3" />

<img width="670" alt="14" src="https://github.com/user-attachments/assets/126aed74-9806-4884-9447-661f20f30ede" />

<img width="665" alt="15" src="https://github.com/user-attachments/assets/f839fb0d-0be5-430d-be96-9f9809b07adc" />

<img width="636" alt="16" src="https://github.com/user-attachments/assets/2da56739-fe6c-4dc1-936f-27dda60147d0" />

<img width="641" alt="17" src="https://github.com/user-attachments/assets/c27b3f1f-23d6-4dcc-baf1-3588cd06ef57" />

<img width="640" alt="18" src="https://github.com/user-attachments/assets/53dfff60-fafa-41c7-9a13-62d0f01baaa7" />

<img width="644" alt="19" src="https://github.com/user-attachments/assets/280f8c8b-b02b-4748-ae0d-c9411dbea380" />

<img width="648" alt="20" src="https://github.com/user-attachments/assets/d5dacf22-ab1c-46e3-a7e8-ad3def3fd0ac" />

<img width="923" alt="placement pic" src="https://github.com/user-attachments/assets/c2e33b59-c4cb-4da7-bf10-4544147eb380" />

