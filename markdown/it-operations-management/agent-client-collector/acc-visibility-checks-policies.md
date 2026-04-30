---
title: Agent Client Collector for Visibility - Content default checks and policies
description: Agent Client Collector for Visibility - Content \(ACC-VC\) provides various checks and policies as well as a business rule.
locale: en-US
release: yokohama
product: Agent Client Collector
classification: agent-client-collector
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 5
keywords: [Agent Client Collector, Agent Client Collector for Visibility, ACC for Visibility]
breadcrumb: [Agent Client Collector for Visibility - Content reference, Agent Client Collector for Visibility - Content, Agent Client Collector, IT Operations Management]
---

# Agent Client Collector for Visibility - Content default checks and policies

Agent Client Collector for Visibility - Content \(ACC-VC\) provides various checks and policies as well as a business rule.

## Policies

**Note:** ACC-VC policies execute at a frequency of once per day. The total data ingested would be approximately 572KB. This takes into consideration an average of approximately 1500 installed software applications and approximately 500 running processes other than CI data per machine.

<table id="table_g55_dyy_5dc"><thead><tr><th>

Name

</th><th>

Description

</th><th>

Checks definitions

</th></tr></thead><tbody><tr><td>

Enhanced Discovery

</td><td>

Runs on a schedule, by default every 24 hours \(86400 seconds\). The policy interval can be adjusted, for example to run every 4 hours \(set the interval to 14400\). The ACC-VC policy configuration is synced to all agents based on the policy filter defined by ACC-VC. Update the following ACC-F system properties, if needed:-   **sn\_agent.disco\_minimum\_threshold\_for\_rediscovery\_minutes**: to avoid discovering the system too frequently.
-   **sn\_agent.disco\_disable\_ci\_clobber\_of\_agentless\_disco**: to avoid Discovery conflicts.
-   **sn\_agent.disco\_ci\_clobber\_of\_agentless\_disco\_threshold\_days**: to avoid Discovery conflicts.

</td><td>

Enhanced Discovery

</td></tr><tr><td>

SAM Discovery

</td><td>

Responsible for capturing the software installed on a Windows endpoint device, such as desktops or servers.

</td><td>

Software installations and usage metrics

</td></tr><tr><td>

SAM background

</td><td>

Enables a background job for processing the Osqueryd logs for SAM on Windows and macOS endpoint devices.

</td><td>

SAM background log check

</td></tr><tr><td>

SAM background \(Non OsqueryD\)

</td><td>

Enables a background job to collect SAM information using osqueryi instead of osqueryd.

</td><td>

SAM Background Policy \(Non OsqueryD\)

</td></tr><tr><td>

Software installed

</td><td>

Responsible for capturing the software installed on all devices except for Windows and macOS endpoint devices. The data collected is stored in the \[cmdb\_sam\_sw\_install\] table. Scheduled to run every 24 hours.

</td><td>

installed software

</td></tr><tr><td>

File-based Discovery background policy

</td><td>

Takes the config file \(`AgentFBDUnixParameters.json`, `AgentFBDWindowsParameters.json`, or `WindowsWhiteList.txt`\) as input from the instance to an agent. Information compiled by the configuration console gets put into the config file after running the **Refresh FBD Config Files** scheduled job. This policy scans the system using config file parameters and stores the output on the agent, in the location of the configuration file.

Runs weekly on the agent when file-based discovery is activated on the configuration console. For details, see [File-based Discovery](../../discovery/concept/file-based-discovery.md).

</td><td>

File-based discovery background

</td></tr><tr><td>

File-based Discovery policy

</td><td>

Collects the output file from the agent's background policy. Sends the collected information to the configuration tables and deletes the file after sending. The output file cannot exceed 2MB.Runs weekly on the agent when file-based discovery is activated on the configuration console. For details, see [File-based Discovery](../../discovery/concept/file-based-discovery.md).

**Note:**

-   During file-based discovery on a Windows system, the servicenow user does not have the necessary permissions. Therefore, manually grant the List Folder Contents permission to the folder you want to scan.
-   To ensure successful retrieval of the file version, run the agent as the local system account user instead of the **servicenow** user.

</td><td>

File-based discovery

</td></tr><tr><td>

VISC Get application metric

</td><td>

Retrieves the SaaS application metrics from the agents.For details on enabling SaaS usage monitoring with ACC-VC, see the [SaaS Usage Monitoring with Agent Client Collector \[KB2320193\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2320193) article in the Now Support Knowledge Base.

</td><td>

VISC Get application metric

</td></tr><tr><td>

VISC Get browser extension device init

</td><td>

Initializes the DEX browser extension with the host sysID.

</td><td>

VISC Get browser extension device init

</td></tr><tr><td>

VISC Get browser extension init

</td><td>

Initializes the DEX browser extension with logged-in users.

</td><td>

VISC Get browser extension init

</td></tr></tbody>
</table>**Note:** Windows endpoint devices include devices that have a Windows operating system and belong to CI class: computer.

See [System properties](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US) for more details. For more details on policies, see [Checks and policies](../concept/checks-policies.md).

## Check type

ACC-VC has the following check types: **Enhanced Discovery**, **SAM Advanced Discovery**, and **Installed Software**.

-   **__Enhanced Discovery__**

    This check type is responsible for invoking the EnhancedDiscoveryHandler script include that processes the payload produced by endpoint\_discovery.rb as executed by ACC.

    Used by File-base Discovery.

-   **__SAM Advanced Discovery__**

    This check type is for the SAM Discovery policy that invokes the EnhancedDiscoveryHandler script include for processing the SAM data produced by the sam\_advanced.rb file.

-   **__Installed Software__**

    This check type for the **Software installed policy** that invokes the EnhancedDiscoveryHandler script include for processing the installed software data produced by the installed\_software.rb file.


## Check definitions

<table id="table_pkc_vdz_5dc"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Enhanced Discovery

</td><td>

Synced to all agents based on the policy filter defined by ACC-VC. The Check definition is configured to run with certain assets and determines what gets synced between the agent and the MID Server. For more details on policies, see [Checks and policies](../concept/checks-policies.md).**Note:**

For the agent to retrieve the OS serial numbers and TCP connections along with associated running processes, sudo access for “dmidecode” and “ss” is required on Linux systems. For example, this content could be added to /etc/sudoers or to an individual file in `/etc/sudoers.d/`:

```
Cmnd_Alias AGENT_ACC_V = /usr/sbin/dmidecode -s baseboard-serial-number,/usr/sbin/dmidecode -s chassis-serial-number,/usr/sbin/dmidecode -s system-serial-number,/usr/sbin/dmidecode -s system-uuid,/usr/sbin/ss -tanp
servicenow ALL=(root) NOPASSWD:AGENT_ACC_V
```

</td></tr><tr><td>

SAM background log check

</td><td>

Runs every 8 minutes and performs inline aggregation of data generated from Osqueryd logs. After collecting the data, it writes all the intermediate data results into a temporary marker file which is reused in the next run. This reuse limits the number of log files and disk space needed on target systems. **Note:** You may notice a spike in system resource consumption, as the background aggregation check runs every interval.

</td></tr><tr><td>

Software installations and usage metrics

</td><td>

Collects data every 24 hours.

</td></tr><tr><td>

Installed software

</td><td>

Fetches installed software data for all devices other than Windows and macOS endpoint devices.

</td></tr><tr><td>

File-based discovery background

</td><td>

Runs a file scanning background job on the agent.

</td></tr><tr><td>

File-based discovery

</td><td>

Fetches the file data from the agent.

</td></tr></tbody>
</table>## Business rule

The **Enhanced Discovery – On Host CI Delete** business rule triggers the Endpoint Discovery Check when the CI associated with a given CI is deleted from sn\_agent\_cmdb\_ci\_agent.

