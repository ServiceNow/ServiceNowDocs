---
title: Agent Client Collector for Visibility - Content default checks and policies
description: Agent Client Collector for Visibility - Content \(ACC-VC\) provides various checks and policies as well as a business rule.
locale: en-US
release: xanadu
product: Agent Client Collector
classification: agent-client-collector
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Agent Client Collector for Visibility reference, Agent Client Collector for Visibility, Agent Client Collector, IT Operations Management]
---

# Agent Client Collector for Visibility - Content default checks and policies

Agent Client Collector for Visibility - Content \(ACC-VC\) provides various checks and policies as well as a business rule.

## Policies

**Note:** ACC-VC policies execute at a frequency of once per day. The total data ingested would be approximately 572KB prior to file-based discovery, which runs once per week. This takes into consideration an average of approximately 1500 installed software applications and approximately 500 running processes other than CI data per machine.

-   **Enhanced Discovery Policy**

    Runs off a schedule, which is defaulted to 24 hours \(86400 seconds\). The policy interval can be adjusted, for example to run every 4 hours \(set the interval to 14400\). The ACC-V policy configuration is synced to all agents based on the policy filter defined by ACC-V. Update the following ACC-F system properties if needed:

    -   \[**sn\_agent.disco\_minimum\_threshold\_for\_rediscovery\_minutes**\]: to avoid discovering the system too frequently.
    -   \[**sn\_agent.disco\_disable\_ci\_clobber\_of\_agentless\_disco**\]: to avoid Discovery conflicts.
    -   \[**sn\_agent.disco\_ci\_clobber\_of\_agentless\_disco\_threshold\_days**\]: to avoid Discovery conflicts.
-   **SAM Discovery policy**

    Responsible for capturing the software installed on any Windows endpoint device, such as desktops or servers.

-   **SAM background policy**

    Enables a background job for processing the Osqueryd logs for SAM on Windows and macOS endpoint devices.

-   **SAM background policy \(Non OsqueryD\)**

    Enables a background job to collect SAM information using osqueryi instead of osqueryd.

-   **Software installed policy**

    Responsible for capturing the software installed on all Linux devices and instance CIs. The data collected is stored in the \[cmdb\_sam\_sw\_install\] table. The software installed policy is scheduled to run every 24 hours.


**Note:** Windows endpoint devices include devices that have a Windows operating system and belong to CI class: computer.

See [System properties](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US) for more details. For more details on policies, see [Checks and policies](../concept/checks-policies.md).

## Check type

ACC-VC has the following check types: **Enhanced Discovery**, **SAM Advanced Discovery**, and **Installed Software**.

-   **__Enhanced Discovery__**

    This check type is responsible for invoking the EnhancedDiscoveryHandler script include that processes the payload produced by endpoint\_discovery.rb as executed by ACC.

-   **__SAM Advanced Discovery__**

    This check type is for the Windows SAM Discovery policy that invokes the EnhancedDiscoveryHandler script include for processing the SAM data produced by the sam\_advanced.rb file.

-   **__Installed Software__**

    This check type for the **Software installed policy** that invokes the EnhancedDiscoveryHandler script include for processing the installed software data produced by the installed\_software.rb file.


## Check definitions

There are four Check definitions which are used by the four ACC-V Policies.

-   **Enhanced Discovery**

    This policy configuration is synced to all agents based on the policy filter defined by ACC-V. The Check definition is configured to run with certain assets and determines what gets synced between the Agent and the MID Server. For more detail on policies, see [Checks and policies](../concept/checks-policies.md).

    **Note:**

    For the Agent to retrieve the OS serial numbers and TCP connections along with associated running processes, sudo access for “dmidecode” and “ss” is required on Linux systems. For example, this content could be added to /etc/sudoers or to an individual file in `/etc/sudoers.d/`:

    ```
    Cmnd_Alias AGENT_ACC_V = /usr/sbin/dmidecode -s baseboard-serial-number,/usr/sbin/dmidecode -s chassis-serial-number,/usr/sbin/dmidecode -s system-serial-number,/usr/sbin/dmidecode -s system-uuid,/usr/sbin/ss -tanp
    servicenow ALL=(root) NOPASSWD:AGENT_ACC_V
    ```

-   **SAM background log check**

    The check definition log runs every 8 minutes and performs inline aggregation of data generated from Osqueryd logs. After collecting the data, it writes all the intermediate data results into a temporary marker file which is reused in the next run. This reuse limits the number of log files and disk space needed on target systems.

    **Note:** You may notice a spike in system resource consumption as the background aggregation check runs every interval.

-   **Software installations and usage metrics**

    This check definition collects the data every 24 hours.

-   **Installed software**

    This check definition fetches installed software data for all devices other than Windows and macOS endpoint devices.


## Business rule

The **Enhanced Discovery – On Host CI Delete** business rule triggers the Endpoint Discovery Check when the CI associated with a given CI is deleted from sn\_agent\_cmdb\_ci\_agent.

