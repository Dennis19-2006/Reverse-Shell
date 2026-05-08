# Reverse-Shell
# Linux Reverse Shell in C

> Educational reverse shell implementation written in C using Linux sockets and system calls.

⚠️ **Disclaimer:**  
This project is strictly for educational purposes, cybersecurity research, and learning low-level Linux networking concepts. Only use this code inside isolated lab environments, virtual machines, or systems you own and are authorized to test.

---

# Overview

This project demonstrates how a reverse shell works internally using:

- TCP sockets
- Linux system calls
- File descriptor redirection
- Process execution
- Client-server communication

The program connects to a remote listener and redirects the shell’s input/output streams through the network socket.

---

# Features

- TCP client socket creation
- Remote connection using `connect()`
- Input/output redirection with `dup2()`
- Shell execution using `execve()`
- Lightweight and minimal implementation
- Written completely in C

---

# Technologies Used

- C Programming Language
- GCC Compiler
- Linux/POSIX System Calls
- TCP/IP Networking
- Linux Terminal

---

# Concepts Learned

While building this project, I learned about:

- `socket()`
- `connect()`
- `sockaddr_in`
- `AF_INET`
- `SOCK_STREAM`
- `dup2()`
- `execve()`
- Linux file descriptors
- TCP networking basics
- Process execution in Linux
- Remote communication

---

# Environment Used

This project was developed and tested inside:

- Kali Linux VM
- GCC Compiler
- Linux Terminal

Code was written using:

- VS Code / Nano / Vim

---

# Compilation

Compile the program using GCC:

```bash
gcc reverse_shell.c -o reverse_shell
```

---

# Running the Program

## Step 1 — Start a Listener

On the listener machine:

```bash
nc -lvnp 4242
```

## Step 2 — Execute the Reverse Shell

```bash
./reverse_shell
```

The program will connect to the listener and redirect the shell through the TCP socket.

---

# How It Works

1. Create TCP socket
2. Connect to remote IP and port
3. Redirect stdin/stdout/stderr using `dup2()`
4. Execute `/bin/sh`
5. Interact with the shell remotely

---

# Educational Purpose

This project was created to better understand:

- Linux internals
- Socket programming
- Cybersecurity fundamentals
- Reverse shells
- Process management
- System programming in C

---

# Future Improvements

Possible future upgrades:

- Better error handling
- Encrypted communication
- Multi-client support
- Bind shell implementation
- Logging functionality
- Windows version using WinSock
- Command-and-control dashboard
- IPv6 support

---

# Author

Mandeep Singh

B.Tech CSE (Data Science)

---

# License

This repository is intended for educational and research purposes only.
