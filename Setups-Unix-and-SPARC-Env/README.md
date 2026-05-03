# Setups Environment based on Unix system

# Overview
- This project demonstrates how to setup environment.

# Problem
- The systems is unable to detect HDD once enter command probe-ide
- Suspected the HDD or Environment systems problems

# Diagnosis
- The workstation unable to boot up normal startup
- The system cannot hard reboot 
- Retry boot -a but issue is persists
- Using boot -r command but it failed
- Reslot the HDD and change the pin jumper into first and second slot

# Solution
Steps:
1. power on the workstation and press stop + a
2. Write command set-default to reset the all systems to defaults
3. Enter command printenv to verify the environment
4. Make some changes in that environment
5. Press stop + A and enter command probe-ide to make sure the systems detect HDD
4. Write command boot -a to refresh the systems
5. The workstation able to boot up as normal startup

# Commands Used
- ok probe-ide
- ok set-defaults
- ok printenv
- ok boot -a

# Result
- The workstation successfully to boot up as normal startup

# Notes
- This method should only be used for authorized system recovery.
