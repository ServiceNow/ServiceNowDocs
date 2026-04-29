---
title: Agent Client Collector for Visibility - Content reference
description: Review this information for details on OS query scripts, data collected, and definition of terms.
locale: en-US
release: australia
product: Agent Client Collector
classification: agent-client-collector
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 4
keywords: [Agent Client Collector, Agent Client Collector for Visibility, ACC for Visibility]
breadcrumb: [Agent Client Collector reference, Agent Client Collector, IT Operations Management]
---

# Agent Client Collector for Visibility - Content reference

Review this information for details on OS query scripts, data collected, and definition of terms.

## OS module scripts for Agent Client Collector for Visibility - Content \(ACC-VC\)

These platform-specific plugins invoke platform-specific module scripts. Each script outputs to a standard JSON payload regardless of the platform.

<table id="table_dnv_tzy_25b"><thead><tr><th>

Operating System family/plugin

</th><th>

Name of module script

</th></tr></thead><tbody><tr><td rowspan="5">

Linux: acc-f-modules

</td><td>

basic\_inventory.rb \(Starting with ACC-F version 2.10.1, this will not be used.\)

</td></tr><tr><td>

data\_collection.rb

</td></tr><tr><td>

running\_processes.rb

</td></tr><tr><td>

tcp\_connections.rb

</td></tr><tr><td>

 

</td></tr><tr><td rowspan="4">

Windows: acc-f-modules

</td><td>

basic\_inventory.rb \(Starting with ACC-F version 2.10.1, this will not be used.\)

</td></tr><tr><td>

data\_collection.rb

</td></tr><tr><td>

running\_processes.rb

</td></tr><tr><td>

tcp\_connections.rb

</td></tr><tr><td rowspan="3">

macOS Operating Systems: acc-f-modules

</td><td>

basic\_inventory.rb \(Starting with ACC-F version 2.10.1, this will not be used.\)

</td></tr><tr><td>

running\_processes.rb

</td></tr><tr><td>

tcp\_connections.rb

</td></tr><tr><td rowspan="7">

Linux: acc-visibility-modules

</td><td>

installed\_software.rb

</td></tr><tr><td>

file\_systems.rb

</td></tr><tr><td>

storages\_devices.rb \(support for getting physical disk and corresponding disk partitions only\)

</td></tr><tr><td>

network\_adapters.rb

</td></tr><tr><td>

local\_users.rb

</td></tr><tr><td>

enhanced\_inventory.rb

</td></tr><tr><td>

cloud.rb

</td></tr><tr><td rowspan="10">

Windows: acc-visibility-modules

</td><td>

installed\_software.rb

</td></tr><tr><td>

file\_systems.rb

</td></tr><tr><td>

storages\_devices.rb \(support for getting physical disk and corresponding disk partitions only\)

</td></tr><tr><td>

network\_adapters.rb

</td></tr><tr><td>

local\_users.rb

</td></tr><tr><td>

enhanced\_inventory.rb

</td></tr><tr><td>

cloud.rb

</td></tr><tr><td>

sam\_advanced.rb

</td></tr><tr><td>

sam\_processor.rb

</td></tr><tr><td>

intel\_ema.rb

</td></tr><tr><td rowspan="7">

macOS Operating Systems: acc-visibility-modules

</td><td>

installed\_software.rb

</td></tr><tr><td>

file\_systems.rb

</td></tr><tr><td>

storages\_devices.rb \(support for getting physical disk and corresponding disk partitions only\)

</td></tr><tr><td>

network\_adapters.rb

</td></tr><tr><td>

local\_users.rb

</td></tr><tr><td>

enhanced\_inventory.rb

</td></tr><tr><td>

cloud.rb

</td></tr></tbody>
</table>**Note:**

running\_processes.rb and tcp\_connections.rb are interdependent. For an efficient Discovery, keep both tcp\_connections.rb and running\_processes.rb together. Both the files are needed to get the complete data. If one is not there, it will not populate the other data.

To fetch information about all the running\_processes on the macOS, you must provide sudo access to osquery. If this configuration is not made, then running\_processes.rb will only fetch what is triggered by \_servicenow user. For tcp\_connections.rb, you must add ‘sudo lsof’ command in the sudoers file. If this is not done, tcp\_connections.rb will only fetch what is triggered by \_servicenow user.

## Data collected

ACC-VC uses the same classification criteria as IP-based Discovery for classifying as computer or server. The subset of collected data includes the following categories:

-   Basic inventory – Starting with ACC-F version 2.10.1, this will not be used.
-   Data collection - Collects the necessary data for classification and identification of a host CI. This includes host name, serial numbers, and OS information.
-   Installed Software – cmdb\_sam\_sw\_install \(if SAM enabled\) and cmdb\_software\_instance \(if SAM not enabled\)
-   File Systems – cmdb\_ci\_file\_system
-   Storage Devices – cmdb\_ci\_disk and cmdb\_ci\_storage\_device
-   Serial Numbers – cmdb\_serial\_number
-   Network Adapters – cmdb\_ci\_network\_adapter and cmdb\_ci\_ip\_address
-   TCP Connections – cmdb\_tcp
-   Running Processes – cmdb\_running\_process \(ACC-VC also classifies the running processes and creates application CIs in cmdb\_ci\_appl, where possible\)
-   Local User – cmdb\_os\_user \(Populates the local users for all the Operating Systems that ACC-VC supports by adding a new module called local\_user​\)
-   Enhanced inventory – Collects enhanced data \(such CPU info, start\_date, object\_id\) which is not necessary for identifying a unique host.

![This diagram shows the layout and relationships](../image/acc_v_relationships.png "Relationships between host computer, file systems, and storage devices")

## Agent Client Collector terms

-   **Agent Client Collector \(ACC\)**

    The software component installed on target hosts that communicates with the MID Server. Sometimes referred to as Agent. This component is a ServiceNow derivative of Sensu-Go.

-   **Agent Client Collector Framework \(ACC-F\)**

    A ServiceNow base scoped application that leverages ACC and provides core capabilities \(including Check Types, Check Definitions, Policies, and so on\) enabling other ACC scoped applications, including ACC-M and ACC-VC.

-   **Agent Client Collector Monitoring Monitoring \(ACC-M\)**

    A ServiceNow scoped application enabling monitoring use cases.

-   **Agent Client Collector for Visibility - Content \(ACC-VC\)**

    A ServiceNow scoped application that implements push-based Discovery leveraging ACC and ACC-F.

-   **Horizontal IP-based Discovery**

    Traditional Discovery available to customers prior to ACC-VC. It discovers data via Probes and Patterns through the MID Server, requiring the Discovery Plugin.

-   **Modules**

    A subset of discovered data that is populated as part of Discovery. Examples of Modules include: Data Collection, Installed Processes, Serial Numbers, File Systems, Storage Devices, Network Adapters, Running Processes, and TCP Connections.

-   **Push-based Discovery**

    Discover data via ACC, ACC-F, ACC-VC, and the MID Server with a direct push of data from the target host. Discovery does not require specific IP range configuration on a Discovery Schedule or providing Discovery Credentials for target host.

-   **Sensu-Go agent**

    The Free and Open Source project which ACC is derived from.

-   **Virtual Machine Instance**

    A virtual target host running inside of a hypervisor, either on-premise or within a cloud service provider like AWS, GCP, or Microsoft Azure.

-   **Virtual Machine Image**

    A snapshot of a live virtual machine instance persisted to a file system or cloud storage.


-   **[Agent Client Collector for Visibility - Content default checks and policies](../reference/acc-visibility-checks-policies.md)**  
Agent Client Collector for Visibility - Content \(ACC-VC\) provides various checks and policies as well as a business rule.
-   **[Agent Client Collector MID-less installation command parameters](../reference/acc-ics-command-params.md)**  
Description of the command line parameters used during MID-less Agent Client Collector installation.
-   **[Data collected during Agent Client Collector for Visibility - Content file-based Discovery](../reference/data-collected-file-based-discovery.md)**  
The following tables describe the data collected during Agent Client Collector for Visibility - Content file-based Discovery.
-   **[Software edition configuration fields](../reference/software-edition-configuration.md)**  
Description of the software edition configuration fields in use when identifying the edition of Windows software.
-   **[Web usage data collection tables and fields](../reference/web-usage-collection-tables.md)**  
Description of the tables and their fields used when gathering web usage data from your Windows and macOS machines.

**Parent Topic:**[Agent Client Collector reference](../reference/acc-reference.md)

