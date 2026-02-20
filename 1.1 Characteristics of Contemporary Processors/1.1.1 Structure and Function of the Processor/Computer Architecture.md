
|**Architecture**|**Memory Organisation**|**Bus**|**Address Space**|**Control Units**|**Usage**|
|---|---|---|---|---|---|
|**Von Neumann**|Unified Memory|Single|Shared|Single Control Unit|Most modern computers, microcontrollers|
|**Harvard**|Separated Memory|Separate|Distinct|Separate Control Units|Specialised embedded systems|
# 1. Von Neumann Architecture:
- **Description**:
    - Uses a single memory for both data and instructions e.g. single control unit
    - Data and instructions are transferred along a shared data bus.
    - Built on the stored program concept, where programs and data are stored in memory.
    - Uses FDE cycle
- **Advantages**:
    - Cheaper to develop: The control unit is simpler, reducing costs.
    - Program optimization: Programs can be minimized in size.
- **Limitation**:
    - Bottleneck issue: Only one data or instruction can travel at a time along the bus, slowing performance.
![[Pasted image 20250603200214.png]]
---
# 2. Harvard Architecture
- **Description**:
    - Uses separate memory for data and instructions.
    - Different buses are used for data and instruction transfer, allowing simultaneous access.
    - Often used in embedded systems or applications where performance is critical.
- **Advantages**:
    - **Faster execution**: Data and instructions can be fetched in parallel.
    - **Flexible memory sizes**: Instruction memory can be optimized for size and characteristics (e.g., read-only), while data memory can be read-write.
- **Drawbacks:**
	- **Higher Cost**:
	    - The use of separate memory for data and instructions requires more hardware components, making it more expensive to develop and manufacture.
	- **Inefficient Memory Utilization**:
	    - Having dedicated memory for instructions and data can lead to inefficiencies if one type of memory becomes full, while the other has unused space, resulting in wasted resources.
- **Use Case**:
    - Embedded processors in devices like **microwave ovens**, TV remotes, or **medical devices** often use Harvard architecture to maximize efficiency.
![[Pasted image 20250603200228.png]]
---
# How does Harvard architecture improve performance over Von Neumann architecture?
|**Feature**|**Explanation**|
|---|---|
|Two separate areas of memory|One for instructions and one for data<br><br>Instructions and data can be accessed concurrently|
|Different sets of buses|One for instructions and one for data<br><br>Instructions and data can be accessed concurrently|
|Pipelining|Whilst an instruction is being executed the next can be decoded and the subsequent one fetched|
|Use of Cache|A small amount of high performance memory which is next to the CPU<br><br>It stores frequently used data and instructions|
|Virtual cores / Hyper-threading|This is where a physical core can act as two virtual cores|
|Multiple Cores|Each core acts as a separate processing unit|
|Onboard Graphics|Built-in circuitry for graphics processing|
|Performance boosting mode|The clock speed can be temporarily increased for a performance boost|
|Out of Order Execution|Instructions can be executed before earlier ones if they are ready|
|Super Scalar|Multiple instructions can be executed simultaneously|

---
# 3. Contemporary Processing
- **Definition**: Modern CPUs use advanced techniques to improve performance and efficiency beyond the basic Von Neumann model.
- **Key Techniques:
	1. Simultaneous Multithreading (SMT)
		- Runs two threads per core by duplicating fetch/decode units.
		- Better core utilization (execution unit switches between threads).
		- Two physical cores > one core with SMT.
	2. Out-of-Order Execution
		- Executes instructions ahead of time if resources are free (non-dependent).
		- Reduces idle time in the CPU pipeline.
	3. Branch Prediction
		- Predicts the path of conditional branches (e.g., if statements).
		- Minimizes pipeline stalls (avoids clearing the pipeline).
	4. Variable Clock Speed
		- Dynamic Scaling: Temporarily boosts speed for intensive tasks ("turbo boost").
		- Power Saving: Reduces clock speed in portable devices to save battery.
	5. Power Conservation
		- Shuts off unused circuitry (e.g., GPU parts when not needed).