# NFS not responding

# Overview
- This project demonstrates how to solve NFS not responding.

# Problem
- The systems is hang up

# Diagnosis
- The workstation unable to boot up normal startup
- The system cannot hard reboot 
- Retry boot -a but issue is persists
- Using boot -r command but it failed
- Reslot the HDD and change the pin jumper into first and second slot

# Solution
Steps:
1. power on the workstation and press stop + a
2. Write command boot -s to enter single mode
3. Enter command snoop -d eri0
4. Last steps boot -r
5. The workstation able to boot up as normal startup

# Commands Used
- ok snoop -d eri0
- ok boot -r
- ok reboot 

# Result
- The workstation successfully to boot up as normal startup

# Notes
- This method should only be used for authorized system recovery.
