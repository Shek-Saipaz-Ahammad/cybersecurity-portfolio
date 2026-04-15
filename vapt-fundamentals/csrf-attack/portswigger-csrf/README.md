# 🔐 CSRF - Token Validation Depends on Request Method (PortSwigger Lab)

## 📘 Lab Overview

This lab is from PortSwigger Web Security Academy.  
It demonstrates a CSRF vulnerability where the application validates the CSRF token only for specific HTTP methods.

---

## 🧠 Concept

- The application checks the CSRF token for **POST requests**
- But it does **not validate the token for GET requests**
- This creates a bypass opportunity

---

## ⚙️ What I Did

- Intercepted the request using Burp Suite  
- Observed that the request method was **POST**  
- Converted the request method from **POST → GET**  
- Removed the CSRF token from the request  
- Sent the modified request  

---

## 💥 Result

- The request was successfully accepted  
- Action was performed without CSRF token  
- This confirms a **CSRF vulnerability due to improper validation**

---

## 🛠️ Tools Used

- Burp Suite  
- Browser  

---

## 📸 Screenshot

[View Proof of Work](./csrf-poc.png)

---

## ⚠️ Note

This lab was performed on PortSwigger Web Security Academy for educational purposes only.
