# Configure HDD based on Unix system

# Overview
- This project demonstrates how to configure HDD.

# Problem
- HDD corrupted unable to boot up
- The systems is hang up

# Diagnosis
- The workstation unable to boot up normal startup
- The system cannot hard reboot 
- Retry boot -a but issue is persists
- Using boot -r command but it failed
- Reslot the HDD and change the pin jumper into first and second slot

# Solution
Steps:
1. Change the HDD as suspected the hardware faulty
2. power on the workstation and press stop + a
3. Write command boot -s to enter single mode
4. Configure HDD based on IP address given
5. Write command reboot after finish configuration
6. The workstation able to boot up as normal startup

# Commands Used
- ok boot -s
- ok boot 

# Result
- The workstation successfully to boot up as normal startup

# Notes
- This method should only be used for authorized system recovery.
