# RISC-V Internship-cum-Course

The repository tracks all the progress for a duration of 1 month of the Internship provided by VSD (VLSI System Design) under the mentorship of Mr. Kunal Ghosh, Co-Founder of VSD.

## Contents :
- Introduction to RISC-V ISA and GNU Compiler Toolchain
- Intoduction to ABI (Application Binary Interface) and Basic Error Flow
## Day-wise Progress

### Day 0 : 
<details>
<summary>Installation of Ubuntu System (Using Virtual Box and vsdsquadron.vdi)</summary>
  -> Steps to install the System

1. Download the vsdsquadron file from the given link.
2. Next download the Virtual Box from the website and install the Virtual Box.
3. Setup the virtual Machine
4. While on the wizard of "Selecting Virtual Disk", select the location of the downloaded vsdsquadron.vdi file.
5. Finally provide the required space and processor value and finish the setup.
6. Run the Virtual Machine.

![Screenshot 2023-12-28 121708](https://github.com/madhavasawa/somaiya-riscv/assets/154996436/0d911aa5-f855-466f-9253-9802be61d2c1)
</details>

### Day 1 : Introduction to RISC-V ISA and GNU Compiler Toolchain
<details>
<summary> Introduction to RISC-V Basic Keywords </summary>
-> The RISC-V ISA (Instruction Set Architecture) stands out for its simplicity, with fixed-length instructions and a clean design. This simplicity aids in ease of understanding, implementation, and optimization. RISC-V's open-source nature enables a collaborative community, leading to continuous refinement, standardization, and the development of a rich software ecosystem. This openness empowers engineers to tailor processors to specific needs, from embedded systems to high-performance computing. Its royalty-free model fosters widespread adoption, making RISC-V a compelling choice for both academia and industry.

  The different instructions included in RISC-V are listed below:
  
1. Pseudo instructions - For e.g- mv,li,ret etc
2. Base integer instruction (RV64I, RV32I)-For e.g-lui,addi etc
3. Multiply extension (RV64M) -For e.g- mulw,divw etc
4. Single and double floating point instruction (RV64F, RV64D) -For e.g- flw,fadd etc
5. Application binary instruction
6. Memory allocation and stack pointer
</details>

<details> 
<summary> Labwork for RISC-V Software Toolchain</summary>
-> To start with, we first try the basic C-Program to find the sum of numbers from 1 to n
The code for the same is :
  
```
#include <stdio.h>
int main () {
	int i,sum = 0, n = 6;
	for (i = 1; i <=n; ++i) {
		sum += i;
	}
	printf("The sum of the number from 1 to %d is %d\n", n,sum);
	return 0;
	}
```
</details>

<details> 
<summary> Integer Number Representation </summary>
</details>
