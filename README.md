# 🖥️ CPU Scheduling Algorithms Simulator

A C++ command-line simulator for the most common CPU scheduling algorithms, built as an Operating Systems course project. Supports interactive process input, Gantt chart output, and per-process performance metrics.

---

## 📋 Table of Contents

- [About the Project](#about-the-project)
- [Algorithms Implemented](#algorithms-implemented)
- [How to Compile & Run](#how-to-compile--run)
- [Usage](#usage)
- [Sample Output](#sample-output)
- [Project Structure](#project-structure)
- [Technologies Used](#technologies-used)
- [Author](#author)

---

## About the Project

This project simulates five classic CPU scheduling algorithms used in operating systems. It accepts process details (arrival time, burst time, priority) from the user at runtime and computes:

- **Gantt Chart** — visual representation of execution order
- **Turnaround Time** — total time from arrival to completion
- **Waiting Time** — time a process spends waiting in the ready queue
- **Average Turnaround & Waiting Time** — overall performance metrics

---

## Algorithms Implemented

| # | Algorithm | Type |
|---|-----------|------|
| 1 | **FCFS** – First Come First Served | Non-Preemptive |
| 2 | **SJF** – Shortest Job First | Non-Preemptive |
| 3 | **SRTF** – Shortest Remaining Time First | Preemptive |
| 4 | **Priority Scheduling** | Non-Preemptive |
| 5 | **Round Robin** | Preemptive (with configurable quantum) |

---

## How to Compile & Run

### Prerequisites
- A C++ compiler (g++ recommended)
- Linux / WSL / macOS / Windows with MinGW

### Compile
```bash
g++ -o scheduler scheduler.cpp
```

### Run
```bash
./scheduler
```

---

## Usage

1. Run the program
2. Choose a scheduling algorithm (1–5)
3. Enter the number of processes
4. For each process, provide:
   - **Arrival Time**
   - **Burst Time**
   - **Priority** *(only for Priority Scheduling)*
5. For Round Robin, also enter the **Time Quantum**

The program will output the Gantt Chart and a table of results.

---

## Sample Output

```
CPU Scheduling Algorithms
1 - FCFS
2 - SJF
3 - SRTF
4 - Priority
5 - Round Robin
Choose Algorithm: 1
Enter number of processes: 3
P1 (arrival, burst): 0 5
P2 (arrival, burst): 1 3
P3 (arrival, burst): 2 8

Gantt Chart:
P1(0→5)  P2(5→8)  P3(8→16)

PID   Arrival   Burst   Start     Finish    Turn        Wait
1     0         5       0         5         5           0
2     1         3       5         8         7           4
3     2         8       8         16        14          6

Average Turnaround: 8.67
Average Waiting: 3.33
```

---

## Project Structure

```
📁 cpu-scheduling/
│
├── scheduler.cpp       # Main source file (all algorithms)
└── README.md           # Project documentation
```

---

## Technologies Used

- **Language:** C++
- **Standard Library:** `<iostream>`, `<vector>`, `<queue>`, `<algorithm>`, `<iomanip>`, `<numeric>`, `<limits>`
- **Compiler:** g++ (C++11 or later)
- **Platform:** Linux / WSL Ubuntu / Windows

---

## Author

**Eman Fatima**  
BS Computer Science — Operating Systems Project  
[Your University Name]  

> 📌 *Feel free to fork this repo, open issues, or suggest improvements via pull requests!*
