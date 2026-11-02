# Creating a VHDL Project in Xilinx ISE 9.1i

## Project Setup Procedure

The following steps describe how to create, configure, simulate, and implement a VHDL project using Xilinx ISE 9.1i.

### 1. Launch Xilinx ISE (Optional)

Open the terminal and execute:

```bash
source /home/vibhu/Xilinx91i/settings.sh
ise
```

This loads the Xilinx environment and launches Project Navigator.

### 2. Create a New Project

1. Open **File → New Project**.
2. Enter the project name.
3. Select the project directory.
4. Click **Next**.

### 3. Configure Project Settings

Configure the FPGA device and project settings as follows:

| Parameter | Configuration |
|---|---|
| Family | Spartan3E |
| Device | XC3S250E |
| Package | CP132 |
| Speed Grade | -4 |
| Top-Level Source Type | HDL |
| Synthesis Tool | XST (VHDL/Verilog) |
| Simulator | ISim (VHDL/Verilog) |
| Preferred Language | VHDL |

Click **Next → Finish** to create the project.

### 4. Create a VHDL Module

1. Navigate to **Project → New Source**.
2. Select **VHDL Module**.
3. Enter the module name.
4. Define the required input and output ports.
5. Click **Next → Finish**.

### 5. Write the VHDL Code

1. Open the generated `.vhd` file.
2. Write or paste the required VHDL program.
3. Save the file using `Ctrl + S`.

### 6. Check Syntax

1. Select the main VHDL source file.
2. Expand **Synthesize - XST** in the Processes panel.
3. Double-click **Check Syntax**.
4. Verify that no syntax errors are reported.

### 7. Create a Testbench

1. Navigate to **Project → New Source**.
2. Select **VHDL Test Bench**.
3. Enter the testbench name.
4. Associate it with the corresponding VHDL module.
5. Click **Next → Finish**.
6. Add the testbench code and save the file.

### 8. Run Behavioral Simulation

1. Change the Sources panel selection from **Implementation** to **Behavioral Simulation**.
2. Select the testbench module.
3. Expand the Processes panel.
4. Double-click **Simulate Behavioral Model**.
5. Observe the input and output waveforms in the simulator.

### 9. Synthesize and Implement the Design

Switch the Sources panel back to **Implementation**.

Execute the following processes:

1. Check Syntax.
2. Synthesize - XST.
3. Implement Design:
   - Translate
   - Map
   - Place & Route

Verify that the implementation completes successfully without errors.

---

## Overall Workflow

```text
Create New Project
       |
Configure FPGA Device
       |
Create VHDL Module
       |
Write VHDL Code
       |
Check Syntax
       |
Create Testbench
       |
Behavioral Simulation
       |
Synthesis
       |
Implementation
       |
Place & Route
       |
     Done
```

## Tools and Technologies

- **HDL:** VHDL
- **Design Software:** Xilinx ISE 9.1i
- **Simulator:** ISim
- **Synthesis Tool:** XST
- **Target FPGA:** Spartan3E XC3S250E
- **Operating System:** Linux Mint

## Note

The testbench is used to verify the functional behavior of the design through simulation. It is not required for synthesis or FPGA implementation.
