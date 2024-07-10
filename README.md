# Multicore-CPU-Scheduler-Simulation


This C program simulates a multicore CPU scheduler that can handle multiple scheduling algorithms based on user-defined configurations. It reads process data from a binary file, initializes multiple processor cores, and executes processes using various scheduling strategies including Priority Scheduling, Shortest Job First (SJF), Round Robin (RR), and First Come First Served (FCFS). Key functionalities include:

  - Dynamic Process Queue Management: Processes are dynamically queued based on their scheduling priority, CPU burst time, or in a first-come, first-served manner.

  - Multicore Execution: Each CPU core executes processes concurrently, with provisions for load balancing and inter-core process assistance.

  - Supervisor Thread: Monitors CPU cores to determine when all processes have been executed, signaling program completion.

  - File I/O Operations: Reads process details such as priority, CPU burst time, and memory constraints from a binary file.

  - Error Handling: Includes robust error handling for file operations, command-line argument validation, and scheduling algorithm validation.

This simulation provides insights into how multicore CPUs manage and execute processes under different scheduling paradigms, useful for understanding operating system principles and CPU scheduling algorithms.

Instructions to Compile and Run:
  1. Use the gcc compiler to build the executable binary.

     `gcc -o scheduler scheduler.c -pthread`
     
  3. Execute the compiled binary with the appropriate command-line arguments.

     ` ./scheduler <filename> <algro1> <load1> <algro2> <load2> ...`
   
  4. Example Command:

     `./scheduler processes.bin 1 0.3 2 0.4 3 0.3`
