# DVWA Brute Force (Hydra)

## Objective
In this lab, I tried to perform a brute force attack on the DVWA login page to understand how weak authentication can be exploited.

## What I Did

First, I logged into DVWA using default credentials to access the brute force module.

After that, I observed how the login request works. Then I used Burp Suite to capture the login request and understand the parameters like username, password, and cookies.

Once I understood the request structure, I moved to Hydra tool for automation.

## Hydra Setup

In Hydra, I used:
- Username: admin
- Password list: rockyou.txt
- Target: DVWA login page (HTTP GET form)

I included:
- Login request parameters (username & password fields)
- Cookie value (for session handling)
- Failure message (to identify wrong login attempts)

## Command Concept (Simple)
Hydra was configured with:
- username field
- password wordlist
- HTTP GET form
- cookie session
- failure condition

## Result

After running Hydra, it tested multiple passwords automatically and finally found the correct login credentials.

This helped me understand how attackers automate login attempts.

## What I Learned

- How brute force works on web login forms  
- Importance of capturing requests using Burp Suite  
- How Hydra uses parameters like cookies and failure messages  
- Why weak passwords are dangerous  

## Prevention

- Use strong passwords  
- Implement rate limiting  
- Add account lockout mechanism  
- Use CAPTCHA or MFA  

## Note

This practice was done in a controlled lab environment for learning purposes only.

[Hydra Output Screenshot](Screenshot-hydra-output.png)
