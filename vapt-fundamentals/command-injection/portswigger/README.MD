# PortSwigger - Command Injection

## 📌 Overview
In this lab, I tested a simple OS command injection vulnerability.

The goal was to check if user input can be used to execute system commands.

---

## ⚙️ What I Did

- The application was using a parameter: `storeId=1`  
- I modified the input to: `storeId=1 | whoami`  
- Sent the request using Burp Suite  

---

## ✅ Result

- The application executed my command  
- Output received: `peter-bsTjTO`  

This confirmed that the input was vulnerable to command injection.

---

## 🧠 Key Learning

- Even simple parameters can be vulnerable  
- Input is directly passed to system commands  
- Small changes like `| whoami` can confirm the issue  
- Burp Suite helps in modifying and testing requests  

---

## 📸 Proof of Work

- Command injection output: [View Screenshot](screenshot-portswigger.png)   


