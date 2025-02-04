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




After successful completion of the synthesis we navigate to the reports folder of this specific run (25-01_23-16) and inspect the Yosys stats report file:






