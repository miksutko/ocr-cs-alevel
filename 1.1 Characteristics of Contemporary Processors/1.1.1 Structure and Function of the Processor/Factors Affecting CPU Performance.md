# 1. Clock Speed:
- The **clock** in the computer controls operations within the CPU. It repeatedly changes from 0 to 1 to 0 and so on - each one of these is referred to as a state change
- A state change can represent one fetch-decode-execute cycle although some take more than one cycle
- Clock speed is a measure of how many states changes the CPU performs per second. 1 cycle per second = 1 Hz
- A typical computer may have a clock speed of 3-5 GHz = 3,000,000,000-5,000,000,000 Hz which is just over 3-5 billion cycles per second
- If a computer has a higher clock speed, it will be able to execute more instructions per second and therefore carry out tasks more quicklyIf a computer has a higher clock speed, it will be able to execute more instructions per second and therefore carry out tasks more quickly
# 2. Number of Cores:
- A core is a processing unit within the CPU
- A single core processor has one core but a computer can have a dual core processor, quad core processor or octa core processor, and even dozens or over a hundred cores depending on the system.
- Normally each core will run at the same speed
- This means that tasks are carried out more quickly using a multicore processor than a single core processor as each core can carry out its task (this is called parallel processing) but a dual core processor isn’t twice as fast as a single core processor as there is some time spent organising tasks between the cores
- The speed of the CPU is also partially determined by the tasks being carried out as some tasks can’t be split between cores and therefore having more cores is no quicker than having one
# 3. Cache Memory:
- The cache is part of primary storage and is used to store frequently used data and instructions
- It is used as it’s closer to the CPU than RAM and therefore is faster to retrieve data from (some of the cache is included within each core)
- The more cache there is, the more data can be stored which speeds up the performance of the CPU
	- E.g. A website you visit often will be stored in the cache so that the next time you visit the website it can load it up more quickly. When the webpage is updated, what is stored in the cache will be updated too
- **Types of Cache**:

| Level  | Speed               | Size                     | Location              | Purpose                            |
| ------ | ------------------- | ------------------------ | --------------------- | ---------------------------------- |
| **L1** | Fastest             | Smallest (e.g., 32-64KB) | Inside CPU core       | Stores most critical instructions. |
| **L2** | Slower than L1      | Larger (e.g., 256KB-2MB) | Inside CPU (not core) | Backup for L1.                     |
| **L3** | Slowest (but > RAM) | Largest (e.g., 4-32MB)   | Shared between cores  | Helps with Multi-core Processing.  |
