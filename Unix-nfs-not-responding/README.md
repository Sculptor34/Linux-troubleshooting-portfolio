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
3. Enter command snoop -d eri0 (It filter the IP and look the IP itself)
4. Press stop + A after 1-4 hours. (It depends how many IP in the network)
5. Last steps boot -r
6. The workstation able to boot up as normal startup (If the issue persists, need to assign new IP)

# Commands Used
- ok snoop -d eri0
- ok boot -r
- ok reboot 

# Result
- The workstation successfully to boot up as normal startup

# Notes
- This method should only be used for authorized system recovery.
