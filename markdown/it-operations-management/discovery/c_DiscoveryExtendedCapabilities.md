---
title: Advanced Discovery configuration
description: You can configure several additional components of Discovery such as Application Dependency Mapping, the ECC queue, and extensions for the MID server.
locale: en-US
release: australia
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configuring Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# Advanced Discovery configuration

You can configure several additional components of Discovery such as Application Dependency Mapping, the ECC queue, and extensions for the MID server.

-   **[gMSA configuration for Discovery](gmsa-configuration-for-discovery.md#)**  
Group managed service accounts \(gMSAs\) are managed domain accounts that you use to help secure services. gMSAs can be used for credential-less Discovery.
-   **[Credential-less Discovery with Nmap](nmap-credential-less-discovery.md)**  
If the instance fails to identify a configuration item \(CI\) because of authentication failure, Discovery or Service Mapping can run selected Network Mapper \(Nmap\) commands with a MID Server to collect some basic information about the CI without using credentials.
-   **[PowerShell for Discovery and Service Mapping](../reference/r_PowerShellForDiscovery.md)**  
MID Servers use PowerShell and PowerShell Remoting for accessing configuration items \(CIs\) during horizontal and top-down discovery. Review MID Server parameters and script includes, probe parameters, and credentials for using PowerShell.
-   **[Application Dependency Mapping \(ADM\) for Discovery](../reference/r_ApplicationDependencyMapping.md#)**  
Application Dependency Mapping \(ADM\) discovers CIs by detecting TCP connections between devices.
-   **[Discovery behaviors](c_DiscoveryBehaviors.md)**  
Discovery behaviors determine the probes that Shazzam launches, and from which MID Servers these probes are launched.
-   **[CI deletion strategies for pattern discovery](deletion-strategy.md)**  
When you perform discovery with a pattern, you can choose what to do with configuration items \(CIs\) that are in the Configuration Management Database \(CMDB\) but Discovery can no longer find.
-   **[Configuration file tracking](tracked-config-files.md)**  
The horizontal discovery process can find configuration files that belong to certain applications and add those configuration files to the CMDB. You can track the changes to these files by comparing them to previous versions.
-   **[Change the source name of Discovery results](../task/t_ChangeTheDiscoverySourceName.md)**  
You have the option of changing the source name of discovery results. This might be desirable if Discovery is running on your network together with another discovery product, and you want to use customized identifiers.
-   **[Discovery API plugin](discovery-api-plugin.md)**  
The Discovery API plugin provides APIs for scoped applications and is loaded when the Discovery plugin is activated.
-   **[Running process filters](run-process-filters.md)**  
Filter any processes, using combinations of name and key parameters, from coming back to the instance. Out-of-the box, you can filter OS processes. Filtering processes helps reduce the number of records created, updated, or deleted in the database which can improve overall database performance.
-   **[Configure Discovery to use Event Framework](../task/t_ConfigureDiscoveryEventFramework.md)**  
Configure Discovery to process jobs using the Event Framework method, which enables you to manage discovery throttling effectively and prioritize tasks based on their importance in the queue.
-   **[Post-clone Discovery configuration](PostCloneDiscoveryConfig.md)**  
When a clone occurs, Discovery schedules are copied from the source instance to the target instance. Additional configuration is necessary for these schedules to function correctly on the target instance, helping you properly configure Cloud-based and IP-based Discovery schedules and maintain optimal performance.
-   **[Sensitive data filters](sensitive-data-filters.md)**  
The Discovery Sensitive Data Filters \[discovery\_sensitive\_data\_filter\] table provides a way to help prevent sensitive information from being exposed in the Configuration Management Database \(CMDB\) by applying redaction rules during data collection.

**Parent Topic:**[Configuring Discovery](c_DiscoveryConfiguration.md)

