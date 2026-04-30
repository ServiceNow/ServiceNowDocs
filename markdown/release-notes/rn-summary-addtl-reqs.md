---
title: Additional requirements for all Zurich features and products
description: Cumulative release notes summary on additional requirements for Zurich features and products.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2026-04-08"
reading_time_minutes: 7
breadcrumb: [Release notes summaries for Zurich features, Release notes for upgrading from Yokohama, Learn about the Zurich release, Zurich release notes]
---

# Additional requirements for all Zurich features and products

Cumulative release notes summary on additional requirements for Zurich features and products.

To use certain products, specific setups or third-party requirements are required.

<table id="rn-summary-additional-reqs-table" class="custom-rows"><thead><tr><th class="filter">

Application or feature

</th><th>

Details

</th></tr></thead><tbody><tr><td>

AIOps LEAP

</td><td>

You should have Now Assist for Creator installed to generate playbooks.

</td></tr><tr><td>

Advanced AI Search Management Tools

</td><td>

You must have the User Experience Analytics API application installed from the ServiceNow Store to use Advanced AI Search Management Tools.

</td></tr><tr><td>

Agentic Desktop

</td><td>

The following are required to use AI Desktop Actions:

-   Operating system: Microsoft Windows 11.
-   .NET 9.0 runtime v9.0.10 or .NET 9 Desktop Runtime v9.0.10.
-   No extended monitors are connected.

You must first install the supported Now Assist version of ServiceNow to be able to use the Now Assist AI agents. For more information, see [Install Now Assist AI agents](https://www.servicenow.com/docs/access?context=install-ai-agents-plugins&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

You must enable Next Experience UI Framework before you can use the Now Assist panel.

</td></tr><tr><td>

Applicant Center

</td><td>

The Hiring Core application provides essential data models and shared components for Hiring Experiences. Hiring Core must be activated.

</td></tr><tr><td>

CPQ Configurator

</td><td>

Before implementing CPQ Configurator, you must prepare your environment to use it. For more information, see [Configuring CPQ Configurator](https://www.servicenow.com/docs/access?context=configuring-servicenow-cpq&version=zurich&pubname=zurich-order-management&ft:locale=en-US).

</td></tr><tr><td>

Creator Studio

</td><td>

You must have the App Engine Enterprise license to use Creator Studio.

</td></tr><tr><td>

Dispute Rules Content Pack for Mastercard

</td><td>

This application requires Financial Services Card Operations \(sn\_bom\_credit\_card\) to be installed.

</td></tr><tr><td>

Hiring

</td><td>

The Hiring Core application provides essential data models and shared components for Hiring Experiences. The Hiring Core application must be activated.

</td></tr><tr><td>

Interview management

</td><td>

The Hiring Core application provides essential data models and shared components for Hiring Experiences. The Hiring Core application must be activated.

</td></tr><tr><td>

Knowledge Graph

</td><td>

Ensure that your instance is upgraded to XP7.

</td></tr><tr><td>

Now Assist

</td><td>

The Next Experience UI Framework must be enabled before you can use the Now Assist panel.

</td></tr><tr><td>

Now Assist AI agents

</td><td>

You must first install the supported Now Assist version of the ServiceNow AI Platform to be able to use Now Assist AI agents. For more information, see [Install Now Assist AI agents](https://www.servicenow.com/docs/access?context=install-ai-agents-plugins&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

Next Experience UI Framework must be enabled before you can use the Now Assist panel.

</td></tr><tr><td>

Now Assist for Customer Service Management \(CSM\)

</td><td>

Check your entitlements to determine whether you have access to the Now Assist for CSM application.

</td></tr><tr><td>

Now Assist for FSM

</td><td>

The Now Assist for FSM application requires Field Service Management.

</td></tr><tr><td>

Now Assist for Hardware Asset Management \(HAM\)

</td><td>

The Now Assist for HAM application requires the Hardware Asset Management Pro plus license.

</td></tr><tr><td>

Now Assist for IT Operations Management \(ITOM\)

</td><td>

The Now Assist for ITOM application requires an ITOM Pro Plus or Enterprise Plus license.

</td></tr><tr><td>

Now Assist for Sales Force Automation \(SFA\)

</td><td>

The Now Assist for SFA application requires the Sales Development AI agents.

</td></tr><tr><td>

Now Assist in Document Intelligence

</td><td>

Now Assist in Document Intelligence requires the installation of the Document Intelligence application \(sn\_docintel\) and at least one Now Assist product.

</td></tr><tr><td>

Now Assist in Virtual Agent

</td><td>

[Now Assist in Virtual Agent](https://www.servicenow.com/docs/access?context=now-assist-in-va-landing&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US) requires a license for Virtual Agent and at least one Now Assist product.

</td></tr><tr><td>

Performance Analytics

</td><td>

To use the new data snapshots feature, your instance must be on the RaptorDB Professional database.

</td></tr><tr><td>

Playbooks in Workflow Studio

</td><td>

Download the latest Workflow Studio app in the ServiceNow Store to access the newest features.

</td></tr><tr><td>

RPA Hub

</td><td>

To use the Unattended Robot application, the hardware requirements for a single robot are as follows:

|Resource|Minimum|Recommended|
|--------|-------|-----------|
|CPU|2 cores of Intel 1.8 GHz 64-bit processor|4 cores of Intel 2.4 GHz 64-bit processor|
|RAM|4-GB RAM|8-GB RAM|
|Disk space|Minimum 50-GB free disk space after installing the OS, patches, and base software|Minimum 100-GB free disk space after installing the OS, patches, and base software|

To use the Unattended Robot application, the minimum and recommended hardware requirements for a high density robot are multiplied by the number of runtimes. Multiple robots execute jobs concurrently on the same Windows Server machine. For example, with three users concurrently executing jobs, the minimum hardware requirements for a high density robot are:

-   6 cores of Intel 1.8GHz 64-bit \(6 cores of 1.8GHz 64-bit per runtime\).
-   12 GB of RAM \(4 cores per runtime\).

To use the Unattended Robot application, the software requirements for a standard robot are:

-   Operating system: Microsoft Windows 10, Windows Server 2016, Windows Server 2019, Windows Server 2022.
-   NET framework: Windows 4.7.1 or greater.
-   DPI scaling setting must be deactivated.

To use the Unattended Robot application, the software requirements for a high density robot are:

-   Operating system: Windows Server 2022.
-   NET framework: Windows 4.7.1 or greater.
-   DPI scaling setting must be deactivated.

If you are upgrading to Zurich, verify that you have the latest robot MSI from Zurich installed. The older versions of the robots do not work.

An unattended robot is mapped to only one machine. This is applicable for standard robot.

Virtual Machines \(VMs\) that are used for the Unattended Robot application must be persistent and constantly on.

To use the Attended Robot application, the hardware requirements are:

|Resource|Minimum|Recommended|
|--------|-------|-----------|
|CPU|Intel Processor \(1vCPU\)|Intel Processor \(4vCPU\)|
|RAM|4-GB RAM|8-GB RAM|
|Disk space|Minimum 20-GB free disk space after installing the OS, patches, and base software|Minimum 50-GB free disk space after installing the OS, patches, and base software|

To use the Attended Robot application, the software requirements are:

-   Operating system: Microsoft Windows 10 or Windows Server 2016 or Windows Server 2019.
-   NET framework: Windows 4.7.1 or greater.
-   DPI scaling setting must be deactivated.

An attended robot is mapped to only one user.

To use the RPA Desktop Design Studio application, the hardware requirements are:

|Resource|Minimum|Recommended|
|--------|-------|-----------|
|CPU|Intel Processor \(At least, Core i5\)|Intel Processor \(Core i7\).|
|RAM|4-GB RAM|8-GB RAM|
|Disk space|Minimum 20-GB free disk space after installing the OS, patches, and base software|Minimum 50-GB free disk space after installing the OS, patches, and base software|

To use the RPA Desktop Design Studio application, the software requirements are:

-   Operating system: Microsoft Windows 10 or Windows Server 2016 or Windows Server 2019.
-   NET framework: Windows 4.7.1 or greater.
-   Monitor with 1920x1080p resolution.
-   DPI scaling setting must be deactivated.

</td></tr><tr><td>

Recruitment workspace

</td><td>

The Hiring Core application provides essential data models and shared components for Hiring Experiences. The Hiring Core application must be activated.

</td></tr><tr><td>

SQL API

</td><td>

You must download the SQL API ODBC and JDBC drivers on your client machine. These drivers enable your BI tools and data analysis platforms to connect to your ServiceNow data and run the SQL API queries. You can download the ODBC and JDBC drivers from ServiceNow store.

</td></tr><tr><td>

ServiceNow IDE

</td><td>

ServiceNow IDE uses the public npm registry \(`https://registry.npmjs.org`\) as its default package source. If your network blocks access to this registry, you must have access to an alternate registry to download packages and build applications in the ServiceNow IDE. If access to the public npm registry is blocked on your system, you must configure a private npm registry in your Package Manager user settings in the ServiceNow IDE. For more information, see [Install an npm package from a private registry with the ServiceNow IDE](https://www.servicenow.com/docs/access?context=use-library-private-npm-registry&version=zurich&pubname=zurich-application-development&ft:locale=en-US).

</td></tr><tr><td>

ServiceNow SDK

</td><td>

You must have Node.js and Node Package Manager \(npm\) installed to install the ServiceNow SDK. For more information, see [Install the ServiceNow SDK in an application](https://www.servicenow.com/docs/access?context=install-servicenow-sdk&version=zurich&pubname=zurich-application-development&ft:locale=en-US).

</td></tr><tr><td>

Skills Foundation

</td><td>

-   The Human Resources Scoped App \(sn\_hr\_core\) plugin on Australia family release must be installed for HR profile and Talent job profile synchronization.

**Note:** For earlier releases, you might encounter Restricted Caller Access \(RCA\) approval messages requesting for an update in the access request. Approve the message and re-import the plugin manually.

-   The Skills foundation \(sn\_skills\_int\) v 10.0 for the skills foundation features.
-   The Skills Workspace plugin \(sn\_skills\_int\_ws\) v 6.1 must be installed to access the workspace experience.
-   HRSD integration for SAP SuccessFactors \(sn\_hr\_sf\) Plugin which depends on SuccessFactors \(sn\_successfactors\) spoke v 4.6.1-7 to fetch skills and user skills data.

</td></tr><tr><td>

Smart Assessment Engine

</td><td>

Check your entitlements to determine whether you have access to the collaboration features in the SAE application.

</td></tr><tr><td>

Telecommunications Network Inventory

</td><td>

-   You must install Telecommunications Alarm Management Open API \(sn\_ind\_tmf642\) and Customer Service Problem Management \(sn\_sprb\_mgmt\) plugin to view incident and alert details.
-   You must install the Indoor Mapping plugin \(sn\_map\_core\) to create and manage floor maps for data centers.

</td></tr><tr><td>

Zero Copy Connector for ERP

</td><td>

SAP ECC and SAP S/4 HANA are currently the only available systems that integrate with Zero Copy Connector for ERP.

</td></tr></tbody>
</table>**Parent Topic:**[Release notes summaries for Zurich features](../release-notes-summaries.md)

