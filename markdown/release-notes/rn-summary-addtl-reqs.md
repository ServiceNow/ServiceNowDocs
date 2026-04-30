---
title: Additional requirements for all Yokohama features and products
description: Cumulative release notes summary on additional requirements for Yokohama features and products.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2026-04-08"
reading_time_minutes: 6
breadcrumb: [Release notes summaries for Yokohama features, Release notes for upgrading from Xanadu, Learn about the Yokohama release, Yokohama release notes]
---

# Additional requirements for all Yokohama features and products

Cumulative release notes summary on additional requirements for Yokohama features and products.

To use certain products, specific setups or third-party requirements are required.

<table id="rn-summary-additional-reqs-table" class="custom-rows"><thead><tr><th class="filter">

Application or feature

</th><th>

Details

</th></tr></thead><tbody><tr><td>

AIOps LEAP

</td><td>

You should have the following dependencies installed:

-   Now Assist for Platform
-   Now Assist for Creator \(optional\)

</td></tr><tr><td>

Advanced AI Search Management Tools

</td><td>

You must have the User Experience Analytics API application installed from the ServiceNow Store to use Advanced AI Search Management Tools.

</td></tr><tr><td>

Creator Studio

</td><td>

You must have the App Engine Enterprise license to use Creator Studio.

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

You must first install the supported Now Assist version of ServiceNow to be able to use the Now Assist AI agents. For more information, see [Install Now Assist AI agents](https://www.servicenow.com/docs/access?context=install-ai-agents-plugins&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).

Enable the Next Experience UI Framework before you can use the Now Assist panel.

</td></tr><tr><td>

Now Assist Skill Kit

</td><td>

The Next Experience UI Framework must be enabled to use the Now Assist panel.

</td></tr><tr><td>

Now Assist for App Engine

</td><td>

Check your entitlements to determine whether you have access to the Now Assist for App Engine application.

</td></tr><tr><td>

Now Assist for Customer Service Management \(CSM\)

</td><td>

The Now Assist for CSM application requires a Customer Service Management Pro Plus or Enterprise Plus license.

</td></tr><tr><td>

Now Assist for Field Service Management \(FSM\)

</td><td>

The Now Assist for FSM application requires Field Service Management.

</td></tr><tr><td>

Now Assist for Financial Services Operations \(FSO\)

</td><td>

The Now Assist for FSO application requires a Financial Services Operations Professional Plus or Enterprise Plus license.

</td></tr><tr><td>

Now Assist for Hardware Asset Management \(HAM\)

</td><td>

The Now Assist for Hardware Asset Management \(HAM\) application requires the Hardware Asset Management Pro plus license.

</td></tr><tr><td>

Now Assist for IT Operations Management \(ITOM\)

</td><td>

The Now Assist for ITOM application requires an ITOM Pro Plus or Enterprise Plus license.

</td></tr><tr><td>

Now Assist for IT Service Management \(ITSM\)

</td><td>

The Now Assist for ITSM application requires an IT Service Management Pro Plus or Enterprise Plus license.

</td></tr><tr><td>

Now Assist for Software Asset Management \(SAM\)

</td><td>

The Now Assist for SAM application requires the Software Asset Management Pro plus or the Enterprise plus license.

</td></tr><tr><td>

Now Assist in Document Intelligence

</td><td>

Now Assist in Document Intelligence requires the installation of the Document Intelligence application \(sn\_docintel\) and at least one Now Assist product.

</td></tr><tr><td>

Now Assist in Virtual Agent

</td><td>

[Now Assist in Virtual Agent](https://www.servicenow.com/docs/access?context=now-assist-in-va-landing&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US) requires a license for Virtual Agent and at least one Now Assist product.

</td></tr><tr><td>

Performance Analytics

</td><td>

To use the new data snapshots feature, your instance must be on the RaptorDB Professional database.

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

If you are upgrading to Yokohama, verify that you have the latest robot MSI from Yokohama installed. The older versions of the robots do not work.

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

Service Observability

</td><td>

For the best experience, an APM instance should be installed and an API Key Credential for that instance should be configured on the ServiceNow® platform. Service Observability supports Datadog, Dynatrace, or New Relic.

</td></tr><tr><td>

ServiceNow Add-in for Microsoft 365

</td><td>

You must have Microsoft Outlook 2019 or a later version to use ServiceNow Add-in for Microsoft 365.

</td></tr><tr><td>

ServiceNow SDK

</td><td>

You must have Node.js and Node Package Manager \(npm\) installed to install the ServiceNow SDK. For more information, see [Install the ServiceNow SDK in an application](https://www.servicenow.com/docs/access?context=install-servicenow-sdk&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US).

</td></tr><tr><td>

Skills Foundation

</td><td>

The Skills Workspace plugin \(sn\_skills\_int\_ws\) must be installed to access the workspace experience.

</td></tr><tr><td>

Smart Assessment Engine

</td><td>

Check your entitlements to determine whether you have access to the post-assessment automations and response automation for the SAE application.

</td></tr><tr><td>

Synthetic monitoring

</td><td>

You must do the following before you can use synthetic monitoring:

-   If you have version 1.0, configure at least one proxy agent on the Agent Client Collector. These agents should be the ones you use to monitor the health and performance of the services to be monitored. For more information about proxy agents, see [Using proxy agents in Agent Client Collector](https://www.servicenow.com/docs/access?context=proxy-agent&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US).

Starting with version 1.2, you can run tests from your local Glide instance instead of a proxy agent.

-   Add CIs in the CMDB for the endpoints that you want to monitor.
-   If your endpoints require authentication, configure credentials in the Credentials \[discovery\_credentials\] table.

</td></tr><tr><td>

Talent Feedback

</td><td>

The Skills Foundation plugin \(sn\_skills\_int\) must be installed to be able to request skill feedback on Talent Feedback.

</td></tr><tr><td>

Usage Insights

</td><td>

Customer must use ADC v3 to access the new User Experience Analytics experience. Customers on ADC v2 will have access to the Xanadu version of User Experience Analytics.

</td></tr><tr><td>

Zero Copy Connector for ERP

</td><td>

SAP ECC and S/4 HANA are currently the only available systems that integrate with Zero Copy Connector for ERP.

</td></tr></tbody>
</table>**Parent Topic:**[Release notes summaries for Yokohama features](../release-notes-summaries.md)

