---
title: Cybersecurity Controls Accelerator
description: The Cybersecurity Controls Accelerator enables users to easily adopt the CIS Controls from The Center for internet Security to enhance their overall security preparedness and cyber-defense posture.Before you run the GRC: Cybersecurity Controls Accelerator application in your instance, you must download it from the ServiceNow Store.After you have accessed the Cybersecurity Controls Accelerator, you can monitor the controls using these modules.If you use the CIS or ISO authority documents imported from UCF, you can still manage compliance activities using the 285 \(171 CIS and 114 ISO\) automatically monitored indicator templates.
locale: en-US
release: xanadu
product: GRC Common Functions
classification: grc-common-functions
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 9
breadcrumb: [GRC use case accelerators, Common GRC features, Governance, Risk, and Compliance]
---

# Cybersecurity Controls Accelerator

The Cybersecurity Controls Accelerator ™ enables users to easily adopt the CIS Controls from The Center for internet Security ™ to enhance their overall security preparedness and cyber-defense posture.

CIS Control adoption is further enhanced by targeting the leading cybersecurity methodologies to the user's maturity and readiness level.

The Cybersecurity Controls Accelerator contains the CIS Controls version 7.1 authority document, 191 associated CIS citations, and 191 CIS control objectives that are related to the citations.

The [Technology Controls Monitoring Accelerator](../../grc-tech-controls-monitoring-accel/concept/tech-controls-monitoring-accel.md) application \(com.sn\_grc\_infosec\), which must also be downloaded to use the Cybersecurity Controls Accelerator, includes 171 \(26 basic\) predefined indicator templates that are mapped to the CIS Controls. These indicator templates provide automated control validation and continuous monitoring.

## Support for CIS Controls ™ v8

Beginning with the Xanadu release, Cybersecurity Controls Accelerator supports CIS Controls ™ v8 authority documents, citations, and control objectives that are related to the citations.

## Content for CSA CCM v4.0

Beginning with the Xanadu release, Cybersecurity Controls Accelerator supports the Cloud Security Alliance Cloud Controls Matrix \(CSA CCM v4.0\) content such as Authority Document, Citations, and Control Objectives.

**Parent Topic:**[Governance, Risk, and Compliance use case accelerators](../../grc-common/reference/grc-use-case-accelerators.md)

## Download the Cybersecurity Controls Accelerator

Before you run the GRC: Cybersecurity Controls Accelerator application in your instance, you must download it from the ServiceNow Store.

### Before you begin

Prior to running the Cybersecurity Controls Accelerator application, you must download and activate the following GRC applications:

-   GRC: Policy and Compliance Management
-   GRC: Profiles
-   GRC: Technology Controls Monitoring Accelerator

Role required: admin

### Procedure

1.  Follow the instructions for [Download a GRC application from the ServiceNow Store for the first time](../../grc-common/task/download-grc-first-time.md).


## Monitoring cybersecurity controls

After you have accessed the Cybersecurity Controls Accelerator, you can monitor the controls using these modules.

<table id="table_i5x_35b_2jb"><thead><tr><th>

Application/Module

</th><th>

Description

</th></tr></thead><tbody><tr><td colspan="2">

**CIS Controls**

</td></tr><tr><td>

Authority Documents

</td><td>

The **Authority Documents** module provides a list of authority documents, including the CIS Controls v7.1 and v8 authority documents. The authority documents include references to citations and control objectives.The authority documents are stored in the Authority Document table \[sn\_compliance\_authority\_document\].

</td></tr><tr><td>

Citations

</td><td>

The **Citations** module provides a list of citations contained in the CIS Controls v7.1 and v8 authority document. Each citation can include one or more control objectives and refers to:-   Content references
-   Information objects

 The citations are stored in the Citation table \[sn\_compliance\_citation\].

</td></tr><tr><td>

Control Objectives

</td><td>

The **Control Objectives** module provides a list of control objectives associated with the citations in the CIS Controls v7.1 and v8 authority document. Each control objective can include one or more of the following items:-   Entity types
-   Additional entities
-   Policies
-   Controls
-   Indicator Templates
-   Policy Exceptions
-   Issues
-   Risk statements
-   Content references

 The control objectives are stored in the Control Objective table \[sn\_compliance\_policy\_statement\]

</td></tr><tr><td>

Indicator Templates

</td><td>

The **Indicator Templates** module provides a list of predefined indicator templates that are mapped to the CIS Controls. The indicator templates automate control validation and provide continuous monitoring.Indicator Template Reference to Content \[sn\_grc\_m2m\_ind\_temp\_cont\]

</td></tr></tbody>
</table>As previously mentioned, the [Technology Controls Monitoring Accelerator](../../grc-tech-controls-monitoring-accel/concept/tech-controls-monitoring-accel.md) application \(com.sn\_grc\_infosec\) is a dependant application when you download the Cybersecurity Controls Accelerator application. The [Technology Controls Monitoring Accelerator](../../grc-tech-controls-monitoring-accel/concept/tech-controls-monitoring-accel.md) application provides predefined indicator templates that are mapped to the CIS Controls.

**Note:** Should you decide not to implement the Cybersecurity Controls Accelerator application, you can still use the [Technology Controls Monitoring Accelerator](../../grc-tech-controls-monitoring-accel/concept/tech-controls-monitoring-accel.md) to validate compliance with CIS and ISO 27002 via the Unified Compliance Framework \(UCF\) from the Policy and Compliance Management application. For more information, see [Technology Controls Monitoring Accelerator](../../grc-tech-controls-monitoring-accel/concept/tech-controls-monitoring-accel.md).

## UCF controls mapped to indicator templates

If you use the CIS or ISO authority documents imported from UCF, you can still manage compliance activities using the 285 \(171 CIS and 114 ISO\) automatically monitored indicator templates.

The 171 indicator templates are mapped to the 171 CIS control objectives provided with the Cybersecurity Controls Accelerator application.

**Note:** the information in the 26 basic indicator templates is drawn from various ServiceNow ITx applications, as shown in the following example.

|CIS Control|Description|ITx Source applications|
|-----------|-----------|-----------------------|
|CIS Control 1.1|Utilize an active discovery tool to identify devices connected to the organization's network and update the hardware asset inventory.|Discovery|
|CIS Control 1.2|Utilize a passive discovery tool to identify devices connected to the organization's network and automatically update the organization's hardware asset inventory.|Discovery|
|CIS Control 1.4|Maintain an accurate and up-to-date inventory of all technology assets with the potential to store or process information. This inventory shall include all hardware assets, whether connected to the organization's network or not.|Discovery|
|CIS Control 1.5|Ensure that the hardware asset inventory records the network address, hardware address, machine name, data asset owner, and department for each asset and whether the hardware asset has been approved to connect to the network.|Discovery|
|CIS Control 1.6|Ensure that unauthorized assets are either removed from the network, quarantined, or the inventory is updated in a timely manner.|Discovery|
|CIS Control 1.7|Utilize port level access control, following 802.1x standards, to control which devices can authenticate to the network. The authentication system shall be tied into the hardware asset inventory data to ensure only authorized devices can connect to the network.|Discovery|
|CIS Control 1.8|Use client certificates to authenticate hardware assets connecting to the organization's trusted network.|Discovery|
|CIS Control 2.1|Maintain an up-to-date list of all authorized software that is required in the enterprise for any business purpose on any business system.|Software Asset Management|
|CIS Control 2.2|Ensure that only software applications or operating systems currently supported by the software's vendor are added to the organization's authorized software inventory. Unsupported software should be tagged as unsupported in the inventory system.|Software Asset Management|
|CIS Control 2.3|Utilize software inventory tools throughout the organization to automate the documentation of all software on business systems.|Software Asset Management|
|CIS Control 2.4|The software inventory system should track the name, version, publisher, and installation date for all software, including operating systems authorized by the organization.|Software Asset Management|
|CIS Control 2.5|The software inventory system should be tied into the hardware asset inventory so all devices and associated software are tracked from a single location.|CMDB|
|CIS Control 3.1|Utilize an up-to-date SCAP-compliant vulnerability scanning tool to automatically scan all systems on the network on a weekly or more frequent basis to identify all potential vulnerabilities on the organization's systems.|Vulnerability Response|
|CIS Control 3.2|Perform authenticated vulnerability scanning with agents running locally on each system or with remote scanners that are configured with elevated rights on the system being tested.|Vulnerability Response|
|CIS Control 3.6|Regularly compare the results from back-to-back vulnerability scans to verify that vulnerabilities have been remediated in a timely manner.|Vulnerability Response|
|CIS Control 3.7|Utilize a risk-rating process to prioritize the remediation of discovered vulnerabilities.|Vulnerability Response|
|CIS Control 15.1|Maintain an inventory of authorized wireless access points connected to the wired network.|CMDB|
|CIS Control 16.1|Maintain an inventory of each of the organization's authentication systems, including those located onsite or at a remote service provider.|CMDB|
|CIS Control 18.5|Use only standardized and extensively reviewed encryption algorithms.|Discovery|
|CIS Control 18.8|Establish a process to accept and address reports of software vulnerabilities, including providing a means for external entities to contact your security group.|Vulnerability Response|
|CIS Control 19.1|Ensure that there are written incident response plans that defines roles of personnel as well as phases of incident handling/management.|Security Incident Response|
|CIS Control 19.2|Assign job titles and duties for handling computer and network incidents to specific individuals and ensure tracking and documentation throughout the incident through resolution.|Security Incident Response|
|CIS Control 19.3|Designate management personnel, as well as backups, who will support the incident handling process by acting in key decision-making roles.|Security Incident Response|
|CIS Control 19.4|Devise organization-wide standards for the time required for system administrators and other workforce members to report anomalous events to the incident handling team, the mechanisms for such reporting, and the kind of information that should be included in the incident notification.|Security Incident Response|
|CIS Control 19.6|Publish information for all workforce members, regarding reporting computer anomalies and incidents to the incident handling team. Such information should be included in routine employee awareness activities.|Security Incident Response|
|CIS Control 19.8|Create an incident scoring and prioritization schema based on known or potential impact to your organization. Utilize score to define frequency of status updates and escalation procedures.|Security Incident Response|

Control objectives that are downloaded from UCF have UCF as the source, as shown below.

![Control objective obtained from UCF](../image/ucf-control-objective.png "UCF control objective")

If you click the **Citations** related list, you can see that two citations are present: one obtained from CIS and one from ISO 27001 authority documents from UCF.

![Citations included in a UCF control objective](../image/ucf-control-objective-citations.png "Citations included in UCF control objective")

These citations allow you to use the CIS controls downloaded from UCF, instead of the CIS Controls included with the Cybersecurity Controls Accelerator application while still associating the controls with the indicator templates provided.

If you want to associate this UCF control objective to similar indicator templates, you can click the **Indicator Templates** related list and then click the **Suggested** button.

![Indicator Templates related list](../image/ucf-control-objective-suggested.png "Indicator Templates related list")

A list of indicator templates that may apply to the selected control objective are shown.

![Suggested indicator templates](../image/suggested-indicator-templates.png "Suggested indicator templates")

Select the indicator templates you want to map to the UCF control objective and click **Add**.

![Mapping an indicator template to a UCF control objective](../image/suggested-indicator-templates-add.png "Mapping an indicator template to a UCF control objective")

