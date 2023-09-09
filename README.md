# nmap-cheatsheet
This repository contains information about nmap commands.

## Basic Scanning:

- Scan a single target: nmap target_ip
- Scan multiple targets: nmap target1 target2 target3
- Scan an entire subnet: nmap target_ip_range
- Scan a range of ports: nmap -p start_port-end_port target_ip

## Scan Types:

- TCP SYN scan (default): nmap -sS target_ip
- TCP Connect scan: nmap -sT target_ip
- UDP scan: nmap -sU target_ip

## Output Options:

- Save scan results to a file: nmap -oN output.txt target_ip
- Save results in all formats: nmap -oA output target_ip

## Host Discovery:

- Ping scan: nmap -sn target_ip_range
- Disable DNS resolution: nmap -n target_ip
  
## Service and Version Detection:

- Service/version detection: nmap -sV target_ip
- Detect operating system: nmap -O target_ip

## Scripting Engine (NSE):

- Run a specific NSE script: nmap --script script_name target_ip
- Run default NSE scripts: nmap -sC target_ip

## Timing and Performance:

- Set timing template (0-5): nmap -T4 target_ip
- Adjust scan delay: nmap --scan-delay time target_ip

## Firewall Evasion Techniques:

- Fragmented packets: nmap -f target_ip
- Idle zombie scan: nmap -sI zombie_host target_ip

## Aggressive Scanning:

- Aggressive scan with OS detection: nmap -A target_ip

## Output Filters:

- Show only open ports: nmap --open target_ip

## Advanced Options:

- Use a custom source IP: nmap -S source_ip target_ip

## Common Port Scans:

- Top 1000 ports: nmap -F target_ip
- Top 100 ports: nmap --top-ports 100 target_ip

## Miscellaneous:

- Perform a fast scan (no DNS resolution): nmap -F -n target_ip
