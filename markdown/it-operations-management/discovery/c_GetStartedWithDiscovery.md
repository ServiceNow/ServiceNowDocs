---
title: Exploring Discovery
description: Discovery finds computers, servers, printers, a variety of IP-enabled devices, and the applications that run on them. It can then update the configuration items \(CIs\) in your Configuration Management Database \(CMDB\) with the data it collects.
locale: en-US
release: australia
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Discovery, ITOM Visibility, IT Operations Management]
---

# Exploring Discovery

Discovery finds computers, servers, printers, a variety of IP-enabled devices, and the applications that run on them. It can then update the configuration items \(CIs\) in your Configuration Management Database \(CMDB\) with the data it collects.

## Horizontal discovery and top-down discovery

There are two types of discovery:

-   **Horizontal discovery**

    Horizontal discovery is a technique that Discovery uses to scan your network, find computers and devices, and then populate the CMDB with the CIs it finds. Horizontal discovery creates direct relationships between CIs, such as a `runs on` relationship between an application CI and the actual computer CI that it runs on. Horizontal discovery is not aware of business services and does not create relationships between CIs based on the business service they are in.

-   **Top-down discovery**

    Top-down discovery is a technique that Service Mapping uses to find and maps CIs that are part of business services, such as an email service. For example, top-down discovery can map a website business service by showing the relationships between an Apache Tomcat web server service, a Windows server, and the MSSQL database that stores the data for the business service.

    Typically, Service Mapping and Discovery work together to run horizontal discovery first to find CIs, and then top-down discovery to establish the relationships between business services that you need to know.


## Probes, sensors, and patterns

Discovery uses these components to find CIs:

-   **[Probes and sensors](c_DiscoProcessFlows.md)**

    Probes and sensors are scripts that collect and process data on a host and then update the CMDB. More specifically, probes explore or investigate CIs on your network, and sensors parse the data returned from the probes. Several probes and sensors are provided by default, but you can customize them to find different information, or you can create ones. You can also configure several parameters to control the behavior of a particular probe every time it is triggered.

-   **[Patterns](disco-process-flow-patterns.md)**

    Patterns, like probes and sensors, are a series of operations that also collect data on a host, process it, and update the CMDB. Patterns differ from probes and sensors in that they are written in Neebula Discovery Language \(NDL\) rather than JavaScript, and they are called into action in the later stages of the horizontal discovery process. Default patterns are provided, but you can also customize or create patterns using the Pattern Designer.


## Horizontal discovery phases

The phases of horizontal discovery are:

Discovery follows these phases:

-   **Scanning**

    Discovery sends a probe called Shazzam to the network to see if commonly used ports are open and if these ports can respond to queries. For example, if Shazzam finds a device that responds on port 135, Discovery knows that it’s a Windows server.

-   **Classification**

    If Discovery finds devices or computers, it sends additional probes to find the type of device or the operating system on the device. For example, Discovery sends the WMI probe to a Windows machine to detect the Windows 2012 operating system. Then Discovery uses records called classifiers, which specify the trigger probe or probes that run during the next two phases. If you’re using patterns, the classifier specifies a trigger probe that in turn launches a pattern.

-   **Identification**

    Discovery tries to gather more information about the device and then tries to determine if a CI for the device exists in the CMDB. Discovery then uses additional probes, sensors, and identifiers to update existing CIs in the CMDB or create new ones. Identifiers, also known as identification rules, specify the attributes that the probes look at when reconciling data with the CIs in the CMDB. If you’re using patterns, Discovery uses the appropriate identification rule for the CI type specified in the pattern.

-   **Exploration**

    The identifier launches additional probes configured in the classifier. These probes are especially designed as exploration probes to gather additional information about the device, like the applications running it, and additional attributes, such as memory, network cards, and drivers. Discovery then creates relationships between applications and devices and between applications. If you’re using patterns, the operations in the pattern perform the exploration of the CI.


## Discovery communication through MID Servers

A MID Server, which constantly queries the instance for probes to run, executes the instructions in the probe or in the pattern that the probe specifies. The MID Server then returns the results to the instance, where sensors process it. The MID Server does not retain any discovery information.

The MID Server starts all communications, using SOAP on HTTPS, which means that all communications are secure, and all communications are initiated inside the enterprise's firewall. No special firewall rules or VPNs are required.

Because Discovery is agentless, meaning that it does not require any permanent software to be installed on any computer or device to be discovered, the MID Server uses several techniques to probe devices without using agents. For example, the MID Server uses SSH to connect to a Unix or Linux computer, and then it can run a standard command, as specified in the probe, to gather information. Similarly, it uses the Simple Network Management Protocol \(SNMP\) to gather information from a network switch or a printer.

## Types of discovery

The types of horizontal discovery that the Discovery application can perform are explained in the following table:

<table id="table_b2w_1hl_f2b"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Network discovery

</td><td>

Run this type of discovery to find the internal IP networks within your organization. If you already know the IP address ranges in your network, it is not necessary to run network discovery.

</td></tr><tr><td>

CI discovery

</td><td>

Run this type of discovery to find the devices, computers, and applications on your network. This is essentially the standard type of discovery that you run most often.

</td></tr><tr><td>

Cloud discovery

</td><td>

Run this type of discovery to find AWS and Azure resources in your organization's cloud.

</td></tr><tr><td>

Serverless discovery

</td><td>

Run this type of discovery to find applications on host machines without the need to discover the host first. Serverless discovery relies on patterns to explore CIs on a host.

</td></tr></tbody>
</table>## IP service affinity

IP Service affinity saves the IP service information that is used to successfully find a device and associates it with the IP address of the device. Using this information, Discovery can target the device in subsequent runs with the accurate protocol. Discovery records the IP Service along with the IP address. Discovery can store the successful IP service information in the IP Service Affinity table \[ip\_service\_affinity\].

For example: A network device has both an SSH port and an SNMP port open. By its agentless design, Discovery tries SSH first. However, network devices should be discovered through SNMP. Discovery tries the SSH probe and it fails. This triggers the SNMP probe, which succeeds. With the association between the IP address and the IP service, subsequent discovery runs that target this IP address use SNMP first, because that is the probe that succeeded.

-   **[Horizontal discovery process flow with probes and sensors](c_DiscoProcessFlows.md)**  
The horizontal discovery process passes through the four phases of discovery using probes, which gather information on the target machine, and then sensors, which help Discovery determine what to do with that information.
-   **[Horizontal discovery process flow with patterns](disco-process-flow-patterns.md)**  
Horizontal discovery with patterns has four phases, just as horizontal discovery with probes does. However, for the last two phases, Discovery triggers operations from a pattern, rather than additional sets of probes.

**Parent Topic:**[Discovery](../reference/r-discovery.md)

**Related topics**  


[Discovery setup](discovery-setup.md)

[Discovery monitoring and issue resolution](c_DiscoveryTroubleshooting.md)

