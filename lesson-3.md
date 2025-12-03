# How JavaScript executes the code - behind the scenes

Following are the steps to execute a JavaScript code:  

**Step #1 - Parsing**  

Parsing  
Identifies keywords and tokens (other than keywords).
Creates a syntax tree.

**Step #2 - Compilation using JIT Compiler**  

JIT Compiler  
Compiles code into Byte Code.
At the end Byte Code is then converted into Machine Code for the execution.

**Step #3 - Code Execution**  
Machine Code is executed as and when required.

---

## 💻 JavaScript Code Execution: A Refined View

### **Step #1 - Parsing**

The description for parsing is accurate.

* **Parsing** involves the engine reading the raw JavaScript code file.
* It **tokenizes** the code (breaks it into meaningful chunks like keywords, identifiers, and operators).
* It then creates an **Abstract Syntax Tree (AST)**, which is a tree-like representation of the code's structural relationships. 
* The AST is essential for the next step.

---

### **Step #2 - Compilation (via Interpreter and JIT)**

This is where your step can be refined. Modern JavaScript engines use a sophisticated **two-tiered compilation** approach, starting with an Interpreter for speed and then optimizing hot code with an Optimizing Compiler.

1. **Initial Compilation to Bytecode (by the Interpreter):**
    * The engine first uses an **Interpreter** (like Ignition in V8) to quickly convert the **AST** into **Bytecode**.
    * The engine immediately starts executing this Bytecode. This allows the code to start running much faster than waiting for full optimization.

2. **Profiling and JIT Optimization (by the Optimizing Compiler):**
    * While the Interpreter is running the Bytecode, the code is **monitored** (profiled).
    * If a function or block of code is run many times ("**hot code**"), a **Just-In-Time (JIT) Compiler** (like TurboFan in V8) takes that Bytecode and compiles it into highly optimized **Machine Code**.
    * The JIT compiler's job is to make the frequently used parts of the code run as fast as native compiled code.

> **Key takeaway:** Code is often first executed as **Bytecode** by the Interpreter, and then the "hot" parts are re-compiled into **Machine Code** by the JIT Compiler for maximum performance.

---

### **Step #3 - Code Execution**

The execution step also involves the **Execution Context** and **Call Stack**.

* The **Machine Code** (or Bytecode) is executed by the computer's CPU.
* The entire process takes place within an **Execution Context**, which is created for every function call.
* The execution contexts are managed on the **Call Stack** (or Execution Stack). This stack ensures code is executed in the correct order (Last-In, First-Out).
