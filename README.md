# VSD Hardware Design Program  

## ChipCraft Installation and Usage Guide  

### 📚 Contents

  - [Steps to Install ChipCraft and Run GUI](#steps-to-install-chipcraft-and-run-gui)
    - [1. Clone the ChipCraft Repository](#1-clone-the-chipcraft-repository)
    - [2. Setup Dependencies](#2-setup-dependencies)
    - [3. Build ChipCraft](#3-build-chipcraft)
    - [4. Verify the Installation](#4-verify-the-installation)
    - [5. Run a Sample Design Flow](#5-run-a-sample-design-flow)
    - [6. Launch the Graphical Interface](#6-launch-the-graphical-interface)
  - [Directory Structure and File Organization](#directory-structure-and-file-organization)

---

**ChipCraft** is an open-source digital design automation (EDA) framework that automates front-end to back-end IC implementation.  
It integrates synthesis, floorplanning, placement, routing, and timing closure into a single modular environment.  
Ideal for VLSI learners and researchers who want to explore open hardware design.

---

### `Steps to Install ChipCraft and Run GUI`

### 1. Clone the ChipCraft Repository

```bash
git clone --recursive https://github.com/vsdprogram/ChipCraft
cd ChipCraft
```

---

### 2. Setup Dependencies

Before building, ensure all dependencies are installed.

```bash
sudo ./install_deps.sh
```

---

### 3. Build ChipCraft

Once dependencies are installed, build the main environment:

```bash
./build_chipcraft.sh
```

📸 Example Output  
![Alt Text](Images/setup_step2.jpg)

---

### 4. Verify the Installation

Source the environment and check if the tools run correctly:

```bash
source ./env.sh
chipcraft --version  
chiprun --help
```



---

### 5. Run a Sample Design Flow

To test your setup, execute a demo design flow:

```bash
cd examples/demo_flow
make run
```

📸 Example Output  
![Alt Text](Images/setup_step4.jpg)

---

### 6. Launch the Graphical Interface

Visualize your layout results using the built-in GUI:

```bash
make gui_view
```


✅ **Installation Complete!**  
You’re ready to explore the full RTL-to-GDSII flow with ChipCraft 🚀  

---

## `Directory Structure and File Organization`

ChipCraft/

```plaintext
├── ChipCraft
│   ├── bin              -> Executable binaries for ChipCraft tools
│   ├── config           -> Configuration files and global settings
│   ├── docs             -> Documentation and tutorials
│   ├── examples         -> Built-in design examples for testing
│   ├── flow             -> Design flow scripts for synthesis and layout
│   ├── libs             -> Technology libraries (LEF/DEF/GDS)
│   ├── scripts          -> Utility and automation scripts
│   ├── setup_env.sh     -> Environment setup script for tool execution
│   ├── install_deps.sh  -> Dependency installer for required packages
│   └── build_chipcraft.sh -> Script to compile and build ChipCraft
```

Inside the `flow/` directory:

```plaintext
├── flow
│   ├── designs          -> Example design files for various nodes
│   ├── platforms        -> Technology-specific setup files
│   ├── makefile         -> Automated flow control script
│   ├── reports          -> Timing, power, and area analysis results
│   ├── scripts          -> TCL and Python-based automation utilities
│   └── utils            -> Helper tools and custom commands
```
and update the commands or image na
