- **Processor**: the computer's brain; executes instructions to run programs. Made up of a Control Unit (CU), Registers and Arithmetic and Logic Unit (ALU).

![[Pasted image 20241227173034.png]]
# 1. Control Unit (CU):
- This is where instructions are decoded. The CU also controls the data within the CPU and how it moves around.
---
# 2. Registers:
- **Definition**: temporary storage/memory locations inside the CPU which are used for a single specific purpose. They have a faster access speed than RAM / secondary storage.

| Registers                          | Purpose                                                                                                                                       |
| ---------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------- |
| Program Counter (PC)               | Stores the address of the next instruction to be fetched.                                                                                     |
| Memory Address Register (MAR)      | This is where addresses are stored, either for where data is being sent in memory, or where it is being fetched from                          |
| Memory Data Register (MDR)         | This is where data/instructions are stored, either before it sent to memory, or after being fetched                                           |
| Current Instruction Register (CIR) | When an instruction has been fetched from memory it is loaded here before being split into opcode and operand. After this, it will be decoded |
| Accumulator (ACC)                  | This is where values are stored temporarily, either after they’ve been inputted or loaded, or after being calculated in the ALU               |

| Register | Role                     | Example Value     |
| -------- | ------------------------ | ----------------- |
| **PC**   | Next instruction address | 0x01, then 0x02   |
| **MAR**  | Memory address to access | 0x01              |
| **MDR**  | Data fetched or to write | "Load 7 into ACC" |
| **CIR**  | Current instruction      | "Load 7 into ACC" |
| **ACC**  | Operation result         | 7 → 12            |

---
# 3. Arithmetic and Logic Unit (ALU):
- This performs any arithmetic calculations (e.g. adding binary) or any logic comparisons (using AND, OR, NOT).
- Made up of several components:
	- **Arithmetic circuit**
	    - This carries out any arithmetic (addition, subtraction, multiplication or division)
	- **Logic circuit**
	    - This carries out operations like AND, OR, NOT, XOR
	- **Registers**
	    - These are additional registers to those mentioned above and can store data
	- **Status flags**
	    - This includes overflow flags (if the value is too large for the register) or could include a zero flag (to tell if the answer is 0 easily)
	- **Buses**
	    - These are used to transport data around the ALU and to other parts of the CPU
## Example: Addition Instruction
1. **Operation**: Add two numbers.
2. **Input**: Two binary numbers.
    - Example: `5` (binary: `0101`) and `3` (binary: `0011`).
3. **ALU Action**: Perform binary addition.
    - `0101 + 0011 = 1000` (binary), which equals `8` in decimal.
4. **Output**: The result of the addition (`1000`).
---
# 4. Buses in the CPU:
- There are three main buses that connect the CPU, main memory (RAM) and other components:
	- Data bus
	- Address bus
	- Control bus
## Types of Buses:
1. **Data Bus**:
	- **Purpose**: Transfers data and instructions between the CPU, memory and input/output devices
	- **Direction**: Read/Write (Bidirectional)
	- **In a CPU Example**:
		- Suppose the CPU needs to add two numbers stored in memory:
	    1. The CPU uses the **data bus** to fetch the numbers (e.g., **7** and **5**) from memory.
	    2. After the addition, the CPU uses the **data bus** again to send the result (e.g., **12**) back to memory.
2. **Address Bus**: 
	- **Purpose**: Transfers the memory address of where data or instructions are to be read from or written to
	- **Direction**: Write only (Unidirectional) CPU → Memory/I/O
	- **In a CPU Example**:
		- Continuing the example of adding two numbers:
	    1. The CPU uses the **address bus** to point to the memory location where the first number (**7**) is stored.
	    2. The address bus then points to the memory location of the second number (**5**) for retrieval.
3. **Control Bus**: 
    - **Purpose**: Transfers control signals used to manage the operations of the computer system (e.g. memory read, memory write, interrupt requests)
	- **Direction**: Sends signals (Bidirectional)
	- **In a CPU Example**:
		- While adding two numbers:
	    1. The control bus sends a **"read" signal** to memory, instructing it to send the number **7** to the CPU.
	    2. After the CPU processes the addition, the control bus sends a **"write" signal**, telling memory to store the result (**12**).
---
# 5. Pipelining
- Pipelining is the process of carrying out multiple instructions concurrently 
- Each instruction will be at a different stage of the fetch-decode-execute cycle 
- One instruction can be fetched while the previous one is being decoded and the one before is being executed 
- In the case of a branch (in a branch the instruction in the next location in memory is not necessarily executed next. See assembly language for more detail), the pipeline is flushed 
- While one instruction is being executed, the next instruction will be decoded and the following instruction will be fetched
- Pipelining increases instruction throughput by overlapping stages, while latency per instruction remains unchanged
- The CPU is not idle while waiting for the next instruction which increases the speed of execution
- The next instruction is fetched while the current one is decoded/executed
- All parts of the processor can be used at any instance in time