# DVWA - CSRF Practice

## 🧪 Lab Info

This lab was done on DVWA (Damn Vulnerable Web Application).  
DVWA is intentionally insecure and used for learning web security.

---

## 🎯 Goal

To understand how CSRF works in:
- Low security  
- Medium security  

---

## 🔓 Low Security

### ✔ What I Did
- Logged into DVWA  
- Created a simple CSRF PoC (`attack.html`)  
- Sent request to change password  

### 💥 Result
- Attack worked successfully  
- Password changed  

### 🧠 Reason
- No security checks  
- Server accepted all requests  

---

## 🔐 Medium Security

### ⚠️ What Changed
- Application checks **HTTP Referer header**  
- It verifies request source  

---

### ❌ Problem Faced
- Normal CSRF attack failed  
- Because request did not contain proper **Referer header**  

---

### 🔍 What I Did

- Captured request using Burp Suite  
- Observed missing/incorrect `Referer` header  
- Understood that server is checking this header  

---

### 🛠️ Solution

- Added correct `Referer` header in request  
- Sent modified request  

---

### 💥 Result
- Attack worked on medium security also  

---

## 🧠 Key Learning

- CSRF works when server trusts user session  
- Browser sends cookies automatically  
- Medium security uses Referer check  
- Referer check can be bypassed  

---

## 📌 Conclusion

➡️ Low security = direct attack works  
➡️ Medium security = need to bypass Referer check  

CSRF attack tricks the server using the victim's browser.

---

## ⚠️ Note

This testing was done only on DVWA (intentionally vulnerable)  
for learning purposes in a safe environment.
