# Timeout waiting ARP/RARP packet

# Overview
- This project demonstrates how to solve Timeout waiting ARP/RARP packet in Unix and Sparc.

# Problem
- The system displays Timeout waiting ARP/RARP packet in ok prompt

# Diagnosis
- The workstation unable to boot up normal startup
- The system cannot hard reboot 

# Solution
Steps:
1. Chnage the pin slot into primary/secondry in HDD
2. Make sure all cables in good condition
3. Reboot the workstation
4. Press stop + A
5. Run probe-ide command to confirm HDD is detected (If HDD not detected, suspect HDD/Cablo IDE issue)
6. Reboot one more time and systems is able to boot up as normal startup
   
# Commands Used
- probe-ide
- boot
  
# Result
- The workstation successfully to boot up as normal startup

# Notes
- This method should only be used for authorized system recovery.
