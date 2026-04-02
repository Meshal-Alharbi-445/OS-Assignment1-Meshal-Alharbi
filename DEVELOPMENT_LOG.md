# Development Log

## Instructions
Document your development process as you work on the assignment. Add entries showing:
- What you worked on
- Problems you encountered
- How you solved them
- Time spent

**Requirements**: Minimum 5 entries showing progression over time.

---

## Example Entry Format:

### Entry 1 - [April 1, 2026, 2:30 PM]
**What I did**: Forked the repository and set up my student ID

**Details**: 
- Created GitHub account with university email
- Forked the starter repository
- Changed student ID on line 92 to my actual ID (441234567)
- Compiled and ran the program successfully

**Challenges**: Had to install JDK first because javac wasn't recognized

**Solution**: Downloaded JDK 17 from Oracle website and set PATH variable

**Time spent**: 30 minutes

---

## Your Development Log:

### Entry 1 - [March 30, 2026, 11:30 AM]
**What I did**: 
Created a GitHub account with my university email and forked the project repository.
**Details**: 
Set up my environment by linking my academic email to GitHub for verification. I then forked the starter repository and updated the student ID on line 150 in the code to my actual ID for unique random generation.
**Challenges**: 
Initial permission issues when pushing changes back to the repository.
**Solution**: 
Logged into GitHub through VS Code using my university credentials to sync the project.
**Time spent**: 
35 minutes
---

### Entry 2 - [April 2, 2026, 5:45 AM]
**What I did**: 
Implementation of Feature 1 (Process Priority)
**Details**: 
• Added a private integer field priority to the Process class.
• Updated the Process constructor to accept and initialize the priority value.
• Modified the process creation loop in SchedulerSimulation to generate a random priority (1-5) using random.nextInt(5) + 1.
• Updated the output message to display the priority when a process enters the ready queue.
**Challenges**: 
Encountered a logic error where the priority value was identical to the burst time for every process.
**Solution**: 
Realized I was either using the same random variable or passing the wrong parameter in the constructor. Fixed it by ensuring a separate nextInt call for priority and correctly mapping the parameters in the new Process() call.
**Time spent**: 
40 minutes
---

### Entry 3 - [April 2, 2026, 2:30 PM]
**What I did**: 
Implemented a counter to track context switches between processes.
**Details**: 
Added a static int contextSwitchCount that increments every time the scheduler pulls a new thread from the queue. This measures the overhead of the Round Robin algorithm.
**Challenges**: 
Ensuring the counter increments correctly even when a process yields and is re-enqueued.
**Solution**: 
Placed the increment logic at the beginning of the while loop so it counts every CPU transition.
**Time spent**: 
45 minutes
---

### Entry 4 - [April 2, 2026, 4:00 PM]
**What I did**: 
Tracked process lifecycle and created a final summary statistics table.
**Details**: 
Used System.currentTimeMillis() to capture creation and finish times. Calculated waiting time for each process and displayed a formatted table showing Name, Burst Time, and Waiting Time at the end.
**Challenges**: 
Capturing the finish time for the very last process in the queue after it runs to completion.
**Solution**: 
Updated the if-else logic to ensure setFinishTime() is called and the process is added to completedProcesses in all termination scenarios.
**Time spent**: 
1 hour
---

### Entry 5 - [Date and Time]
**What I did**: 

**Details**: 

**Challenges**: 

**Solution**: 

**Time spent**: 

---

### Entry 6 - [Optional - Date and Time]
**What I did**: 

**Details**: 

**Challenges**: 

**Solution**: 

**Time spent**: 

---

## Summary

**Total time spent on assignment**: [7 hours]

**Most challenging part**: 
Ensuring all finished processes were accurately captured and stored for the final summary table, especially managing the edge case where the last process runs to completion without returning to the queue.
**Most interesting learning**: 
Understanding how System.currentTimeMillis() can be used to track low-level process lifecycles and seeing how context switches directly impact the overall efficiency of the Round Robin algorithm.
**What I would do differently next time**: 
I wish I had started working on the program earlier to give myself more time for deep debugging and UI refinement. In the future, I plan to manage my time better and explore adding more advanced features like dynamic time quantum adjustments.
