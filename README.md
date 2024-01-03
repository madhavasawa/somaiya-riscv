# RISC-V Internship-cum-Course

The repository tracks all the progress for a duration of 1 month of the Internship provided by VSD (VLSI System Design) under the mentorship of Mr. Kunal Ghosh, Co-Founder, VSD.

## Contents 
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
	int i,sum = 0, n = 10;
	for (i = 1; i <=n; ++i) {
		sum += i;
	}
	printf("The sum of the number from 1 to %d is %d\n", n,sum);
	return 0;
	}
```
- To compile the above program, use the following command :
  ```
  gcc sum1ton.c
  ```
- Next, using the command below, we can get the output :
  ```
  ./a.out
  ```

  - The output of the above program is given below :
    ![Lab 1 0](https://github.com/madhavasawa/somaiya-riscv/assets/154996436/fc0d636d-f9cc-4f7f-9607-6a0a3afe4cb8)

-> Now in the case of RISC-V GNU , the following commands are executed :
- To use RISC-V gcc compiler, type
  ```
  riscv64-unknown-elf-gcc  -o <object filename.o> <filename.c>
  ```
- To List the details of a file, type
  ```
  riscv64-unknown-elf-gcc  -o <object filename.o> <filename.c>
  ```
- To deassemble the object file, type
  ```
  riscv64-unknown-elf-objdump <object file> -d <object filename.o>
  ```
- To highlight the main function
  ```
  riscv64-unknown-elf-objdump <object file> -d <object filename.o> | less
  ```
  ```
  /main
  n
  ```
  - The output for the above commands is give below (with total no of instructions)
  ![No of instr](https://github.com/madhavasawa/somaiya-riscv/assets/154996436/69f3563d-49d4-4e6c-bd8c-7b1e28172862)

</details>

<details> 
<summary> Integer Number Representation </summary>
- 64-bit Number System for Unsigned Numbers

![positive nos](https://github.com/madhavasawa/somaiya-riscv/assets/154996436/3b8a5c06-ad1e-4eea-b9ce-3dcc00a36c64)

- 64-bit Number System for Signed Numbers
   
![all nos](https://github.com/madhavasawa/somaiya-riscv/assets/154996436/7c44e57b-08ee-4f4f-a98b-0714ca3f5995)

-> The basic code to find the Highest Unsigned number possible in the 64-bit system is as follows
```
#include <stdio.h>
#include <math.h>

int main()
{
unsigned long long int max = (unsigned long long int)(pow(2,64)-1);
printf("Highest Number represented by unsigned long long int is %llu \n", max);
return 0;
}
```
- The output for the same is :
![unsigndHigh](https://github.com/madhavasawa/somaiya-riscv/assets/154996436/d4ef2265-2fc3-418f-aae0-5ea4e53cb246)

-> The basic code to find the Highest and Smallest number possible in the 64-bit system is as follows
```
#include <stdio.h>
#include <math.h>

int main()
{
  long long int max = (long long int)(pow(2,64)-1);
  long long int min = (long long int)(pow(2,64)*-1);
  printf("Highest Number represented by signed long long int is %llu \n", max);
  printf("Lowest Number represented by signed long long int is %llu \n", min);
  return 0;
}
```
- The output for the same is
  ![HighLow](https://github.com/madhavasawa/somaiya-riscv/assets/154996436/99ebdd83-f87f-4a99-906a-619cd6d614d0)

</details>



### Day 2 :
<details>
<summary> Application Binary Interface (ABI) </summary>
-> Application Binary Interface (ABI) defines how software components interact at a binary level, ensuring compatibility across different compilers, platforms, and architectures. It specifies the conventions for function calls, data structures, and system calls, enabling interoperability between software modules and facilitating communication between programs at a low-level binary interface.
	
</details>

<details>
<summary> Lab Work using ABI function calls </summary>
</details>

<details>
<summary> Basic Verification flow using iverilog </summary>
</details>
