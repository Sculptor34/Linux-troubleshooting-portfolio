# The systems blank screen

# Overview
- This project demonstrates how to solve blank screen issue.

# Problem
- The workstation hang at CDE environment

# Diagnosis
- Remote the systems to confirm not HDD issue
- The systems able to remote as suspected the systems or hardware issue

# Solution
Steps:
1. Changethe display cable to confirm not hardware issue
2. If the issue persists, as suscpetd the systems itself problem
3. RSH the system using own PC/Laptop
4. Run cd / command and ls -a
5. soft link ADS_common to /tools/ADS_common/SOLARIS to ADS_Common
6. Reboot the workstation
7. The systems is able to boot up and displays the login screen

# Commands Used
- ok boot -s
- ok boot 

# Result
- The workstation successfully to boot up as normal startup

# Notes
- This method should only be used for authorized system recovery.
