# nmap-cheatsheet

![image](https://github.com/nenomg/nmap-cheatsheet/assets/105873794/fd7bfbd0-4cb1-4153-9015-f315f713ddd3)


This repository contains information about nmap commands.


## Basic Scanning:

- Scan a single target:
  
  ```terminal
  nmap target_ip
  ```
- Scan multiple targets:
  
  ```terminal
  nmap target1 target2 target3
  ```
- Scan an entire subnet:
  ```terminal
  nmap target_ip_range
  ```
- Scan a range of ports:

  ```terminal
  nmap -p start_port-end_port target_ip
  ```

## Scan Types:

- TCP SYN scan (default):
  
  ```terminal
  nmap -sS target_ip
  ```
- TCP Connect scan:

  ```terminal
  nmap -sT target_ip
  ```
- UDP scan:
  
  ```terminal
  nmap -sU target_ip
  ```

## Output Options:

- Save scan results to a file:

  ```terminal
  nmap -oN output.txt target_ip
  ```
- Save results in all formats:

  ```terminal
  nmap -oA output target_ip
  ```

## Host Discovery:

- Ping scan:

  ```terminal
  nmap -sn target_ip_range
  ```
- Disable DNS resolution:

  ```terminal
  nmap -n target_ip
  ```
  
## Service and Version Detection:

- Service/version detection:

  ```terminal
  nmap -sV target_ip
  ```
- Detect operating system:

  ```terminal
  nmap -O target_ip
  ```

## Scripting Engine (NSE):

- Run a specific NSE script:

  ```terminal
  nmap --script script_name target_ip
  ```
- Run default NSE scripts:

  ```terminal
  nmap -sC target_ip
  ```
  
## Timing and Performance:

- Set timing template (0-5):

  ```terminal
  nmap -T4 target_ip
  ```
- Adjust scan delay:

  ```terminal
  nmap --scan-delay time target_ip
  ```

## Firewall Evasion Techniques:

- Fragmented packets:

  ```terminal
  nmap -f target_ip
  ```
- Idle zombie scan:

  ```terminal
  nmap -sI zombie_host target_ip
  ```

## Aggressive Scanning:

- Aggressive scan with OS detection:

  ```terminal
  nmap -A target_ip
  ```

## Output Filters:

- Show only open ports:

  ```terminal
  nmap --open target_ip
  ```

## Advanced Options:

- Use a custom source IP:

  ```terminal
  nmap -S source_ip target_ip
  ```
  
## Common Port Scans:

- Top 1000 ports:

  ```terminal
  nmap -F target_ip
  ```
- Top 100 ports:

  ```terminal
  nmap --top-ports 100 target_ip
  ```

## Miscellaneous:

- Perform a fast scan (no DNS resolution):

  ```terminal
  nmap -F -n target_ip
  ```
