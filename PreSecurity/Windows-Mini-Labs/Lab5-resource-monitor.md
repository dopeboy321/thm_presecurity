# Lab 5 – Resource Monitor: Detect Unusual Network Activity

## Objective

The goal of this task is to analyze and compare network activity by identifying processes that maintain external network connections. By comparing the data, we aim to identify any unusual or suspicious network activity and understand how processes interact with the network.

Tasks:

- Open resmon.exe and go to the Network tab.
- Find processes maintaining external connections (e.g., to public IPs or using unusual ports).
- Take screenshots and compare with: `netstat -anob`

## Steps Taken

1. Opened Resource Monitor (resmon.exe) and navigated to the Network tab.

2. Identified processes with active external network connections.

3. Noted the external IP addresses and port numbers used by each process (e.g., SearchApp.exe, smartscreen.exe, svchost.exe, etc.).

4. Ran the `netstat -anob` command in CMD to get detailed information about active network connections and their corresponding processes.

5. Cross-checked the information from the Resource Monitor and `netstat` to ensure consistency between the two sources.

6. Ignored out local IP addresses (e.g., `192.168.x.x`) and ignored connections in the `LISTENING` or `CLOSE_WAIT` state as instructed.

## Evidence

Resource Monitor:

<img src="../images/resource_monitored.png" width="1200" />


Netstat Command Output:

<img src="../images/netstat_anob.png" width="500" />

# Findings

- The processes SearchApp.exe, smartscreen.exe, and svchost.exe (running the WpnService) were found maintaining active external connections.

- IP addresses identified (e.g., 191.233.176.51:443, 2.23.77.188:80, 52.113.196.254:443) correspond to Microsoft services (Azure, Bing, Windows Updates).

- All connections were ESTABLISHED, indicating active communication with trusted Microsoft servers, primarily over secure ports (443 for HTTPS).

- No unusual ports or suspicious IP addresses were found, and all connections seemed to follow normal system behavior.


# Relevance for SOC Analyst

- This task demonstrates the process of identifying potentially suspicious network traffic by comparing data from different monitoring tools (Resource Monitor and netstat).
