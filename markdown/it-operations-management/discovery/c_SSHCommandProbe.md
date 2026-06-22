---
title: SSHCommand probe
description: A probe using the ECC queue topic name SSHCommand executes a shell command on the target host, and returns the resulting output to the sensor.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/discovery/c\_SSHCommandProbe.html
release: zurich
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [List of Discovery probes, Discovery probes and sensors, Using Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# SSHCommand probe

A probe using the ECC queue topic name SSHCommand executes a shell command on the target host, and returns the resulting output to the sensor.

Discovery supports Bourne Shell \(sh\) and Bourne-again Shell \(bash\) commands. Enter shell script commands in the probe's ECC queue name field. The shell script can use variables and file operations supported by the target UNIX shell.

-   The SSH engine is active by default on new instances.
-   Customers on upgraded instances can manually enable ServiceNow SSH for a particular probe by setting the use\_snc\_ssh parameter to true. Alternatively, enable it for all probes on the MID Server by setting the MID Server parameter mid.ssh.use\_snc to true.

**Note:** To discover network devices, such as routers and switches, use [SNMP credentials](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-security/connections-and-credentials/c_SNMPCredentials.md) credentials, not SSH credentials.

-   **[SSHCommand parameters](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery/r_Parameters.md)**  
Several parameters are available for the SSHCommand probe.
-   **[SSHCommand path](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery/c_SSHCommandPath.md)**  
The SSHCommand probe computes the default path from the following sources.
-   **[Shell script options](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery/r_ShellScriptOptions.md)**  
The SSHCommand probe supports the following scripting options in the ECC queue name field.
-   **[Non-privileged SSH commands during probe-based discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery/discovery-ssh-probe-commands.md)**  
These tables display the SSH commands run by Discovery probes on target devices during horizontal discovery. These SSH commands don’t require elevated privileges to run.
-   **[SSH commands requiring a privileged user during probe-based discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery/discovery-ssh-command-require-priv.md)**  
These tables display the SSH commands run by Discovery probes during horizontal discovery. These SSH commands require elevated privileges to run.

**Parent Topic:**[List of Discovery probes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery/r_ListOfDiscoveryProbes.md)

