# Altoro Web App Brute Force (Burp Suite)

## Objective
In this lab, I performed a manual brute force attack on the Altoro manual web application login to understand how authentication can be bypassed without automation tools like Hydra.

## What I Did

First, I opened the Altoro vulnerable web application and went to the login page.

Then I entered a random username and password and captured the request using Burp Suite to understand how the login request is sent.

## Approach

- Intercepted login request using Burp Suite Proxy  
- Sent the request to Intruder  
- Selected username/password parameters for attack  
- Used a password wordlist for payloads  
- Observed response length and status to identify valid login  

## Key Point

Instead of using Hydra, this was a manual brute force approach where I analyzed server responses to detect successful login attempts.

## Result

After running the attack, I found the correct credentials based on response differences.

This helped me understand how attackers manually analyze authentication systems.

## What I Learned

- How Burp Suite Intruder works  
- Difference between manual and automated brute force  
- Importance of analyzing server responses  
- How weak login systems can be exploited  

## Prevention

- Implement rate limiting  
- Use CAPTCHA or MFA  
- Lock account after multiple failed attempts  
- Monitor suspicious login activity  

## Screenshots

- Burp request captured during login (proof of work): [View Screenshot](screenshots/burp-capture.png)  
- Intruder attack result showing valid response (evidence): [View Screenshot](screenshots/intruder-result.png)

## Note

This practice was done in a controlled lab environment for learning purposes only.
