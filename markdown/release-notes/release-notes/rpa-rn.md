---
title: RPA Hub release notes
description: The ServiceNow RPA Hub application enables end-to-end automation for your organization. RPA Hub was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 5
---

# RPA Hub release notes

The ServiceNow® RPA Hub application enables end-to-end automation for your organization. RPA Hub was enhanced and updated in the Australia release.

## RPA Hub highlights for the Australia release

-   You can now selectively define which actions \(components\) are handled within a Try-Catch block and which are handled outside it.
-   Versions of model provider are now supported for RPA bot generation skill.

See [Learn about RPA suite of applications](https://www.servicenow.com/docs/access?context=rpa-explore&version=australia&pubname=australia-integrate-applications&ft:locale=en-US) for more information.

**Important:** RPA Hub is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Important information for upgrading RPA Hub to Australia

Upgrade any of these currently installed Microsoft Software Installers \(MSIs\) by downloading the RPA applications:

-   RPA Desktop Design Studio
-   Attended Robot
-   Unattended Robot
-   Unattended Robot Login Agent

For more information, see [Download the RPA applications from RPA Hub](https://www.servicenow.com/docs/access?context=download-installer-rpa&version=australia&pubname=australia-integrate-applications&ft:locale=en-US).

The following upgrade information is applicable only when you’re upgrading from San Diego or Tokyo to Australia.

Based on the number of records in the application file table, you may experience a delay while upgrading the RPA Hub applications from Tokyo or earlier releases to Australia.

Before upgrading RPA Hub to Australia, you must set the value of the **glide.rollback.blacklist.TableParentChange.change** system property to **false**. If this property doesn't exist in the System Property \[sys\_properties\] table, add the property and set its value to false. For more information on how to add a property, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=australia&pubname=australia-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

After you upgrade to Australia, the bot process definitions change to the new structure, which is the bot process configuration.

Although the bot process configuration doesn't replace the bot process completely, most fields are moved from the bot process to the bot process configuration. If you upgrade to Australia without updating the system property value, the tables don’t extend the Application File \[sys\_metadata\] table. To update the table changes manually, see the [Restructuring RPA Hub tables to sys\_metadata in Utah and beyond release \[KB1223629\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1223629) article in the Now Support Knowledge Base.

## New in the Australia release

-   **[Try catch component enhancement](https://www.servicenow.com/docs/access?context=use-general-try-catch&version=australia&pubname=australia-integrate-applications&ft:locale=en-US)**

    You can now precisely control the scope of Try-Catch blocks by selecting which actions \(components\) to include within exception handling and which to manage outside it. This enhancement provides better control over error handling logic and improves workflow reliability.


## Activation information

Install RPA Hub by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

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

## Browser requirements

ServiceNow workspaces don’t support mobile devices. For more information about the list of supported browsers, see [Browser support](../../administer/navigation-and-ui/reference/browser-support.md).

## Accessibility information

-   **Accessibility improvements**

    Accessibility improvements were completed to support WCAG 2.1 Level AA conformance.


## Localization information

RPA Hub supports international languages. For more information, see [Internationalization support for RPA Hub](https://www.servicenow.com/docs/access?context=rpa-hub-international-language-support&version=australia&pubname=australia-integrate-applications&ft:locale=en-US).

## Related ServiceNow applications and features

-   **[Workflow Studio](https://www.servicenow.com/docs/access?context=workflow-studio&version=australia&pubname=australia-build-workflows&ft:locale=en-US)**

    ServiceNow® Workflow Studio integrates with RPA Hub for a seamless robot execution. You can use the Workflow Studio design environment to author flows and actions, as well as view the results they produce.


**Parent Topic:**[App development and low-code release notes](build-automate-rn-landing.md)

