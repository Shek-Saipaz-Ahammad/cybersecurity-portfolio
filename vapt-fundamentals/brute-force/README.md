# Brute Force Attacks

## Overview
This section demonstrates practical brute force attack scenarios performed on multiple vulnerable environments to understand real-world authentication weaknesses.

The objective was not just tool usage, but identifying login mechanisms, selecting appropriate attack vectors, and executing controlled brute force attempts.

## Labs Covered

- DVWA  
  Performed web login brute force using Hydra by analyzing request parameters and automating credential attempts.

- Metasploitable2 (Telnet)  
  Conducted service-level brute force attack on Telnet to gain unauthorized access using password wordlists.

- Altoro Web Application  
  Executed manual brute force attack using Burp Suite Intruder by capturing and modifying authentication requests.

## Key Learning

- Difference between web-based and service-based brute force attacks  
- Practical usage of Hydra and Burp Suite in real scenarios  
- Identifying weak authentication implementations  
- Importance of wordlists and attack optimization  
- Understanding how attackers approach login systems

## Prevention Awareness

- Implement strong password policies  
- Enable account lockout / rate limiting  
- Use multi-factor authentication (MFA)  
- Monitor and log suspicious login attempts

This practice was performed in a controlled lab environment for educational purposes only.
