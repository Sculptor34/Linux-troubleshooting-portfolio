# The file systems unable to repair

# Overview
- This project demonstrates how to solve file systems corrupted in Unix and SPARC

# Problem
- The system displays file system error during boot up

# Diagnosis
- The workstation unable to boot up normal startup
- The system cannot hard reboot
- Retry reboot after Change the pin slot but it failed (The hardisk is about to corrupt)

# Solution
Steps:
1. boot -s
2. run fsck -y command 
3. Reboot the workstation
5. The hardisk able to boot up as normal startup (If the issue persists, change the new HDD)

# Commands Used
- boot -s
- fsck -y
- boot

# Result
- The workstation successfully to boot up as normal startup

# Notes
- This method should only be used for authorized system recovery.
