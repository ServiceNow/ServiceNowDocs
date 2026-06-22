---
title: Combined RPA Hub release notes for upgrades from Yokohama to Australia
description: Consolidated page of all release notes for RPA Hub from Yokohama to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-yokohama-australia/australia-yokohama-rpahub-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-06-22"
reading_time_minutes: 22
breadcrumb: [Products combined by family]
---

# Combined RPA Hub release notes for upgrades from Yokohama to Australia

Consolidated page of all release notes for RPA Hub from Yokohama to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family RPA Hub release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Yokohama to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading RPA Hub to Australia

Before you upgrade to Australia, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

Upgrade any of these currently installed Microsoft Software Installers \(MSIs\) by downloading the RPA applications:

-   RPA Desktop Design Studio
-   Attended Robot
-   Unattended Robot
-   Unattended Robot Login Agent

For more information, see [Download the RPA applications from RPA Hub](https://www.servicenow.com/docs/access?context=download-installer-rpa&family=yokohama&ft:locale=en-US).

 The following upgrade information is applicable only when you’re upgrading from San Diego or Tokyo to Yokohama.

 Based on the number of records in the application file table, you may experience a delay while upgrading the RPA Hub applications from Tokyo or earlier releases to Yokohama.

 Before upgrading RPA Hub to Yokohama, you must set the value of the **glide.rollback.blacklist.TableParentChange.change** system property to **false**. If this property doesn't exist in the System Property \[sys\_properties\] table, add the property and set its value to false. For more information on how to add a property, see [Add a system property](https://www.servicenow.com/docs/access?context=t_AddAPropertyUsingSysPropsList&family=yokohama&ft:locale=en-US).

 After you upgrade to Yokohama, the bot process definitions change to the new structure, which is the bot process configuration.

 Although the bot process configuration doesn't replace the bot process completely, most fields are moved from the bot process to the bot process configuration. If you upgrade to Yokohama without updating the system property value, the tables don’t extend the Application File \[sys\_metadata\] table. To update the table changes manually, see the [Restructuring RPA Hub tables to sys\_metadata in Utah and beyond release \[KB1223629\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1223629) article in the Now Support Knowledge Base.

</td></tr><tr><td>

Zurich

</td><td>

Upgrade any of these currently installed Microsoft Software Installers \(MSIs\) by downloading the RPA applications:

-   RPA Desktop Design Studio
-   Attended Robot
-   Unattended Robot
-   Unattended Robot Login Agent

For more information, see [Download the RPA applications from RPA Hub](https://www.servicenow.com/docs/access?context=download-installer-rpa&family=zurich&ft:locale=en-US).

 The following upgrade information is applicable only when you’re upgrading from San Diego or Tokyo to Zurich.

 Based on the number of records in the application file table, you may experience a delay while upgrading the RPA Hub applications from Tokyo or earlier releases to Zurich.

 Before upgrading RPA Hub to Zurich, you must set the value of the **glide.rollback.blacklist.TableParentChange.change** system property to **false**. If this property doesn't exist in the System Property \[sys\_properties\] table, add the property and set its value to false. For more information on how to add a property, see [Add a system property](https://www.servicenow.com/docs/access?context=t_AddAPropertyUsingSysPropsList&family=zurich&ft:locale=en-US).

 After you upgrade to Zurich, the bot process definitions change to the new structure, which is the bot process configuration.

 Although the bot process configuration doesn't replace the bot process completely, most fields are moved from the bot process to the bot process configuration. If you upgrade to Zurich without updating the system property value, the tables don’t extend the Application File \[sys\_metadata\] table. To update the table changes manually, see the [Restructuring RPA Hub tables to sys\_metadata in Utah and beyond release \[KB1223629\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1223629) article in the Now Support Knowledge Base.

</td></tr><tr><td>

Australia

</td><td>

Upgrade any of these currently installed Microsoft Software Installers \(MSIs\) by downloading the RPA applications:

-   RPA Desktop Design Studio
-   Attended Robot
-   Unattended Robot
-   Unattended Robot Login Agent

For more information, see [Download the RPA applications from RPA Hub](https://www.servicenow.com/docs/access?context=download-installer-rpa&family=australia&ft:locale=en-US).

 The following upgrade information is applicable only when you’re upgrading from San Diego or Tokyo to Australia.

 Based on the number of records in the application file table, you may experience a delay while upgrading the RPA Hub applications from Tokyo or earlier releases to Australia.

 Before upgrading RPA Hub to Australia, you must set the value of the **glide.rollback.blacklist.TableParentChange.change** system property to **false**. If this property doesn't exist in the System Property \[sys\_properties\] table, add the property and set its value to false. For more information on how to add a property, see [Add a system property](https://www.servicenow.com/docs/access?context=t_AddAPropertyUsingSysPropsList&family=australia&ft:locale=en-US).

 After you upgrade to Australia, the bot process definitions change to the new structure, which is the bot process configuration.

 Although the bot process configuration doesn't replace the bot process completely, most fields are moved from the bot process to the bot process configuration. If you upgrade to Australia without updating the system property value, the tables don’t extend the Application File \[sys\_metadata\] table. To update the table changes manually, see the [Restructuring RPA Hub tables to sys\_metadata in Utah and beyond release \[KB1223629\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1223629) article in the Now Support Knowledge Base.

</td></tr></tbody>
</table>## New features

Between your current release family and Australia, new features were introduced for RPA Hub.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   **[New third-party AI model provider options available for all Now Assist applications](https://www.servicenow.com/docs/access?context=exploring-large-language-models&family=yokohama&ft:locale=en-US)**

Google Gemini and AWS Claude are available for RPA bot generation skill in addition to Now LLM Service and Azure OpenAI.

-   **[Enhanced ACLs for security measures](https://www.servicenow.com/docs/access?context=installed-with-rpa-hub&family=yokohama&ft:locale=en-US)**

Enhanced access controls for RPA bot generation skill for Now Assist for RPA Hub in compliance with AI security directives.

Access to RPA bot generation skill is now restricted to users with the RPA developer or RPA admin role. These roles contain the RPA Hub Admin user role \(sn\_nowassist\_admin.user\).

-   **[RPA bot generation](https://www.servicenow.com/docs/access?context=rpa-now-assist-studio&family=yokohama&ft:locale=en-US)**

Use the Robotic Process Automation \(RPA\) bot generation skill in RPA Desktop Design Studio to create and edit automations and activities through short text instructions and preview options, accelerating automation development for both new and existing users. For more information about creating automations using Now Assist, see [Create an automation with Now Assist](https://www.servicenow.com/docs/access?context=create-automation-now-assist&family=yokohama&ft:locale=en-US). For more information about creating activities using Now Assist, see [Create an activity with Now Assist](https://www.servicenow.com/docs/access?context=create-activity-now-assist&family=yokohama&ft:locale=en-US).

Enhance automation logic using the **Build automation** option, starting from components or from a blank canvas based on text instructions. For more information, see [Build an automation with Now Assist](https://www.servicenow.com/docs/access?context=build-automation-now-assist&family=yokohama&ft:locale=en-US).

-   **[High density robots](https://www.servicenow.com/docs/access?context=high-density-robots-rpa-hub&family=yokohama&ft:locale=en-US)**

Enable multiple unattended robots to run simultaneously on the same Windows Server machine using the high-density robots feature. These unattended robots run automations in separate Remote Desktop Protocol \(RDP\) sessions. For more information, see [High density robots in Unattended Robot](https://www.servicenow.com/docs/access?context=high-density-robots-uat&family=yokohama&ft:locale=en-US) and [Set up Windows Server machine for high density robots](https://www.servicenow.com/docs/access?context=setup-windows-server-hdr&family=yokohama&ft:locale=en-US).

-   **[Sample automations](https://www.servicenow.com/docs/access?context=sample-automations-rpa-studio&family=yokohama&ft:locale=en-US)**

Use sample automations to jumpstart your automation journey with a library of pre-built automations.

The following unattended and attended sample automations were added to the Sample Explorer and home page of RPA Desktop Design Studio:

    -   User Creation in Badging App
    -   Universal Timezone Converter
    -   Decode Barcode and QR Code to Text
    -   PDF Text to Images
    -   PDF to Word
    -   HTML to CSV
    -   Word Operations
    -   Excel Operations
    -   Highlight Excel Rows
    -   City Weather Reports
    -   Tiff to PDF
    -   Add Word Footer
    -   Date Delta Across Apps
    -   File Ops: Copy, Delete, Move
    -   Extract Data from JSON to Excel
    -   Automate Offer Letters
    -   Summarize Sales Data
    -   Invoice Data Extraction to Excel
    -   Download File from URL
    -   Health Check Bot
-   **[Secure Shell \(SSH\) connector](https://www.servicenow.com/docs/access?context=ssh-connector&family=yokohama&ft:locale=en-US)**

Establish an Secure Shell \(SSH\) connection to a remote server and execute commands in the RPA Desktop Design Studio. In the UNIX environment, SSH is the preferred way to access remote systems. Robots often interact with remote systems such as UNIX servers.

The connector comprises three methods:

    -   Connect: Establishes an SSH connection.
    -   Run Command: Executes commands over an established connection.
    -   Disconnect: Disconnects the session that was established using connect method.
Ensure to install the SSH plugin from the Plugins Manager as a prerequisite.

-   **[Bypassing the legal notice](https://www.servicenow.com/docs/access?context=rpahub-sys-properties&family=yokohama&ft:locale=en-US)**

In RPA Hub, enable the **sn\_rpa\_fdn.bypass\_legal\_notice** system property to authorize the unattended robot to clear the legal notice message set by the system-level policy. This property ensures that a legal notice isn't displayed during the robot's login process.

-   **[What's New tab in the Help Center for RPA Hub](https://www.servicenow.com/docs/access?context=whats-new&family=yokohama&ft:locale=en-US)**

Learn about the following newly released RPA features in your instance in the What's New tab in the Help Center for RPA Hub:

    -   Now Assist for RPA Hub
    -   High density robot
-   **[SAP connector](https://www.servicenow.com/docs/access?context=sap-connector&family=yokohama&ft:locale=en-US)**

The SAP connector helps identify the screens and elements and automating workflows on the SAP GUI. For example, create and save a vendor entry. The SAP Connector is built by Bristlecone, Inc.

-   **[New methods for Universal app connector](https://www.servicenow.com/docs/access?context=universal-app-connector&family=yokohama&ft:locale=en-US)**

In the RPA Desktop Design Studio, the following three new methods for Universal app connector are added.

    -   GetValue: Retrieves a value from an element.
    -   SetValue: Assigns a specified value into an element.
    -   Click: Performs a click action on an element.

</td></tr><tr><td>

Zurich

</td><td>

-   **[Try catch component enhancement](https://www.servicenow.com/docs/access?context=use-general-try-catch&family=zurich&ft:locale=en-US)**

You can now precisely control the scope of Try-Catch blocks by selecting which actions \(components\) to include within exception handling and which to manage outside it. This enhancement provides better control over error handling logic and improves workflow reliability.


 -   **[Role changed for creating, updating, and deleting the Robot License Distribution records](https://www.servicenow.com/docs/access?context=create-lua-record&family=zurich&ft:locale=en-US)**

Role for Create, Update, and Delete ACLs in the Robot License Distribution table is changed from admin to sn\_rpa\_fdn.rpa\_admin.

-   **[Long term stable models](https://www.servicenow.com/docs/access?context=long-term-stable-models&family=zurich&ft:locale=en-US)**

Long term stable \(LTS\) models are part of Now LLM Service and provide longer model stability windows for regulated industries. These models can integrate with tools to provide governance, monitoring, and compliance controls.


-   **[New third-party AI model provider options available for all Now Assist applications](https://www.servicenow.com/docs/access?context=exploring-large-language-models&family=zurich&ft:locale=en-US)**

Google Gemini and AWS Claude are available for RPA bot generation skill in addition to Now LLM Service and Azure OpenAI.

-   **[Python connector](https://www.servicenow.com/docs/access?context=python-connector-rpa&family=zurich&ft:locale=en-US)**

Execute custom Python scripts or files as part of an automation workflow in the RPA Desktop Design Studio.

The connector comprises two methods:

    -   Execute: Runs Python scripts set up in the configuration window.
    -   InvokeScript: Runs Python script on local computers and gets the output.
Ensure to install the Scripting plugin from the Plugins Manager as a prerequisite. Along with Python, VB.NET, C\#, and Javascript connectors are available with this plugin.

-   **[Smart Card authentication](https://www.servicenow.com/docs/access?context=smart-card-il&family=zurich&ft:locale=en-US)**

Use a physical smart card instead of a username and password for logging into a Windows machine.

You can run unattended automations on the machines that use smart cards for authentication. While configuring a robot credential, you can store the smart card username and password to allow the unattended robot to log in to machines that use smart card.

-   **[Enhanced ACLs for security measures](https://www.servicenow.com/docs/access?context=installed-with-rpa-hub&family=zurich&ft:locale=en-US)**

Enhanced access controls for RPA bot generation skill for Now Assist for RPA Hub in compliance with AI security directives.

Access to RPA bot generation skill is now restricted to users with the RPA developer or RPA admin role. These roles contain the RPA Hub Admin user role \(sn\_nowassist\_admin.user\).


</td></tr><tr><td>

Australia

</td><td>

-   **[Try catch component enhancement](https://www.servicenow.com/docs/access?context=use-general-try-catch&family=australia&ft:locale=en-US)**

You can now precisely control the scope of Try-Catch blocks by selecting which actions \(components\) to include within exception handling and which to manage outside it. This enhancement provides better control over error handling logic and improves workflow reliability.


</td></tr></tbody>
</table>## Changes

Between your current release family and Australia, some changes were made to existing RPA Hub features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   **[Changed fields for the Unattended Robot application](https://www.servicenow.com/docs/access?context=set-up-rpa-runtime&family=yokohama&ft:locale=en-US)**

In the Unattended Robot dialog box, the **RPA Hub** field name has been changed to **Instance URL**.

-   **[Embedded Task Automation in RPA Hub](https://www.servicenow.com/docs/access?context=embedded-task-auto-rpa&family=yokohama&ft:locale=en-US)**

Trigger attended bot processes \(attended automations\) from the ServiceNow forms in the Workspace experience apart from initiating them from a classic UI or the Attended Robot application.

-   **[Microsoft Software Installer \(MSI\) compatibility](https://www.servicenow.com/docs/access?context=download-installer-rpa&family=yokohama&ft:locale=en-US)**

Older MSIs that are related to Attended Robot and RPA Desktop Design Studio from the RPA Hub store release versions 7.0.3 and 9.0.0 are compatible and can be used with the current store release version \(12.0.X\) of RPA Hub. For Unattended Robot, the latest MSI must be installed, as it is not backward compatible.

However, there are some limitations:

    -   Any new automation components available in the latest version aren’t available in the older versions. For example, the SSH connector in version 12.0 doesn’t work in older versions.
    -   Components of the same name with different parameters aren’t backward compatible.
If robot machines use older MSIs than the current instance version, they won't have the new features from later versions. For example, features released after version 10.0 won't work in version 10.0 MSIs. Only features from version 10.0 are available in that version.

-   **[TerminateByName component behavior change](https://www.servicenow.com/docs/access?context=use-sysprocess-terminatename&family=yokohama&ft:locale=en-US)**

The TerminateByName component stops processes or applications only within the current user session.


</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Removed

Between your current release family and Australia, some RPA Hub features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Australia, some RPA Hub features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Activation information

Review information on how to activate RPA Hub.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

Install RPA Hub by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=yokohama&ft:locale=en-US).

 Install the Now Assist for RPA Hub application to add the generative AI capability and turn on the Robotic Process Automation \(RPA\) bot generation skill to use generative AI to create automations. For more information about these tasks, see [Configure Now Assist for RPA Hub](https://www.servicenow.com/docs/access?context=configure-now-assist-rpa-hub&family=yokohama&ft:locale=en-US) and [Turn on the RPA bot generation skill](https://www.servicenow.com/docs/access?context=turn-rpa-bot-generation-skill&family=yokohama&ft:locale=en-US).

 For cumulative release notes information on RPA Hub, see [RPA Hub release notes](https://www.servicenow.com/docs/access?context=store-rn-plat-app-engine-rpa-hub&family=yokohama&ft:locale=en-US).

 For cumulative release notes information on RPA Desktop Design Studio, see [RPA Plugin Bundle release notes](https://www.servicenow.com/docs/access?context=store-rn-plat-app-rpa-plugin-bundle&family=yokohama&ft:locale=en-US).

 For cumulative release notes information on Now Assist for RPA Hub, see [Now Assist for RPA Hub release notes](https://www.servicenow.com/docs/access?context=store-rn-plat-app-engine-now-assist-rpa-hub&family=yokohama&ft:locale=en-US).

 If you have previously downloaded the application from the ServiceNow Store and a new version is available, you can update it in your ServiceNow AI Platform instance at **All** &gt; **System Applications** &gt; **All Available Applications**.

</td></tr><tr><td>

Zurich

</td><td>

Install RPA Hub by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=zurich&ft:locale=en-US).

</td></tr><tr><td>

Australia

</td><td>

Install RPA Hub by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=australia&ft:locale=en-US).

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for RPA Hub we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

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

Zurich

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

Australia

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

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for RPA Hub we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

ServiceNow workspaces don’t support mobile devices. For more information about the list of supported browsers, see [Browser support](https://www.servicenow.com/docs/access?context=browser-support&family=yokohama&ft:locale=en-US).

</td></tr><tr><td>

Zurich

</td><td>

ServiceNow workspaces don’t support mobile devices. For more information about the list of supported browsers, see [Browser support](https://www.servicenow.com/docs/access?context=browser-support&family=zurich&ft:locale=en-US).

</td></tr><tr><td>

Australia

</td><td>

ServiceNow workspaces don’t support mobile devices. For more information about the list of supported browsers, see [Browser support](https://www.servicenow.com/docs/access?context=browser-support&family=australia&ft:locale=en-US).

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for RPA Hub, such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   **Accessibility improvements**

Accessibility improvements were completed to support WCAG 2.1 Level AA conformance.


</td></tr><tr><td>

Zurich

</td><td>

-   **Accessibility improvements**

Accessibility improvements were completed to support WCAG 2.1 Level AA conformance.


</td></tr><tr><td>

Australia

</td><td>

-   **Accessibility improvements**

Accessibility improvements were completed to support WCAG 2.1 Level AA conformance.


</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for RPA Hub we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

RPA Hub supports international languages. For more information, see [Internationalization support for RPA Hub](https://www.servicenow.com/docs/access?context=rpa-hub-international-language-support&family=yokohama&ft:locale=en-US).

</td></tr><tr><td>

Zurich

</td><td>

RPA Hub supports international languages. For more information, see [Internationalization support for RPA Hub](https://www.servicenow.com/docs/access?context=rpa-hub-international-language-support&family=zurich&ft:locale=en-US).

</td></tr><tr><td>

Australia

</td><td>

RPA Hub supports international languages. For more information, see [Internationalization support for RPA Hub](https://www.servicenow.com/docs/access?context=rpa-hub-international-language-support&family=australia&ft:locale=en-US).

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for RPA Hub we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   Use generative AI to create and edit automations, activities, and extend automation logic flow through text instructions and preview options in the RPA Desktop Design Studio.
-   Run multiple unattended robots on different user sessions at the same time on the same Windows Server machine using the high-density robots feature.
-   Use new sample automations that were added in the RPA Desktop Design Studio that cater to different use cases.
-   Leverage the communication capabilities of the SSH protocol in the automation processes with the new Secure Shell \(SSH\) connector in the RPA Desktop Design Studio.
-   Use the SAP connector to identify the screens and elements and to automate workflows on SAP graphical user interfaces \(GUI\).
-   Use Google Gemini and Anthropic Claude on AWS as AI model providers for RPA bot generation skill in addition to Now LLM Service and Azure OpenAI.
-   Enhanced access controls for RPA bot generation skill.

 See [Robotic Process Automation \(RPA\) Hub](https://www.servicenow.com/docs/access?context=rpa-main-landing-page&family=yokohama&ft:locale=en-US) for more information.

</td></tr><tr><td>

Zurich

</td><td>

[Zurich Patch 7](https://www.servicenow.com/docs/access?context=zurich-patch-7&family=zurich&ft:locale=en-US)

-   You can now selectively define which actions \(components\) are handled within a Try-Catch block and which are handled outside it.
-   Versions of model provider are now supported for RPA bot generation skill.

 [Zurich Patch 4](https://www.servicenow.com/docs/access?context=zurich-patch-4&family=zurich&ft:locale=en-US)

-   Promote stability with the Long-Term Support \(LTS\) model for generative AI.
-   Only the sn\_rpa\_fdn.rpa\_admin role can create, update, and delete records in the Robot License Distribution table.

 [Zurich Patch 1](https://www.servicenow.com/docs/access?context=zurich-patch-1&family=zurich&ft:locale=en-US)

-   Use Google Gemini and Anthropic Claude on AWS as AI model providers for RPA bot generation skill in addition to Now LLM Service and Azure OpenAI.
-   Use the Python connector to execute custom Python scripts or files as part of an automation workflow.
-   Use a Smart Card authentication for enhanced security.
-   Enhanced access controls for RPA bot generation skill.

 See [Robotic Process Automation \(RPA\) Hub](https://www.servicenow.com/docs/access?context=rpa-main-landing-page&family=zurich&ft:locale=en-US) for more information.

</td></tr><tr><td>

Australia

</td><td>

-   You can now selectively define which actions \(components\) are handled within a Try-Catch block and which are handled outside it.
-   Versions of model provider are now supported for RPA bot generation skill.

 See [Learn about RPA suite of applications](https://www.servicenow.com/docs/access?context=rpa-explore&family=australia&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-yokohama-australia/rn-combined-intro.md)

