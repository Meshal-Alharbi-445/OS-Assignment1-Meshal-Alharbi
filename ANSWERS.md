# Assignment Questions

## Instructions
Answer all 4 questions with detailed explanations. Each answer should be **3-5 sentences minimum** and demonstrate your understanding of the concepts.

---

## Question 1: Thread vs Process

**Question**: Explain the difference between a **thread** and a **process**. Why did we use threads in this assignment instead of creating separate processes?

**Your Answer:**

[A process is an independent program execution that has its own memory space and resources, whereas a thread is a lightweight unit of execution within a process that shares memory with other threads. In this assignment, we used threads because they are much more efficient to create and switch between compared to full processes. Threads allow our simulation to run multiple "tasks" (P1, P2, etc.) simultaneously within the same memory heap, making it easier to manage shared data like the Ready Queue and contextSwitchCount. This setup perfectly mimics how a real CPU handles multiple tasks within a single operating system environment. 
]

---

## Question 2: Ready Queue Behavior

**Question**: In Round-Robin scheduling, what happens when a process doesn't finish within its time quantum? Explain using an example from your program output.

**Your Answer:**

[When a process does not finish within its assigned time quantum, the scheduler interrupts it, saves its current state, and moves it to the back of the Ready Queue. This ensures that no single process monopolizes the CPU, providing fairness to all other waiting tasks. Once the process reaches the front of the queue again, it resumes execution from where it left off. In my program, when a process like "P1" exceeds the 500ms quantum, it is re-enqueued, and the next process in line starts its execution.]

Example from my output:
```
[P1] is running...
[P1] Time Quantum expired. Re-enquing P1...
```

**Explanation of example:**
[This snippet shows that P1 had a remaining burst time larger than the quantum, so the scheduler stopped it and put it at the end of the queue to give other processes a chance.]

---

## Question 3: Thread States

**Question**: A thread can be in different states: **New**, **Runnable**, **Running**, **Waiting**, **Terminated**. Walk through these states for one process (P1) from your simulation.

**Your Answer:**

[
• New: P1 is in the New state when the Process object is first instantiated in the code but before the start() method is called.
• Runnable: P1 becomes Runnable after start() is called and it is added to the readyQueue, waiting for the scheduler to pick it.
• Running: P1 is in the Running state when the scheduler calls its run() method and the CPU is actively executing its instructions.
• Waiting: P1 enters the Waiting (or Blocked) state if it is interrupted by a context switch or if it has to wait for an I/O operation before it can continue.
• Terminated: P1 reaches the Terminated state once its remainingBurstTime reaches zero and it is removed from the execution loop.
]

1. **New**: [P1 is in the New state when the Process object is first instantiated in the code but before the start() method is called.]

2. **Runnable**: [P1 becomes Runnable after start() is called and it is added to the readyQueue, waiting for the scheduler to pick it.]

3. **Running**: [P1 is in the Running state when the scheduler calls its run() method and the CPU is actively executing its instructions.]

4. **Waiting**: [ P1 enters the Waiting (or Blocked) state if it is interrupted by a context switch or if it has to wait for an I/O operation before it can continue.]

5. **Terminated**: [P1 reaches the Terminated state once its remainingBurstTime reaches zero and it is removed from the execution loop.]

---

## Question 4: Real-World Applications

**Question**: Give **TWO** real-world examples where Round-Robin scheduling with threads would be useful. Explain why this scheduling algorithm works well for those scenarios.

**Your Answer:**

### Example 1: [Name of application/scenario]

**Description**: 
[Describe the real-world scenario or application]

**Why Round-Robin works well here**: 
[Explain why Round-Robin scheduling is suitable. Consider fairness, responsiveness, predictability, etc.]

### Example 2: [Name of application/scenario]

**Description**: 
[Describe the real-world scenario or application]

**Why Round-Robin works well here**: 
[Explain why Round-Robin scheduling is suitable. Consider fairness, responsiveness, predictability, etc.]

---

## Summary

**Key concepts I understood through these questions:**
1. 
2. 
3. 

**Concepts I need to study more:**
1. 
2. 
