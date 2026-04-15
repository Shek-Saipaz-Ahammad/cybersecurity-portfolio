# CSRF - Real World Style Simulation

## 🧪 Overview

In this exercise, I studied how CSRF (Cross-Site Request Forgery) can be used in real-world scenarios.

The goal was to understand how a malicious link can trigger unwanted actions in an authenticated session.

This was performed in a controlled learning environment.

---

## 🎯 Scenario

A web application was tested for CSRF behavior using multiple logged-in sessions.

The main focus was:
- Session handling
- Request manipulation
- Impact of forged requests

---

## 🔍 What I Did

- Logged into the application using two different test accounts
- Observed session behavior between accounts
- Captured a sensitive request using Burp Suite
- Modified the request to simulate a malicious action
- Created a fake “click-based” request (PoC) to trigger the action

---

## 🧪 Testing Method

- Intercepted HTTP request using Burp Suite
- Identified session-based request flow
- Reused and modified the captured request
- Sent the modified request while logged into a valid session

---

## 💥 Result

- The session was affected by the forged request
- The application performed an unintended action on the authenticated session
- Demonstrated how CSRF can impact user sessions

---

## 🧠 Key Learning

- CSRF works because browsers automatically send session cookies
- If no CSRF protection exists, requests can be reused or modified
- Session-based authentication alone is not enough protection
- Burp Suite is useful for analyzing and modifying requests

---

## 🛡️ Security Insight

To prevent CSRF attacks:
- Use CSRF tokens
- Validate request origin
- Use SameSite cookies
- Implement proper session validation

---

## 📸 Proof of Work

[View Screenshot](./csrf.png)


## ⚠️ Note

This was performed only in a controlled environment for learning web security concepts.

No real-world system or production data was targeted.
