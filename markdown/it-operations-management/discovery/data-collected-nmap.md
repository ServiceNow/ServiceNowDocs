---
title: Nmap commands and data collected with credential-less Discovery
description: Nmap executes in phases when collecting data and runs a controlled set of safe commands with two patterns for exploring applications and devices.
locale: en-US
release: yokohama
product: Discovery
classification: discovery
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 8
breadcrumb: [Credential-less Discovery with Nmap, Advanced Discovery configuration, Discovery, ITOM Visibility, IT Operations Management]
---

# Nmap commands and data collected with credential-less Discovery

Nmap executes in phases when collecting data and runs a controlled set of safe commands with two patterns for exploring applications and devices.

## Data returned by Nmap from host Discovery

Nmap returns the following data for a host it determines is up:

-   **Operating system family**: If the operating system family is one of the six supported server operating system families, then a host CI associated with the appropriate server class is used to create or update the host CI. If the operating system family returned by Nmap is not one of the supported server operating systems, then a host CI is created or updated using the base Hardware \[cmdb\_ci\_hardware\] class.
-   **MAC address**: If the scanned host is located on the same subnet as the Windows MID Server host that is executing the Nmap commands, then Nmap returns the remote host's MAC address.

## Commands run by Nmap during host Discovery

The MID Server passes the IP address of a remote host to the Nmap command and a set of ports, taken from the IP Service table. The host must be reported by Nmap to be up. The host is up if the port state returned by Nmap is **open** or **open/filtered**. If the host is reported to be up, then the operating system family returned is examined to determine the class used to create or update the host CI.

<table id="table_lcs_rnn_sbb"><thead><tr><th>

Command

</th><th>

Description

</th></tr></thead><tbody><tr><td>

-PS

</td><td>

TCP SYN option determines if the host is online. This option that sends an empty, raw TCP packet with the SYN flag set to all the specified ports on the scan list. Nmap reports the host is online if a SYN/ACK TCP packet is returned and if an RST is returned, indicating that the port is closed. The Nmap host machine tears down the nascent connection with an RST, instead of an ACK, since the SYN/ACK response is unexpected from its perspective. If multiple port probes are specified, they are sent in parallel.Requirements:

-   Raw packet privileges.
-   Must run as root on UNIX.
-   Administrator privileges on Windows.

</td></tr><tr><td>

-PA

</td><td>

Detects packet-filtering devices. This option is a TCP ACK host Discovery, using a specified list of ports. If no list is defined, the default port 80 is used.Nmap sends an empty, raw TCP packet with the ACK flag set. This action acknowledges data over an established TCP connection, causing the remote host to respond with an RST packet. If the remote host does respond with an RST packet, Nmap knows the host is online. The ACK ping probe may get past packet filtering of TCP SYN packets by stateless packet filtering, network entities, such as firewalls, routers, and host routing tables/firewall software. Stateful firewalls drop unexpected packets, causing the ACK packet to be dropped, which increases the likelihood of the SYN TCP probe getting through.

 Requirements:

-   Raw packet privileges.
-   Must run as root on UNIX.
-   Administrator privileges on Windows .

**Note:** Both Ping SYN \(-PS\) and Ping ACK \(-PA\) packets types can be configured together in the same scan attempt.

</td></tr><tr><td>

-O

</td><td>

Enables OS detection against a remote hostm providing the vendor name, underlying OS, OS generation, and device type, such as a router or a switch.Nmap uses TCP/IP stack fingerprinting to determine the OS family running on the host. Nmap sends a series of TCP and UPD packets to the host and examines the responses. After testing the responses thoroughly, Nmap compares results to its **nmap-os-db** database and prints the OS details, if there is a match. If Nmap is not able to guess the OS, and at least one open port and one closed port were found, then it generates a fingerprint and a URL to submit to `nmap.org`.

 OS detection does not use scripts from the Nmap Scripting Engine \(NSE\). OS detection runs after Application/Service Version detection, which helps the accuracy of OS Detection. However, the results of the two scan types might be contradictory. OS Detection runs at the TCP transport layer, while Application/Service Version Detection runs at a higher level in the TCP stack.

 Requirements:

-   Raw packet privileges.
-   Must run as root on UNIX.
-   Administrator privileges on Windows .

</td></tr><tr><td>

-p

</td><td>

List of ports to scan.

</td></tr><tr><td>

-T4

</td><td>

Nmap aggressive timing template.

</td></tr><tr><td>

-v

</td><td>

Enable verbose detail. This command is normally used to provide progress indication to viewers of standard output. However, it can cause the Nmap Scripting Engine \(NSE\) scripts to provide additional detail.

</td></tr><tr><td>

-Pn

</td><td>

Disable the default ping. This command skips the initial Nmap host discovery scan phase and treats all hosts as if they are online. Use this command if you want a port scan even if the set of ports run by the default Discovery probes will not find an open port.

</td></tr><tr><td>

-r

</td><td>

Scan ports consecutively, without randomizing.

</td></tr><tr><td>

--reason

</td><td>

Explains why Nmap classified a port with a specific state.

</td></tr><tr><td>

--system-dns

</td><td>

Use the DNS resolver of the operating system for reverse DNS lookup, rather than the DNS name servers. This option is slower than using DNS servers, since it can only resolve one IP address at a time, while multiple rDNS requests are performed in parallel. However, the value returned matches the value returned by the MID Server that is used to create host CIs.

</td></tr><tr><td>

-X -

</td><td>

Redirects `stdout` to a XML file.

</td></tr><tr><td>

2&gt; &lt;file-path&gt;

</td><td>

Redirects errors messages written by Nmap to `stderr` to the specified file.

</td></tr></tbody>
</table>## Data returned by Nmap during application Discovery

Nmap returns the following application data from a host it determines is up:

-   **Port state**:
    -   **open**: An application is actively accepting TCP \(or UDP\) packets on the port.
    -   **open\|filtered**: Nmap cannot determine if the port is open or filtered. An open port may not return a response when using Nmap’s UDP, IP protocol, FIN, NULL and Xmas scans.
-   **Service name**: Name of the service actively accepting TCP \(or UDP\) packets on the service port.
-   **Service product**: Name of the application running on the open port, as identified by Nmap.
-   **Extra service information**: Any additional information returned by Nmap that Discovery can use to identify the application.

## Commands run by Nmap during application Discovery

The MID Server passes one IP address for a remote host to the Nmap command and one port to scan. Nmap attempts to identify the application actively listening on the port and then determines whether it should create a new CI or update an existing one. The host must be reported by Nmap to be up.

Nmap uses this information to determine which course to take:

-   Service product
-   Service name
-   Extra service information
-   State of the scanned port

    **Note:** The service product and service name values cannot be NULL, and the service name cannot end with a question mark. Nmap appends a question mark to a service name when it guesses at the application listening on the scanned port. The instance does not create or update an application CI if Nmap cannot retrieve the application name from its static `nmap-services` registry file.


<table id="table_ghc_kkt_bbb"><thead><tr><th>

Command

</th><th>

Description

</th></tr></thead><tbody><tr><td>

-sS

</td><td>

TCP SYN \(stealth\) port scan. This is the default scan option and never completes TCP connections. Scans can differentiate between ports that are **open**, **closed**, or **filtered**.TCP SYN scan implements a half-open reset that aborts the request before the connection can be established. The port is **open** \(the application is listening\) if a SYN/ACK is returned. The port is **closed** if an RST is returned. If no response is received after multiple retransmissions, the port is marked **filtered**. The port is also marked filtered if an ICMP unreachable error \(type 3, code 1,2,3,9,10,13\) is received.

 Requirements:

-   Raw packet privileges
-   Must run as root
-   Windows administrator privileges

</td></tr><tr><td>

-sV

</td><td>

Probes open ports to determine the service protocol, application name, version number, hostname, device type, OS Family and miscellaneous details such as the SSH protocol version.When Nmap receives a response it cannot match to the database it prints out a fingerprint and URL for submission to **nmap.org**. If looks for the port number in its static `nmap-services` registry file to determine the name of an application service that might be actively listening on the port. The service name returned by Nmap is appended with a question mark, indicating that Nmap had to guess at its identity. The instance does not create or update an application CI when Nmap guesses at the application running on an open port.

**Note:** This command does not require raw-packet privileges.

</td></tr><tr><td>

--datadir

</td><td>

Path to the directory containing the safe set of Nmap scripts to be run during Application/Version detection.

</td></tr><tr><td>

-p

</td><td>

Single port to scan.

</td></tr><tr><td>

-T4

</td><td>

Nmap aggressive timing template.

</td></tr><tr><td>

-v

</td><td>

Enable verbose detail. This command is normally used to provide progress indication to viewers of standard output. However, it can cause the Nmap Scripting Engine \(NSE\) scripts to provide additional detail.

</td></tr><tr><td>

-Pn

</td><td>

Disable the default ping. This command skips the initial Nmap host discovery scan phase and treats all hosts as if they are online. Use this command if you want a port scan even if the set of ports run by the default Discovery probes will not find an open port.

</td></tr><tr><td>

-r

</td><td>

Scan ports consecutively, without randomizing.

</td></tr><tr><td>

--reason

</td><td>

Explains why Nmap classified a port with a specific state.

</td></tr><tr><td>

--system-dns

</td><td>

Use the DNS resolver of the operating system for reverse DNS lookup, rather than the DNS name servers. This option is slower than using DNS servers, since it can only resolve one IP address at a time, while multiple rDNS requests are performed in parallel. However, the value returned matches the value returned by the MID Server that is used to create host CIs.

</td></tr><tr><td>

-X -

</td><td>

Redirects `stdout` to a XML file.

</td></tr><tr><td>

2&gt; &lt;file-path&gt;

</td><td>

Redirects errors messages written by Nmap to `stderr` to the specified file.

</td></tr></tbody>
</table>**Parent Topic:**[Credential-less Discovery with Nmap](../concept/nmap-credential-less-discovery.md)

