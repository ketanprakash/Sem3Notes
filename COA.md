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
No of instructions executed in running a program/Time required to run the program

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

Eg: 1998 version of a comp executes a program in 200sec. 2000 computer executes in 150sec;

speed up = 200/150 = 1.33

Eg: To achieve a speed up of 3 of a program that originally took 78s to execute, what must be the execution time of the program of the program be reduced to?

new execution time = 78/3 = 26

5. Benchmark Programs
Suite of typical programs that are tested on the programs. Eg: SPECviewperf(by SPEC), Cinebench(by Maxxon), etc. 