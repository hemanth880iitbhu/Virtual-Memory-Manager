# 🖥️ Virtual Memory Manager

<p align="center">

![C++](https://img.shields.io/badge/C%2B%2B-17-blue?style=for-the-badge\&logo=c%2B%2B)
![OS](https://img.shields.io/badge/Operating%20Systems-Virtual%20Memory-success?style=for-the-badge)
![Algorithms](https://img.shields.io/badge/Page-Replacement-orange?style=for-the-badge)
![Platform](https://img.shields.io/badge/Platform-Linux-lightgrey?style=for-the-badge)

</p>

<p align="center">
A C++ simulator for studying and comparing <b>Virtual Memory Page Replacement Algorithms</b> used in modern Operating Systems.
</p>

---

## 📖 Overview

Virtual Memory is one of the most fundamental concepts in Operating Systems. Whenever a requested page is not available in physical memory, the operating system must decide **which page should be replaced**.

This project implements and compares multiple **page replacement algorithms** by simulating memory accesses over a page reference string. It evaluates their efficiency based on:

* 📄 Number of Page Replacements
* ⚡ Execution Time
* 📊 Replacement Penalty compared to the Optimal Algorithm

The simulator allows users to configure the number of available memory frames and execute different replacement policies through a simple command-line interface.

---

## ✨ Features

* ✅ Implements **6 page replacement algorithms**
* ✅ Configurable number of memory frames
* ✅ Reads page reference strings from a file or terminal
* ✅ Benchmarks every algorithm against **Optimal Replacement**
* ✅ Calculates page replacement penalty
* ✅ Measures execution time
* ✅ Lightweight command-line interface
* ✅ Modular C++ implementation

---

# 🧠 Algorithms Implemented

| Algorithm                     | Description                                                                            |
| ----------------------------- | -------------------------------------------------------------------------------------- |
| **FIFO**                      | Replaces the page that entered memory first.                                           |
| **LRU (Stack)**               | Replaces the least recently used page using a doubly linked list.                      |
| **LFU**                       | Replaces the page with the lowest access frequency.                                    |
| **LRU Clock (Second Chance)** | Uses reference bits to approximate LRU efficiently.                                    |
| **LRU-REF8**                  | Uses an 8-bit reference register to approximate LRU.                                   |
| **Optimal**                   | Replaces the page whose next use occurs farthest in the future. Used as the benchmark. |

---

# 🏗️ Project Structure

```text
Virtual-Memory-Manager/
│
├── src/
│   ├── algo.cpp              # Algorithm implementations
│   ├── algo.h                # Data structures & declarations
│   ├── virtualmem.cpp        # Driver program
│   └── virtualmem.h
│
├── input.txt                 # Sample page reference string
└── README.md
```

---

# ⚙️ Data Structures Used

* Singly Linked List
* Doubly Linked List
* Circular Linked List
* STL Vector
* Custom Result Structures

---

# 📂 Sample Input

```
7 0 1 2 0 3 0 4 2 3 0 3 2 1 2 0 1 7 0 1
```

---

# 🚀 Build

Compile using **g++**

```bash
g++ src/virtualmem.cpp src/algo.cpp -o virtualmem
```

---

# ▶️ Usage

```bash
./virtualmem -f <frames> -r <algorithm> -i input.txt
```

### Example

```bash
./virtualmem -f 5 -r FIFO -i input.txt
```

---

# 📌 Command Line Arguments

| Argument | Description                       |
| -------- | --------------------------------- |
| `-f`     | Number of available memory frames |
| `-r`     | Page replacement algorithm        |
| `-i`     | Input file                        |
| `-h`     | Display help information          |

---

# 📋 Supported Algorithms

```
FIFO
LRU-STACK
LFU
LRU-CLOCK
LRU-REF8
```

---

# 📊 Performance Evaluation

For every execution, the simulator reports:

* 📄 Total Page Replacements
* 📈 Page Replacement Penalty
* ⏱️ Execution Time
* ⚖️ Comparison with the Optimal Algorithm

This allows users to understand the trade-offs between different replacement strategies.

---

# 💡 Concepts Demonstrated

* Virtual Memory
* Demand Paging
* Page Replacement Policies
* Memory Management
* Operating Systems
* Performance Analysis
* Linked Lists
* Time Complexity
* Command Line Programming

---

# 🛠️ Tech Stack

| Category        | Technology            |
| --------------- | --------------------- |
| Language        | C++                   |
| Concepts        | Operating Systems     |
| Data Structures | Linked Lists, Vectors |
| Platform        | Linux                 |
| Compiler        | g++                   |

---

# 🔮 Future Improvements

* Add Random Replacement Algorithm
* Implement NRU and MRU
* Support Clock-Pro Algorithm
* Export results to CSV
* Interactive visualization of memory frames
* Graphical comparison of page faults
* Automated benchmarking on larger workloads

---

# 📚 Learning Outcomes

Through this project, I gained hands-on experience with:

* Operating System memory management
* Virtual memory concepts
* Page replacement algorithms
* Algorithmic performance comparison
* Linked list implementation
* Modular C++ project design
* Command-line application development

---

# 👨‍💻 Author

**Paturi Hemanth Sai**

B.Tech, Computer Science and Engineering
Indian Institute of Technology (BHU), Varanasi

---

<p align="center">

⭐ If you found this project useful, consider giving it a star!

</p>
