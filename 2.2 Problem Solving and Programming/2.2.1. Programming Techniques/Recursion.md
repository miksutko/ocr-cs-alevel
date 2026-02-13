# What recursion is
- A **recursive function** is a function that **calls itself** repeatedly **until a base case is met**.

**Advantages:**
- Can be **very simple/elegant** for problems that repeat the same process on smaller inputs (e.g., factorial).
- Many people find it **easier to understand** because you keep applying the same rule again and again.
- Some languages/paradigms rely on recursion heavily (e.g., functional languages that don’t use loops much).

**Disadvantages:**
- **Memory use is higher** than iteration: each recursive call creates a new “copy”/instance in memory, unlike a loop which updates existing variables.
- Needs a correct **base case**, otherwise it can keep calling itself (non-terminating).
- (From your notes, good to mention) can cause a **stack overflow** if too many calls happen, and can be harder to trace than loops.
# Recursion vs iteration
- Both can repeat a process, but recursion can be a more direct way to express some problems.
- Main drawback: recursion typically uses **more memory**, because each call adds another “copy” of the function’s state while it waits to return.
Key exam point: you must state the **base case** clearly, otherwise recursion may never stop.
