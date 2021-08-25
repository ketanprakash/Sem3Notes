# Computer Organization and Architecture

## 2021-08-13

### Computer Architecture

> What makes one computer faster/more performant than other?
> Architectural differences make one computer faster/more performant than other.

> What is Computer Architecture?
> Computer Architecture deals with the funcational behaviour of a computer system and its optimization for a task for which is to be used.  

* Deals with the **functional behaviour** of a computer system.

* To provide **optimum performance** in the context of the uses to which it will be put. 

* Can be seen as a **constraint** optimization problem. This contraint can be **cost**, **system size**, **thermal/mechanical durability**, etc.

* Constaints are made concrete by a set of **performance indicators**. Eg : Processing speed, Graphics speed, etc. 

### Computer Organization

<!-- * Computer organization deals with the implementation of computer architecture at a hardware.  -->

* Computer Organization can be seen as a microarchitecture (logic/hardware implementation)

## 2021-08-16
#### Performance Metrics
1. MIPS(Millions of instructions per second): 
<img height = 40 src="https://render.githubusercontent.com/render/math?math=\frac{\text{No of instructions executed in running a program}}{\text{Time required to run the program}}">


(Number of instructions executed per second)
> Note: MIPS is not commonly used because it does not tell us anything about the architecture

2. CTI/IPC: Cycles per instruction(CPI)/Instructions per Cycle(IPC):

<!-- * CPI: <font size = 4>$\frac{\text{No of clock cycles required to execute the program}}{\text{No of instructions executed in running the program}}$</font>  -->

* CPI: 

<img height = 40 src="https://render.githubusercontent.com/render/math?math=\frac{\text{No of clock cycles required to execute the program}}{\text{No of instructions executed in running the program}}">

  
(Number of clock cycles required to execute one instruction)

* IPC: 1/CPI or (Number of instructions executed in one cycle)

* High IPC: The reference program took fewer cycles 
* High CPI: The reference program took more cycles

Eg: Program consists of 100 instruction loop executed 42 times. If it takes 16000 cycles to execute the program, what are its cpi and ipc values for the program?

Total number of instructions = 100 * 42 = 4200
No of cycles taken = 16000
CPI = 16000/4200 = 80/21 = 3.8
IPC = 21/80 = 0.26

> Note CPI and IPC are rarely used to compare actual computer systems because it cannot tell the amount of time required to execute the program as the system's clock speed is not avaiable

3. Speed Up: 
Describes how the performance of an architecture changes as different improvements are made to the architecture.

<img height = 35 src="https://render.githubusercontent.com/render/math?math=\text{Speed up} = \frac{\text{Execution time before}}{\text{Execution time after}}">

Eg: A program takes 25 seconds to run on machine 1 of second architecture and the same program takes 15s to run of machine 2 of another architecture? 
Speed Up = 25/15 = 1.67 times

4. Amdahl's law: 

<img height = 35 src="https://render.githubusercontent.com/render/math?math=\text{Execution time new = }\text{(Execution time old)} * (\text{Fraction unused} \space \space %2B \space \frac{\text{fraction used}}{\text{Speed Up used}})">

fraction of unused = fraction of time improvement is not used

fraction used = fraction of time imporvement is used

speed up used = speed up achieved when improvement is used

<img height = 35 src="https://render.githubusercontent.com/render/math?math=\text{Speed up} = \frac{\text{Old Execution time}}{\text{New Execution time}}">

Eg: 1998 version of a comp executes a program in 200sec. 2000 computer executes in 150sec

speed up = 200/150 = 1.33

Eg: To achieve a speed up of 3 of a program that originally took 78s to execute, what must be the execution time of the program of the program be reduced to?

new execution time = 78/3 = 26

5. Benchmark Programs
Suite of typical programs that are tested on the programs. Eg: SPECviewperf(by SPEC), Cinebench(by Maxxon), etc. 

## 2021-08-18

Ex: A computer architect is desigining a mem system for the next version of a processor. If the current version of the processor spends 40% of its time processing memory, by how much speed up the memory system must achieve an overall speed up of 1.2?

Solution: 
fraction used = 0.4
fraction unused = 0.6
req speed up overall = 1.2021
speed up = 1/((fraction unused) + (fraction used)/(speed up used))
1.2 = 1/(0.6 + 0.4/(speed up used))
0.4/(speed up used) + 0.6 = 1/1.2
speed up used = 1.71

### Computer Organization

#### Basic Structure of Computer organization

![(image of computer block diagram)](https://ik.imagekit.io/ketanprakash001/NotesAssets/Screenshot_20210818_101252_WsWjGuSyT.png?updatedAt=1629267039559)

![(image of computer block diagram with i/o bifurcation)](https://ik.imagekit.io/ketanprakash001/NotesAssets/Screenshot_20210818_101536_a7hbXdGXO.png?updatedAt=1629267038800)

##### Components of a Processor

1. CU

2. ALU 
    1. IU
    1. FPU

3. Register
    1. MAR
    1. MDR

##### Types of memory

1. ROM
    1. Non-volatile memory segment that consists of the boostrap program that instructs the computer to load the OS. 
    1. BIOS(Basic Input Output System)
    1. Vector Address for the interrupts

  Interrupt Handling:
  ![(interrupt handling image)](https://ik.imagekit.io/ketanprakash001/NotesAssets/Screenshot_20210818_102604_Mwi8UVroU.png?updatedAt=1629267037930)

2. RAM

![(image of computer block diagram with i/o and memory bifurcation)](https://ik.imagekit.io/ketanprakash001/NotesAssets/Screenshot_20210818_105312_Z6nmrbY8d.png?updatedAt=1629267037616)

* Entire memory bus can be seen as a set of buses divided into the address bus, control bus and data bus.

* Address Bus: Used by processor to address the instruction. 

* Data Bus: Carries instruction/data depending on the instruction by processor. 

* Control Bus: Controls the timings of various actions during the interaction(fetching/load, memory read/write, i/o read/write)

* These buses together comprise the memory bus

##### Addressing of Memory Systems

1. Little Endian System: LSB is stored in the address specified by the store operation

2. Big Endian System: MSB is stored in the address specified specfied by the store operation

## 2021-08-24

### Computer system: Layers Of Abstraction

*Software*

1. Application Programs
2. Algorithms
3. Language

*Hardware*

4. Instruction set Architecture(and I/O Interfaces)
5. Microarchitecture
6. Circuits
7. Devices

![(image of a cpu)](https://ik.imagekit.io/ketanprakash001/NotesAssets/Screenshot_20210824_101334_xejJPFWNT.png?updatedAt=1629792047277)

#### Transformation between layers of abstraction

**Layers**
*Software*
1. Problem
2. Algorithm
3. Program

*Hardware*

4. Instruction set Architecture
5. Microarchitecture
6. Circuits
7. Devices

**Transformations**

![(image of the flowchart)](https://ik.imagekit.io/ketanprakash001/NotesAssets/Screenshot_20210824_104211_4u_6WTtEn.png?updatedAt=1629792046460)

1. Problem -> Algorithm (Software Design i.e Choose Data Structures and Algorithms)
1. Algorithm -> Program (Programming i.e Use some language to express the design)
1. Program -> ISA (Compiling/Interpreting i.e converting language to machine instructions)
1. ISA -> Microarchitecture (Processor Design i.e. choosing structures to design each instructions)
1. Microarchitecture -> Circuits (logic/circuit design i.e gates and low level circuits to implement the components)
1. Circuits -> Devices (Process Engineering and Fabrication i.e Develop and Manufacture Lowest level of components)

**Choices Available at each level**

![(Image of choices flowchart)](https://ik.imagekit.io/ketanprakash001/NotesAssets/Screenshot_20210824_143248_K79_QGHyH.png?updatedAt=1629795821719)

![(Self Study Work)](https://ik.imagekit.io/ketanprakash001/NotesAssets/Screenshot_20210824_105714_pV3GfOJog.png?updatedAt=1629792045870)

## 2021-08-25

### Instruction Set

**A processor instruction set defines how the instructions access their operands and how the instructions are described in the processor's assembly language**

<hr/>
Eg instruction: 
(i) MOV r1, r2 // Move the contents in register r2 to r1 

r1, r2 - operands
MOV - operation or "opcode"

Here the instruction accesses the contents of the registers r1 and r2 directly

The instruction performs three operations:
1. Fetch
The instructions are fetched 
1. Decode
Instructions are decoded in the CPU
1. Execute
Instructions are executed according to the operation implementation in the CPU

(ii) MUL r0, M[addr1]  
The instruction accesses the second operand indirectly
(iii) MUL r1, r2{M[addr1]}
The instruction accesses the second operand indirectly

![(source and destination image)](https://ik.imagekit.io/ketanprakash001/NotesAssets/Screenshot_20210825_101516_1CAJKkHT_.png?updatedAt=1629874201454)
<hr/>

**Opcode: Operations to be done by the processor**
**Operand: That are to be used in the operation**

>Instruction has both Opcode and Operand

**Instruction: Instruction is a word in binary of m-bytes where m = 1, 2, 3, ... n, opcode is put in the opcode field of the instruction which is fetched by the processor.**

![(instruction fields image 1)](https://ik.imagekit.io/ketanprakash001/NotesAssets/Screenshot_20210825_101923_lbjluo6os.png?updatedAt=1629874104566)