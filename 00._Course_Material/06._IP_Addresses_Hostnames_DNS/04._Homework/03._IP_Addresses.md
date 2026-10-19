# IP Addresses Exercises

## Exercise 1: Find Public and Private IP Addresses
1. Find your computer's private IP address:
   - On **Mac/Linux**, open a terminal and type: `ifconfig` or `ip addr show`
   - On **Windows**, open Command Prompt and type: `ipconfig` or `ipconfig /all`
   - Note down the private IP address.
2. Find your public IP address:
    - Open a Terminal or Command Prompt and type: `curl ipinfo.io`.
3. Find the subnet mask associated with your private IP address using the same commands above.
4. Find the default gateway (router IP address) using:
   - On **Mac/Linux**: `netstat -nr | grep default`
   - On **Windows**: `ipconfig` and look for "Default Gateway".

## Exercise 2: Subnetting Practice
For each of the following IP addresses with their respective CIDR notation, calculate the following:
- The network address
- The broadcast address
- The range of usable host addresses
- The total number of hosts in this subnet

**1. Target IP address `192.168.1.10/24`.**

**2. Target IP address `81.74.43.132/26`.**

**3. Target IP address `10.43.123.219/20`.**

**4. Target IP address `172.16.5.4/16`.**

<!-- Extra subnetting exercises: https://subnetipv4.com -->