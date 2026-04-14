# Architecture of Linux

The Linux operating system architecture defines how different components of the system interact with each other to
manage hardware resources, run applications, and provide a stable and secure computing environment.
Linux follows a **layered architecture**, where each layer has a specific role and responsibility.


<img align=center width="423" height="400" alt="image" src="https://github.com/user-attachments/assets/e951cd0e-f534-409e-bb1e-787b0984cd11" />

### Main Components
* **Application**
* **Shell**
* **Kernel**
* **Hardware**
* **Utilities**

Each layer communicates with the one below it, creating a structured and efficient operating system design.

---

## 1. Kernel
The **Kernel** is the core component of the Linux operating system that sits between the hardware and user space, managing system resources and ensuring smooth communication between software and hardware. It controls how processes are executed, scheduled, and isolated to maintain system stability and security.

### Responsibilities of the Kernel
* **Memory management:** Allocates and manages system memory efficiently.
* **Process management:** Schedules processes and controls execution using queues.
* **Resource allocation:** Distributes CPU, memory, and I/O resources among processes.
* **Device management:** Controls hardware devices through device drivers.
* **Application interaction:** Acts as a bridge between applications and hardware.
* **Security:** Enforces access control and system-level security mechanisms.

### Types of Kernel
1.  **Monolithic Kernel:** Offers high performance due to direct communication between components, but the large kernel size makes it more complex and harder to maintain. All core services (process management, file systems, etc.) run in kernel space.
2.  **Microkernel:** Only essential services like process scheduling run in kernel space; others execute in user space. Provides better security but may have performance overhead due to inter-process communication.
3.  **Exokernel:** Exposes hardware resources directly to applications, allowing low-level management. Enables high flexibility but increases application complexity.
4.  **Hybrid Kernel:** Combines features of monolithic and microkernel architectures. It keeps critical services in kernel space while supporting modular components for a balance of speed and stability.

### Main Subsystems of Kernel

<img width="800" height="400" alt="image" src="https://github.com/user-attachments/assets/006b6a2e-cc0d-433a-b221-5048da795cb9" />


* **Process Scheduler:** Responsible for fairly distributing the processing time among all concurrently running processes.
* **Memory Management Unit:** This subunit is responsible for proper distribution of memory resources among processes.
* **Virtual File System (VFS):** Provides an interface to access stored data across different file systems and physical media.
* **Networking Subsystem:** Handles all network communication, including data transmission, routing, and protocols.
* **Inter-Process Communication (IPC) Unit:** Enables communication and synchronization between multiple running processes.

---

## 2. System Library
System libraries provide predefined functions that allow application programs and system utilities to access kernel features without interacting with the kernel directly.

* **GNU C Library (glibc):** Provides core system calls and functions for executing C programs.
* **libpthread (POSIX Threads):** Enables creation and management of multithreaded applications.
* **libdl (Dynamic Linker):** Supports dynamic loading and linking of shared libraries at runtime.
* **libm (Math Library):** Offers mathematical functions such as trigonometry and logarithms.
* **Other libraries:** Includes `librt` (Real-Time), `libcrypt` (Cryptography), `libnss` (Name Service), and `libstdc++` (C++ Standard Library).

---

## 3. Shell
The **Shell** is the interface to the kernel. It takes commands from the user, interprets them, and transmits them to the kernel to perform requested operations.



### Different Types of Shell

<img width="432" height="408" alt="image" src="https://github.com/user-attachments/assets/d11a35d0-bde4-4677-b769-686967b69a2f" />

1.  **Bourne Shell (sh):** One of the earliest shells; reliable, lightweight, and used for system scripts.
2.  **C Shell (csh):** Designed with syntax similar to the C programming language; introduced command history.
3.  **Korn Shell (ksh):** Combines features of Bourne and C shells; widely used in enterprise environments.
4.  **Bash (Bourne Again Shell):** The default shell on most Linux distributions; includes tab completion and advanced scripting.
5.  **Z Shell (zsh):** Highly customizable; popular among developers for themes and advanced auto-completion.
6.  **Fish (Friendly Interactive Shell):** Designed for ease of use with syntax highlighting and auto-suggestions.

---

## 4. Hardware Layer
The hardware layer is the lowest level and forms the foundation of the OS. It consists of physical devices and low-level controls.
* Includes physical components: **CPU, memory, storage, and I/O devices.**
* Works with **device drivers** to enable hardware communication.
* Supports memory access and CPU control.
* Ensures stable interaction between hardware and the OS.

---
  
## 5. System Utilities
These are specialized programs designed to help users manage the system. They bridge the gap between user needs and the underlying system functions.
* **File Management:** Tools like `cp`, `mv`, and `ls`.
* **System Monitoring:** Tools like `top`, `htop`, or `df`.
* **Network Config:** Tools like `ifconfig` or `ip`.
Here is the architecture of Linux formatted in Markdown for clarity and scannability.

---
