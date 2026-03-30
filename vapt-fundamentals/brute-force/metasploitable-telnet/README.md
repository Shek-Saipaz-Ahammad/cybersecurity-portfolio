# Metasploitable2 Telnet Brute Force (Hydra)

## Objective
In this lab, I tried to perform brute force attack on Telnet service to understand how service-based authentication can be broken.

## What I Did

First, I identified that Telnet service (port 23) is running on the Metasploitable machine.

Then I decided to perform brute force using Hydra tool.

## Approach

- Target IP: Metasploitable machine
- Service: Telnet
- Tool used: Hydra
- Username: msfadmin
- Password list: pass1.txtx

I configured Hydra to try multiple passwords automatically on the Telnet service.

## Result

After running Hydra, it successfully found the correct credentials:
msfadmin / msfadmin

This gave me access to the system through Telnet login.

## What I Learned

- Difference between web login and service login brute force  
- How Hydra works with Telnet service  
- Importance of weak/default credentials  
- Real-world brute force scenario on services  

## Prevention

- Disable Telnet service  
- Use SSH with strong configuration  
- Avoid default credentials  
- Apply account lockout policies  

## Note

This practice was done in a controlled lab environment for learning purposes only.

## Screenshots

- Hydra brute force execution (proof of work): [View Screenshot](Screenshot2-hydra-output.png)  


  

