## Overview
Code Trace is a browser-based learning dashboard for exploring Linux process management, signals, system calls, `/proc`, GDB, and `strace`. This package includes a static dashboard interface with CSS animations and transitions removed.

## Contents
- `index.html` — dashboard interface (no animations or CSS transitions)
- `code_trace.c` — companion C program demonstrating Linux process and system-call concepts
- `run_dashboard.sh` — launch script for the dashboard
- `README_UBUNTU.txt` — brief Ubuntu launch notes

## Requirements
- Ubuntu or another Linux distribution
- A modern web browser
- GCC/build tools to compile the C program
- Optional: `gdb` and `strace` for the related learning modules

Install tools if needed:

```bash
sudo apt update
sudo apt install build-essential gdb strace
```

## Open the dashboard
From a terminal, enter the extracted project directory and run:

```bash
chmod +x run_dashboard.sh
./run_dashboard.sh
```

If the script cannot open a browser, open `index.html` directly in Firefox or another browser.

## Compile and run the C program
From the project directory:

```bash
gcc -Wall -Wextra -std=c11 -o code_trace code_trace.c
./code_trace
```

The C program runs in the terminal. It is separate from the browser dashboard. Some system-call demonstrations may create `trace_output.txt` in the current directory.

## Animation setting
The dashboard uses no CSS animations or transitions. Navigation and section changes are immediate.

## Notes
- The dashboard is an HTML/CSS/JavaScript web interface; the companion program is written in C.
- Run only on a system where you have permission to inspect processes or use debugging/tracing tools.
