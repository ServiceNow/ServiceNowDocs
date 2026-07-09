---
title: RPA Hub release notes
description: The ServiceNow RPA Hub application enables end-to-end automation for your organization. RPA Hub was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 7
---

# RPA Hub release notes

The ServiceNow® RPA Hub application enables end-to-end automation for your organization. RPA Hub was enhanced and updated in the Zurich release.

## RPA Hub highlights for the Zurich release

[Zurich Patch 7](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-7.md)

-   You can now selectively define which actions \(components\) are handled within a Try-Catch block and which are handled outside it.
-   Versions of model provider are now supported for RPA bot generation skill.

[Zurich Patch 4](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-4.md)

-   Promote stability with the Long-Term Support \(LTS\) model for generative AI.
-   Only the sn\_rpa\_fdn.rpa\_admin role can create, update, and delete records in the Robot License Distribution table.

[Zurich Patch 1](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-1.md)

-   Use Google Gemini and Anthropic Claude on AWS as AI model providers for RPA bot generation skill in addition to Now LLM Service and Azure OpenAI.
-   Use the Python connector to execute custom Python scripts or files as part of an automation workflow.
-   Use a Smart Card authentication for enhanced security.
-   Enhanced access controls for RPA bot generation skill.

See [Robotic Process Automation \(RPA\) Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/integrate-applications/rpa-main-landing-page.md) for more information.

**Important:** RPA Hub is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Important information for upgrading RPA Hub to Zurich

Upgrade any of these currently installed Microsoft Software Installers \(MSIs\) by downloading the RPA applications:

-   RPA Desktop Design Studio
-   Attended Robot
-   Unattended Robot
-   Unattended Robot Login Agent

For more information, see [Download the RPA applications from RPA Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/integrate-applications/download-installer-rpa.md).

The following upgrade information is applicable only when you’re upgrading from San Diego or Tokyo to Zurich.

Based on the number of records in the application file table, you may experience a delay while upgrading the RPA Hub applications from Tokyo or earlier releases to Zurich.

Before upgrading RPA Hub to Zurich, you must set the value of the **glide.rollback.blacklist.TableParentChange.change** system property to **false**. If this property doesn't exist in the System Property \[sys\_properties\] table, add the property and set its value to false. For more information on how to add a property, see [Add a system property](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/t_AddAPropertyUsingSysPropsList.md).

After you upgrade to Zurich, the bot process definitions change to the new structure, which is the bot process configuration.

Although the bot process configuration doesn't replace the bot process completely, most fields are moved from the bot process to the bot process configuration. If you upgrade to Zurich without updating the system property value, the tables don’t extend the Application File \[sys\_metadata\] table. To update the table changes manually, see the [Restructuring RPA Hub tables to sys\_metadata in Utah and beyond release \[KB1223629\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1223629) article in the Now Support Knowledge Base.

## New in the Zurich release

-   **[Try catch component enhancement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/integrate-applications/use-general-try-catch.md)**

    You can now precisely control the scope of Try-Catch blocks by selecting which actions \(components\) to include within exception handling and which to manage outside it. This enhancement provides better control over error handling logic and improves workflow reliability.


-   **[Role changed for creating, updating, and deleting the Robot License Distribution records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/integrate-applications/create-lua-record.md)**

    Role for Create, Update, and Delete ACLs in the Robot License Distribution table is changed from admin to sn\_rpa\_fdn.rpa\_admin.

-   **[Long term stable models](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/long-term-stable-models.md)**

    Long term stable \(LTS\) models are part of Now LLM Service and provide longer model stability windows for regulated industries. These models can integrate with tools to provide governance, monitoring, and compliance controls.


-   **[New third-party AI model provider options available for all AI applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/exploring-large-language-models.md)**

    Google Gemini and AWS Claude are available for RPA bot generation skill in addition to Now LLM Service and Azure OpenAI.

-   **[Python connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/integrate-applications/python-connector-rpa.md)**

    Execute custom Python scripts or files as part of an automation workflow in the RPA Desktop Design Studio.

    The connector comprises two methods:

    -   Execute: Runs Python scripts set up in the configuration window.
    -   InvokeScript: Runs Python script on local computers and gets the output.
    Ensure to install the Scripting plugin from the Plugins Manager as a prerequisite. Along with Python, VB.NET, C\#, and Javascript connectors are available with this plugin.

-   **[Smart Card authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/integrate-applications/smart-card-il.md)**

    Use a physical smart card instead of a username and password for logging into a Windows machine.

    You can run unattended automations on the machines that use smart cards for authentication. While configuring a robot credential, you can store the smart card username and password to allow the unattended robot to log in to machines that use smart card.

-   **[Enhanced ACLs for security measures](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/integrate-applications/installed-with-rpa-hub.md)**

    Enhanced access controls for RPA bot generation skill for Now Assist for RPA Hub in compliance with AI security directives.

    Access to RPA bot generation skill is now restricted to users with the RPA developer or RPA admin role. These roles contain the RPA Hub Admin user role \(sn\_nowassist\_admin.user\).


## Activation information

Install RPA Hub by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Additional requirements

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

## Browser requirements

ServiceNow workspaces don’t support mobile devices. For more information about the list of supported browsers, see [Browser support](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/browser-support.md).

## Accessibility information

-   **Accessibility improvements**

    Accessibility improvements were completed to support WCAG 2.1 Level AA conformance.


## Localization information

RPA Hub supports international languages. For more information, see [Internationalization support for RPA Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/integrate-applications/rpa-hub-international-language-support.md).

## Related ServiceNow applications and features

-   **[Workflow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/build-workflows/workflow-studio.md)**

    ServiceNow® Workflow Studio integrates with RPA Hub for a seamless robot execution. You can use the Workflow Studio design environment to author flows and actions, as well as view the results they produce.


**Parent Topic:**[App development and low-code release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/build-automate-rn-landing.md)

