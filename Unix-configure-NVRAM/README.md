# Configure NVRAM based on Unix system

# Overview
This project demonstrates how to configure NVRAM.

# Problem
- IDPROM invalid 

# Diagnosis
- The workstation unable to boot up normal startup
- The system cannot hard reboot 
- Retry boot -a but issue is persists
- Using boot -r command but it failed

# Solution
Steps:
1. Change the NVRAM hardware as suspected the hardware faulty
2. power on the workstation and press stop + a
3. Configure NVRAM based on MAC address generate
4. Write command banner to make sure not displays IDPROM invalid
5. Last steps write command reset-all
6. The workstation able to boot up as normal startup

# Commands Used
ok boot -a
ok boot -r
ok banner
ok reset-all

# Result
The workstation successfully to boot up as normal startup

# Notes
This method should only be used for authorized system recovery.
