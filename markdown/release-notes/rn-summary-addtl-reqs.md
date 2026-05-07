---
title: Additional requirements for all Australia features and products
description: Cumulative release notes summary on additional requirements for Australia features and products.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-05-04"
reading_time_minutes: 5
breadcrumb: [Release notes summaries for Australia features, Release notes for upgrading from Zurich, Learn about the Australia release, Australia release notes]
---

# Additional requirements for all Australia features and products

Cumulative release notes summary on additional requirements for Australia features and products.

To use certain products, specific setups or third-party requirements are required.

<table id="rn-summary-additional-reqs-table" class="custom-rows"><thead><tr><th class="filter">

Application or feature

</th><th>

Details

</th></tr></thead><tbody><tr><td>

AI Desktop Actions

</td><td>

The following are required to use AI Desktop Actions:

-   Operating system: Microsoft Windows 11.
-   .NET 9.0 runtime v9.0.10 or .NET 9 Desktop Runtime v9.0.10.
-   No extended monitors are connected.

You must first install the supported Now Assist version of ServiceNow to be able to use the Now Assist AI agents. For more information, see [Install Now Assist AI agents](https://www.servicenow.com/docs/access?context=install-ai-agents-plugins&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

You must enable Next Experience UI Framework before you can use the Now Assist panel.

</td></tr><tr><td>

Agentic Contact Center for Banking

</td><td>

This application is dependent on Now Assist for Financial Services Operations \(FSO\). For more information, see [Now Assist for Financial Services Operations \(FSO\) release notes](../financial-services-operations/now-assist-for-financial-services-operations-rn.md).

</td></tr><tr><td>

Customer Service Problem Management

</td><td>

You must install Case Playbook for Complaints \(sn\_complaint\) plugin to use the ADR case type.

</td></tr><tr><td>

Dispute Rules Content Pack for Mastercard

</td><td>

This application requires Financial Services Card Operations \(sn\_bom\_credit\_card\) to be installed.

</td></tr><tr><td>

Financial Services Operations Integration with Verifi

</td><td>

The system property sn\_bom\_credit\_card.is\_verifi\_integration\_enabled must be set to true, so that it will be shipped as false out of the box.

</td></tr><tr><td>

Now Assist

</td><td>

The Next Experience UI Framework must be enabled before you can use the Now Assist panel.

</td></tr><tr><td>

Now Assist AI Agents

</td><td>

You must first install the supported Now Assist version of the ServiceNow AI Platform to be able to use Now Assist AI agents. For more information, see [Install Now Assist AI agents](https://www.servicenow.com/docs/access?context=install-ai-agents-plugins&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

Next Experience UI Framework must be enabled before you can use the Now Assist panel.

</td></tr><tr><td>

Now Assist for FSM

</td><td>

The Now Assist for FSM application requires Field Service Management.

</td></tr><tr><td>

Now Assist in Document Intelligence

</td><td>

Now Assist in Document Intelligence requires the installation of the Document Intelligence application \(sn\_docintel\) and at least one Now Assist product.

</td></tr><tr><td>

Now Assist in Virtual Agent

</td><td>

 

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

If you are upgrading to Australia, verify that you have the latest robot MSI from Australia installed. The older versions of the robots do not work.

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

SQL API

</td><td>

You must download the SQL API ODBC and JDBC drivers on your client machine. These drivers enable your BI tools and data analysis platforms to connect to your ServiceNow data and run the SQL API queries. You can download the ODBC and JDBC drivers from ServiceNow Store.

</td></tr><tr><td>

ServiceNow IDE

</td><td>

ServiceNow IDE uses the public npm registry \(`https://registry.npmjs.org`\) as its default package source. If your network blocks access to this registry, you must have access to an alternate registry to download packages and build applications in the ServiceNow IDE. If access to the public npm registry is blocked on your system, you must configure a private npm registry in your Package Manager user settings in the ServiceNow IDE. For more information, see [Install an npm package from a private registry with the ServiceNow IDE](https://www.servicenow.com/docs/access?context=use-library-private-npm-registry&version=australia&pubname=australia-application-development&ft:locale=en-US).

</td></tr><tr><td>

ServiceNow SDK

</td><td>

You must have Node.js and Node Package Manager \(npm\) installed to install the ServiceNow SDK. For more information, see [Install the ServiceNow SDK in an application](https://www.servicenow.com/docs/access?context=install-servicenow-sdk&version=australia&pubname=australia-application-development&ft:locale=en-US).

</td></tr><tr><td>

Telecommunications Network Inventory

</td><td>

You must install Customer service install base management \(sn\_cs\_sm\_request\) plugin and Remote Hands plugin from the ServiceNow Store to use the Remote Hands feature.

</td></tr><tr><td>

Zero Copy Connector for ERP

</td><td>

SAP ECC and SAP S/4 HANA are currently the only available systems that integrate with Zero Copy Connector for ERP.

</td></tr></tbody>
</table>**Parent Topic:**[Release notes summaries for Australia features](../release-notes-summaries.md)

