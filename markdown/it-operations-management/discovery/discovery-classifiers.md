---
title: Discovery classifiers
description: A classifier tells Discovery which probes to trigger for the identification and exploration phases of discovery. Classifiers can also trigger the Horizontal Pattern probe, which launches a pattern, rather than additional probes, for identification and exploration.
locale: en-US
release: australia
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Configuring Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# Discovery classifiers

A classifier tells Discovery which probes to trigger for the identification and exploration phases of discovery. Classifiers can also trigger the Horizontal Pattern probe, which launches a pattern, rather than additional probes, for identification and exploration.

The classifier essentially starts the identification stage. Discovery uses it after the classification probe returns important parameters to the instance that tell Discovery what to do next.

In most cases, you do not need to create a classifier or modify a classifier. But if you are having trouble with horizontal discovery, you might want to check the conditions that determine when a classifier runs based on the parameters the classification probe returns to the instance. Or if you want to discover a new type of CI that Discovery does not already find, you can create your own classifier.

## Device, process, and IP address classification

Discovery classification can be broken down into three types: device classification, process classification, and IP address \(or IP scan\) classification:

-   **Device classification**

    The classification of actual device types, such as a computer running Windows, a computer running a flavor or UNIX or LINUX, a router, a switch, or a load balancer, and so on.

    When Discovery identifies a computer CI, it triggers an active processes probe to explore the computer CI further. Discovery compares the results of the active processes probe to the process classification conditions to determine if there is a match.

    ![CI classification workflow](../image/ComputerCIClassificationWorkflow.png "Computer CI classification workflow")

    Starting with the Madrid release, the horizontal discovery process can classify devices using HTTP.

    Of all protocols that Discovery uses \(including WMI, SSH, and SNMP\), HTTP is the lowest priority by default. Discovery uses HTTP classification only if:

    -   Shazzam determines that the ports for HTTP \(80\) and HTTPS \(443\) traffic are open.
    -   The horizontal discovery process fails for the higher priority port probes \(WMI, SSH, and SNMP\) if the ports for those protocols are not open, or if discovery for those protocols fail. The horizontal discovery process can fail, for example, if SSH and SNMP credentials are not configured or are incorrect.

        **Note:** See [Port Probes](../reference/r_PortProbes.md) for more details on how port scanning works and to see the priorities of the different protocols.

    HTTP classification launches the **HTTP Classify** probe to classify the device. The **HTTP - Classify** probe runs a GET request for each device for each HTTP classification. The URL of the request is built as follows: `PROTOCOL://IP:PORT/PATH`, where:

    For more information on port probes, see [Port probes](../reference/r_PortProbes.md). For instructions on creating an HTTP classifier, see [Create an HTTP classification](../task/create-an-http-classifier.md).

-   **Process classification**

    The classification of applications based on the processes that are running.

    Discovery classifies processes during the last phase of discovery: the exploration phase, after identifying devices in the Computer \[cmdb\_ci\_computer\] table and its extensions. Just like device classification, process classification has its own classification criteria and also has the ability to launch probes. Unlike device classification, process classification creates child configuration items \(CI\) with Runs on::Runs relationships. By default, Discovery includes classifications for most common processes.

    If a process matches the classification criteria, Discovery determines whether to run the process handler script. The process handler script modifies the parameter data to help Discovery identify whether the process represents an existing or new application CI. Discovery process handlers prevent the creation of duplicate CIs by filtering out parameters known to have inconsistent values before process classification occurs. Every time Discovery adds or updates an application CI, it also determines the application dependency mapping of the application CI to other CIs in the CMDB.

    ![Process classification workflow](../image/ProcessClassificationWorkflow.png "Process classification workflow")

-   **IP address \(IP scan\) classification**

    IP address discovery is credential-less, meaning that it attempts to identify devices and software based on just the open ports and banners it finds without requiring you to create credentials. If the classification criteria are met for a device in the IP Scan mode, Discovery automatically updates the CI in the CMDB. After a device is properly classified, Discovery launches the exploration probes configured for that class of device and begins gathering detailed information about the CI.

    In the default Discovery system, the Linux classifier triggers eleven exploration probes that return information such as disk size, memory, and the number of current connections. The data from these probes returns at different times and is stored in the ECC Queue until processing is complete.

    This diagram shows the processing flow for classifying and probing devices with an IP scan \(no identifiers\):

    ![IP acan classification](../image/DiscoveryClassificationDiagram.png "IP scan classification")


See [Classification for IP address discovery](ip-address-scanning-classification.md) for more details about the parameters available to classifiers for this type of discovery.

## Classifier criteria

Classifiers also provide criteria that you can use to specify when Discovery should use the classifier under the conditions that you define. The criteria is based on the parameters that a classify probe returns to Discovery. Criteria is constructed with the parameter, an operator, and a value.

**Note:** Condition filters in process classifiers are case-sensitive.

## Classifiers and patterns

Discovery can use patterns, rather than probes, to identify and explore CIs. Discovery triggers patterns from the Horizontal Discovery probe, which can be specified on a classifier. You can create you own patterns and add them, via the Horizontal Discovery probe, to a classifier. See [Add the Horizontal Pattern probe to a classifier](c-UsingPatternsForHorizontalDiscovery.md#) for instructions. You might already be using one of the out-of-box patterns that are provided with Discovery. You can verify this by looking at the classifier to see if the Horizontal Pattern Probe is specified.

## Logging classification debugging information

To log debugging information about classifications, add the following system property. The resulting log entries list the name of each classifier that runs, along with all the names and values that are available to the criteria in the classifier.

<table id="table_a4q_lly_2cb"><thead><tr><th>

System property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

`glide.discovery.debug.classification`

</td><td>

Enables debugging information for process classification. -   **Type**: true \| false
-   **Default Value**: false
-   **Location**: Add to the System Properties \[sys\_properties\] table. For more information, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=australia&pubname=australia-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

</td></tr></tbody>
</table>## What you can do with Discovery classification

-   Create or modify a discovery classifier if you want to classify CIs that Discovery does not already classify, or trigger other probes that are not already on a classifier. You can modify classifiers that Discovery uses in [standard CI discovery](../task/create-discovery-ci-classification.md), [process classifiers for applications](../task/t_CreateAProcessClassification.md), and [classifiers based on IP address scans](../task/t_ClassifForIPAddrScan.md).

    Before you modify any classifiers, [review the parameters](../reference/classification-parameters.md) that are available for each type of classifier.

-   If Windows machines are on your network, you can use the WinRM protocol, rather than WMI, for more efficient lightweight data transfer and remote command execution. By default, Discovery uses WMI. For instructions on the classifier modifications you can make to use WinRM, see [Use Windows Remote Management for classification](../../mid-server/task/t_EnableDeviceClassWinRemoteMgmt.md).
-   If you have Windows computers that are acting as servers and you want them to be classified by their function rather than by the operating system, you can make changes to the criteria of the Windows classifier. See [Reclassify a Windows Workstation machine as a server](../task/t_ReClassWinWorkstnAsSvr.md) for instructions.

