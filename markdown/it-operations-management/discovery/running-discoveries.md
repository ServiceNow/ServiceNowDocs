---
title: Running discoveries in your network
description: You can run discoveries from schedules or scripts to create configuration items, define subnets, or to find resources in AWS and Azure clouds.
locale: en-US
release: yokohama
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2025-07-08"
reading_time_minutes: 4
breadcrumb: [Discovery, ITOM Visibility, IT Operations Management]
---

# Running discoveries in your network

You can run discoveries from schedules or scripts to create configuration items, define subnets, or to find resources in AWS and Azure clouds.

## MID Server configuration prerequisites

Ensure that your MID Servers are properly configured prior to creating a Discovery schedule.

-   **Supported applications**: Select the applications that are allowed to use the MID Server. You can use the **ALL** application option to allow any application to use the MID Server.
-   **IP ranges**: Define the ranges of IP address the MID Server can scan. To find a MID Server match, the IP range you configure on the Discovery schedule must fall into the ranges that one or more MID Servers can support.

    **Note:** To improve security, limit the range to IP address you control and exclude unnecessary ranges.

-   **Capabilities**: Create the capabilities that the MID Server supports. You can use the **ALL** capability option to allow any application to use the MID Server.

## Discovery configuration prerequisites

Ensure that your MID Servers can authenticate on the devices they find and classify configuration items \(CI\) properly.

-   **Credentials**: Configure the MID Servers with the login credentials they need to query the devices in the network. The MID Server tries all available credentials on each discovered device, then creates an affinity for any successful credentials. For more information, see [Credential affinity for Discovery and Orchestration](https://www.servicenow.com/docs/access?context=c_CredentialAffinity&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).
-   **Classifications**: The device and process classifications provided in the base platform are normally sufficient. Create classifications as needed for the devices, processes, and applications in the network not covered by the default classifiers.

## Get started running a discovery

1.  Use the Discovery Configuration Console to get started with Discovery. The console provides configuration options which let you choose the types of devices, applications, software files, and software CIs you want Discovery to find. If you select a CI to exclude from scanning, the instance disables the related probe or classifier that Discovery uses to identify the CI. See [Discovery Configuration Console](c_DiscoveryConfigurationConsole.md#) to get started.
2.  Determine what type of discovery to run:
    -   [Run a Configuration item \(CI\) discovery](../task/t_CreateADiscoverySchedule.md) to find the devices, computers, and applications on your network. This is the most common type of discovery. Run CI discovery from the Discovery Schedule, where you to set up a recurring schedule or run a discovery on demand. The Discovery Schedule also provides configuration options for MID Servers and the Shazzam port probe.
    -   [Run a Network Discovery](c_NetworkDiscovery.md#) to find the internal IP networks within your organization. If you already know the IP address ranges in your network, it is not necessary to run Network Discovery. It is intended for organizations that do not have complete knowledge of the IP addresses available for Discovery in their networks.
    -   [Run a Serverless Discovery](serverless-discovery.md) to find applications on host machines without the need to discover the host first. Serverless Discovery relies on infrastructure patterns to explore CIs on a host. This kind of discovery skips the scanning and classification phases of discovery. You need an advanced knowledge of patterns to use this type of discovery. Refer to [Patterns and horizontal discovery](c-UsingPatternsForHorizontalDiscovery.md#) to get started with patterns.
3.  After you run a discovery, monitor the results of the discovery and resolve errors if they occurred:
    -   [Use the Discovery status](c_DiscoveryStatus.md) to see a summary of a Discovery and to access the ECC queue, which shows probe and sensor activity, as well as the actual XML payload that is sent to or from an instance.
    -   Use the [Discovery Admin Workspace](discovery-admin-workspace.md) to monitor ongoing Discovery operations.
    -   Use the [Discovery Home page](discovery-home-page.md#) to access details for all schedules, cloud resources \(virtual machines\), discovered devices, and related errors that might have occurred. Error details include possible remediation steps.

**Related topics**  


[Discovery resource utilization](../reference/discovery-resource-utilization.md)

