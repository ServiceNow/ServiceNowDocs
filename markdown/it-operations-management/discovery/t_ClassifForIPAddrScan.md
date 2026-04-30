---
title: Modify classifiers for IP address discovery
description: When you run an IP address type of discovery, port probes scan devices without the use of credentials, and then Discovery can determine which classifiers to use. You can add port probes and additional classifiers for IP address discovery.
locale: en-US
release: zurich
product: Discovery
classification: discovery
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Classification for IP address discovery, Discovery classifiers, Configuring Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# Modify classifiers for IP address discovery

When you run an IP address type of discovery, port probes scan devices without the use of credentials, and then Discovery can determine which classifiers to use. You can add port probes and additional classifiers for IP address discovery.

## Before you begin

Role required: admin

## About this task

Although no credentials are required to scan for Windows or UNIX devices with this type of scan, credentials are still required for SNMP devices. By determining which ports are open on the devices that it scans, IP address classification can discover such things as the type of device \(computer, UPS, etc.\), operating system, running applications, and version numbers.

**Note:** IP address classification attempts to classify devices when no credentials are available; however, Discovery will use credentials when they are available, even when IP address classification is configured.

To use IP address classification, follow these steps:

## Procedure

1.  Determine what ports to use for classification and run a scan program such as Nmap on specific IP addresses to decide which ports reveal the desired information about a device or application.

    The scan can reveal several pieces of data that are useful for configuring classification parameters. An Nmap scan displays port numbers, their state \(open or closed\), their service names, and any version information it can find. From the port information returned in the example below, we can construct criteria to classify UNIX servers \(port 22\), MySQL \(port 3306\), and Apache Tomcat \(port 16000\).

    ![scan output](../image/DiscoveryNmapScan.png)

2.  Add an IP Service and port probe.

    The out-of-box system supplies probes for some of the most common ports, but additional port probes will be needed for effective IP address scanning.

    1.  Navigate to **Discovery Definition** &gt; **IP Services** and click New.
    2.  Create a new IP Service record using the port number and service from the Nmap scan. In this example, we associate the mysql service with port 3306 and add the CI \(sanops02\) on which the service runs to the Available on Related List.

        ![IP service](../image/DiscoveryIPService.png "Discovery IP Service")

    3.  To use Basic Discovery, navigate to **Discovery Definition** &gt; **Functionality Definition** and select the record for **All**.
    4.  Add the new port probes to the list. This tells Discovery which port probes to run for IP address scans.

        ![Discovery functionality definition](../image/DiscoveryFunctionalityDef.png "Discovery functionality definition")

    5.  Save the record and navigate to **Discovery Definition** &gt; **Port Probes** and click **New**.
    6.  Create a port probe using the new IP Service you just defined.

        ![Discovery Port Probe form](../image/DiscoveryPortProbe.png "Discovery Port Probe")

3.  Create a new classification and add the parameter for IP address scanning.

    In this example, we have created an application classifier that will discover Apache Tomcat, based on the port information we received from the Nmap scan. See the following section for details about forming parameters for IP address scans.

    ![Application Classifier form](../image/DiscoveryApplicationClassifier.png "Discovery Application Classifier")

4.  In the Classification Criteria related list, create a criteria filter that determines when this classifier applies to the discovered devices.

    See the [IP address classification parameters](../reference/classification-parameters.md) for a list of the parameters you can use.


## What to do next

Run a IP address discovery through the [Discovery Schedule](t_CreateADiscoverySchedule.md#) to search for devices.

