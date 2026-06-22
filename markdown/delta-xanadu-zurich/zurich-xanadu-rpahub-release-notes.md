---
title: Combined RPA Hub release notes for upgrades from Xanadu to Zurich
description: Consolidated page of all release notes for RPA Hub from Xanadu to Zurich.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/delta-xanadu-zurich/zurich-xanadu-rpahub-release-notes.html
release: zurich
topic_type: reference
last_updated: "2026-06-22"
reading_time_minutes: 30
breadcrumb: [Products combined by family]
---

# Combined RPA Hub release notes for upgrades from Xanadu to Zurich

Consolidated page of all release notes for RPA Hub from Xanadu to Zurich.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family RPA Hub release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Xanadu to Zurich.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading RPA Hub to Zurich

Before you upgrade to Zurich, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

Upgrade any of these currently installed Microsoft Software Installers \(MSIs\) by downloading the RPA applications:

-   RPA Desktop Design Studio
-   Attended Robot
-   Unattended Robot
-   Unattended Robot Login Agent

For more information, see [Download the RPA applications from RPA Hub](https://servicenow-staging.fluidtopics.net/access?context=download-installer-rpa&family=xanadu&ft:locale=en-US).

 The following upgrade information is applicable only when you’re upgrading from San Diego or Tokyo to Xanadu.

 Based on the number of records in the application file table, you could experience a potential delay while upgrading the RPA Hub applications from Tokyo or earlier releases to Xanadu.

 Before upgrading RPA Hub to Xanadu, you must set the value of the **glide.rollback.blacklist.TableParentChange.change** system property to **false**. If this property doesn't exist in the System Property \[sys\_properties\] table, add the property and set its value to false. For more information on how to add a property, see [Add a system property](https://servicenow-staging.fluidtopics.net/access?context=t_AddAPropertyUsingSysPropsList&family=xanadu&ft:locale=en-US).

 After you upgrade to Xanadu, the bot process definitions change to the new structure, which is the bot process configuration.

 Although the bot process configuration doesn't replace the bot process completely, most fields are moved from the bot process to the bot process configuration. If you upgrade to Xanadu without updating the system property value, the tables don’t extend the Application File table. To update the table changes manually, see the [Restructuring RPA Hub tables to sys\_metadata in Utah and beyond release](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1223629) article in the Now Support knowledge base.

</td></tr><tr><td>

Yokohama

</td><td>

Upgrade any of these currently installed Microsoft Software Installers \(MSIs\) by downloading the RPA applications:

-   RPA Desktop Design Studio
-   Attended Robot
-   Unattended Robot
-   Unattended Robot Login Agent

For more information, see [Download the RPA applications from RPA Hub](https://servicenow-staging.fluidtopics.net/access?context=download-installer-rpa&family=yokohama&ft:locale=en-US).

 The following upgrade information is applicable only when you’re upgrading from San Diego or Tokyo to Yokohama.

 Based on the number of records in the application file table, you may experience a delay while upgrading the RPA Hub applications from Tokyo or earlier releases to Yokohama.

 Before upgrading RPA Hub to Yokohama, you must set the value of the **glide.rollback.blacklist.TableParentChange.change** system property to **false**. If this property doesn't exist in the System Property \[sys\_properties\] table, add the property and set its value to false. For more information on how to add a property, see [Add a system property](https://servicenow-staging.fluidtopics.net/access?context=t_AddAPropertyUsingSysPropsList&family=yokohama&ft:locale=en-US).

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

For more information, see [Download the RPA applications from RPA Hub](https://servicenow-staging.fluidtopics.net/access?context=download-installer-rpa&family=zurich&ft:locale=en-US).

 The following upgrade information is applicable only when you’re upgrading from San Diego or Tokyo to Zurich.

 Based on the number of records in the application file table, you may experience a delay while upgrading the RPA Hub applications from Tokyo or earlier releases to Zurich.

 Before upgrading RPA Hub to Zurich, you must set the value of the **glide.rollback.blacklist.TableParentChange.change** system property to **false**. If this property doesn't exist in the System Property \[sys\_properties\] table, add the property and set its value to false. For more information on how to add a property, see [Add a system property](https://servicenow-staging.fluidtopics.net/access?context=t_AddAPropertyUsingSysPropsList&family=zurich&ft:locale=en-US).

 After you upgrade to Zurich, the bot process definitions change to the new structure, which is the bot process configuration.

 Although the bot process configuration doesn't replace the bot process completely, most fields are moved from the bot process to the bot process configuration. If you upgrade to Zurich without updating the system property value, the tables don’t extend the Application File \[sys\_metadata\] table. To update the table changes manually, see the [Restructuring RPA Hub tables to sys\_metadata in Utah and beyond release \[KB1223629\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1223629) article in the Now Support Knowledge Base.

</td></tr></tbody>
</table>## New features

Between your current release family and Zurich, new features were introduced for RPA Hub.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   **[Credential Management in RPA Hub](https://servicenow-staging.fluidtopics.net/access?context=credential-management-rpa-hub&family=xanadu&ft:locale=en-US)**

Create application credentials, robot credentials, and Time-based One-time Password \(TOTP\) authentications and reuse them in multiple bot processes through a credential group.

-   **[Migration of a bot process configuration in RPA Hub](https://servicenow-staging.fluidtopics.net/access?context=bot-process-migration&family=xanadu&ft:locale=en-US)**

Migrate the bot process configuration and associated assets from one environment to another environment.

For example, when the bot process is ready to be migrated from a developer’s environment to a UAT environment, an RPA developer or RPA administrator can select the **Ready for Migration** button on a published bot process. This action enables the **Migrate** button to appear. This button is only visible when the bot process migration isn’t in progress. Then, the RPA release manager or RPA administrator can initiate the migration process by selecting the **Migrate** button. After the bot process and associated assets are migrated, a release manager can make any necessary changes, create and associate credentials, create an associated bot process record, and publish the bot process on the UAT \(target\) environment.

-   **[Enhanced element interrogations using the recorder feature](https://servicenow-staging.fluidtopics.net/access?context=recording-automations&family=xanadu&ft:locale=en-US)**

In the RPA Desktop Design Studio application, while using the recorder feature, you can move and position your recorded actions and screens in the Recorded actions pane. You can also edit a recorded action and element name.

-   **[New sample automations](https://servicenow-staging.fluidtopics.net/access?context=rpa-studio-ui&family=xanadu&ft:locale=en-US)**

Use the unattended and attended sample automations that were added to the Sample Automations page of RPA Desktop Design Studio. You can also view them in the Samples Explorer section.

    -   Merge CSV files
    -   Convert Excel to JSON
    -   Fetch contact info from email
    -   Resume Skill Matcher
    -   Copying a Range from One Excel File to Another
    -   Email Archiving or Deletion
    -   Streamlining Report Data Analysis
    -   Extract Excel Table to Embed in Email Body
    -   Zip and Unzip files
    -   XML to Excel Conversion
    -   Extract Data from Table and Saving to Excel
    -   Merge Excel Sheets
    -   Download attachments from Outlook
A sample automation is a prebuilt automation that shows how an automation works in the RPA Desktop Design Studio. The RPA Desktop Design Studio provides multiple sample automations that cater to different use cases.

-   **[Skill enhancements](https://servicenow-staging.fluidtopics.net/access?context=override-skill-version-rpahub&family=xanadu&ft:locale=en-US)**

View a skill package version for an associated package in a bot process or attended and unattended packages in RPA Hub. As an RPA release manager, you can override a skill version to use a specific skill package version for your bot process.

For example, to use a latest version of the skill package, you can override the skill package version in RPA Hub without publishing the attended or unattended package again. You can either override a skill version for a bot process or select the bot processes to override in the skill package version.

You can use the different versions of the same skill for different bot processes depending on your specific requirements. When the bot process executes, it uses the selected version instead of the version that was defined in the automation.

The following tabs were added:

    -   Use the **Skill Overrides** tab on the bot process form to view the skill version that was used. You can also use this tab to override the skill version for a specific bot process.
    -   Use the **Skills** tab on the package version of either the type attended or unattended to see the skills that were used in the package version.
    -   Use the **Bot process** tab on the skill package version to override the skill version for one or more bot processes.
In the RPA Desktop Design Studio, the Assign Bot Process feature is enabled for Skills automation projects. It shows both attended and unattended bot processes in the **Bot process** field. For the unattended processes, the associated robots are listed in a drop-down menu. For more information, see [Assign bot process to an automation project](https://servicenow-staging.fluidtopics.net/access?context=assign-bot-process&family=xanadu&ft:locale=en-US).

If any skills are overridden in the bot process, use the Assign Bot Process feature in the RPA Desktop Design Studio to use the revised skill version during the current execution.

If a skill is overridden while the robot is in execution, the robot doesn't use the overridden skill for the current execution. Instead, the robot considers the updated skill version starting from the next execution.

-   **[Sensitive request content in queues](https://servicenow-staging.fluidtopics.net/access?context=work-queue-form&family=xanadu&ft:locale=en-US)**

Pass both sensitive data and non-sensitive data separately in work items.

In the Work item form, the **Sensitive Request Content** field was added to store the sensitive content. For more information, see [Work item form](https://servicenow-staging.fluidtopics.net/access?context=work-queue-form&family=xanadu&ft:locale=en-US).

In the RPA Desktop Design Studio, RPA developers can handle the sensitive data in the Queue connector methods:

    -   For the **CreateJSONWorkItem**, **PickWorkItem**, and **UpdateWorkItem** methods, RPA developers can identify and mark specific JSON fields as sensitive.
    -   For the **CreateStringWorkItem** method, RPA developers have an option to include both sensitive and non-sensitive request content. A new parameter **Sensitive Request Content** was added to capture those details. The data that is passed in the sensitive request content is stored as encrypted data and the data that is passed in the request content field is stored as plain data.
For more information about these methods, see [Queue connector methods](https://servicenow-staging.fluidtopics.net/access?context=connectors-queues-methods&family=xanadu&ft:locale=en-US).

-   **[New CreateFile component in the Zip category](https://servicenow-staging.fluidtopics.net/access?context=use-zip-createfile&family=xanadu&ft:locale=en-US)**

Zip an existing folder or create a zip file by using the CreateFile component in RPA Desktop Design Studio.

-   **[Robot user mapping in RPA Hub](https://servicenow-staging.fluidtopics.net/access?context=create-unattended-robot&family=xanadu&ft:locale=en-US)**

Map an authorized user to an unattended robot to make the robot credentials accessible only to the mapped user.

In the Unattended robot form, the **User** field was added.

For upgrading customers, the **User** fields are automatically mapped with the user names who have recently created the process jobs for the selected unattended robots. If no process jobs are found for a selected robot, the RPA release managers must manually map the appropriate users to the robots.

-   **[Guided Tours in RPA Hub](https://servicenow-staging.fluidtopics.net/access?context=use-guided-tour-rpa-hub&family=xanadu&ft:locale=en-US)**

The following guided tours are available in the classic environment:

    -   Queues: Get step-by-step quick instructions in your instance on how to create queues.
    -   Bot process: Get step-by-step quick instructions in your instance on how to do an end-to-end configuration of the bot process and its related lists. You can select the tour to create an unattended bot process, attended bot process, or Embedded Task Automation.
-   **[What's New tab in the Help Center for RPA Hub](https://servicenow-staging.fluidtopics.net/access?context=whats-new&family=xanadu&ft:locale=en-US)**

Learn about the newly released features of RPA Hub in your instance.

If new content is available for you, the blue indicator on the **Help Center** button notifies that the feature content is new and unread by you on your instance.


</td></tr><tr><td>

Yokohama

</td><td>

-   **[New third-party AI model provider options available for all Now Assist applications](https://servicenow-staging.fluidtopics.net/access?context=exploring-large-language-models&family=yokohama&ft:locale=en-US)**

Google Gemini and AWS Claude are available for RPA bot generation skill in addition to Now LLM Service and Azure OpenAI.

-   **[Enhanced ACLs for security measures](https://servicenow-staging.fluidtopics.net/access?context=installed-with-rpa-hub&family=yokohama&ft:locale=en-US)**

Enhanced access controls for RPA bot generation skill for Now Assist for RPA Hub in compliance with AI security directives.

Access to RPA bot generation skill is now restricted to users with the RPA developer or RPA admin role. These roles contain the RPA Hub Admin user role \(sn\_nowassist\_admin.user\).

-   **[RPA bot generation](https://servicenow-staging.fluidtopics.net/access?context=rpa-now-assist-studio&family=yokohama&ft:locale=en-US)**

Use the Robotic Process Automation \(RPA\) bot generation skill in RPA Desktop Design Studio to create and edit automations and activities through short text instructions and preview options, accelerating automation development for both new and existing users. For more information about creating automations using Now Assist, see [Create an automation with Now Assist](https://servicenow-staging.fluidtopics.net/access?context=create-automation-now-assist&family=yokohama&ft:locale=en-US). For more information about creating activities using Now Assist, see [Create an activity with Now Assist](https://servicenow-staging.fluidtopics.net/access?context=create-activity-now-assist&family=yokohama&ft:locale=en-US).

Enhance automation logic using the **Build automation** option, starting from components or from a blank canvas based on text instructions. For more information, see [Build an automation with Now Assist](https://servicenow-staging.fluidtopics.net/access?context=build-automation-now-assist&family=yokohama&ft:locale=en-US).

-   **[High density robots](https://servicenow-staging.fluidtopics.net/access?context=high-density-robots-rpa-hub&family=yokohama&ft:locale=en-US)**

Enable multiple unattended robots to run simultaneously on the same Windows Server machine using the high-density robots feature. These unattended robots run automations in separate Remote Desktop Protocol \(RDP\) sessions. For more information, see [High density robots in Unattended Robot](https://servicenow-staging.fluidtopics.net/access?context=high-density-robots-uat&family=yokohama&ft:locale=en-US) and [Set up Windows Server machine for high density robots](https://servicenow-staging.fluidtopics.net/access?context=setup-windows-server-hdr&family=yokohama&ft:locale=en-US).

-   **[Sample automations](https://servicenow-staging.fluidtopics.net/access?context=sample-automations-rpa-studio&family=yokohama&ft:locale=en-US)**

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
-   **[Secure Shell \(SSH\) connector](https://servicenow-staging.fluidtopics.net/access?context=ssh-connector&family=yokohama&ft:locale=en-US)**

Establish an Secure Shell \(SSH\) connection to a remote server and execute commands in the RPA Desktop Design Studio. In the UNIX environment, SSH is the preferred way to access remote systems. Robots often interact with remote systems such as UNIX servers.

The connector comprises three methods:

    -   Connect: Establishes an SSH connection.
    -   Run Command: Executes commands over an established connection.
    -   Disconnect: Disconnects the session that was established using connect method.
Ensure to install the SSH plugin from the Plugins Manager as a prerequisite.

-   **[Bypassing the legal notice](https://servicenow-staging.fluidtopics.net/access?context=rpahub-sys-properties&family=yokohama&ft:locale=en-US)**

In RPA Hub, enable the **sn\_rpa\_fdn.bypass\_legal\_notice** system property to authorize the unattended robot to clear the legal notice message set by the system-level policy. This property ensures that a legal notice isn't displayed during the robot's login process.

-   **[What's New tab in the Help Center for RPA Hub](https://servicenow-staging.fluidtopics.net/access?context=whats-new&family=yokohama&ft:locale=en-US)**

Learn about the following newly released RPA features in your instance in the What's New tab in the Help Center for RPA Hub:

    -   Now Assist for RPA Hub
    -   High density robot
-   **[SAP connector](https://servicenow-staging.fluidtopics.net/access?context=sap-connector&family=yokohama&ft:locale=en-US)**

The SAP connector helps identify the screens and elements and automating workflows on the SAP GUI. For example, create and save a vendor entry. The SAP Connector is built by Bristlecone, Inc.

-   **[New methods for Universal app connector](https://servicenow-staging.fluidtopics.net/access?context=universal-app-connector&family=yokohama&ft:locale=en-US)**

In the RPA Desktop Design Studio, the following three new methods for Universal app connector are added.

    -   GetValue: Retrieves a value from an element.
    -   SetValue: Assigns a specified value into an element.
    -   Click: Performs a click action on an element.

</td></tr><tr><td>

Zurich

</td><td>


 -   **[Role changed for creating, updating, and deleting the Robot License Distribution records](https://servicenow-staging.fluidtopics.net/access?context=create-lua-record&family=zurich&ft:locale=en-US)**

Role for Create, Update, and Delete ACLs in the Robot License Distribution table is changed from admin to sn\_rpa\_fdn.rpa\_admin.

-   **[Long term stable models](https://servicenow-staging.fluidtopics.net/access?context=long-term-stable-models&family=zurich&ft:locale=en-US)**

Long term stable \(LTS\) models are part of Now LLM Service and provide longer model stability windows for regulated industries. These models can integrate with tools to provide governance, monitoring, and compliance controls.


-   **[New third-party AI model provider options available for all Now Assist applications](https://servicenow-staging.fluidtopics.net/access?context=exploring-large-language-models&family=zurich&ft:locale=en-US)**

Google Gemini and AWS Claude are available for RPA bot generation skill in addition to Now LLM Service and Azure OpenAI.

-   **[Python connector](https://servicenow-staging.fluidtopics.net/access?context=python-connector-rpa&family=zurich&ft:locale=en-US)**

Execute custom Python scripts or files as part of an automation workflow in the RPA Desktop Design Studio.

The connector comprises two methods:

    -   Execute: Runs Python scripts set up in the configuration window.
    -   InvokeScript: Runs Python script on local computers and gets the output.
Ensure to install the Scripting plugin from the Plugins Manager as a prerequisite. Along with Python, VB.NET, C\#, and Javascript connectors are available with this plugin.

-   **[Smart Card authentication](https://servicenow-staging.fluidtopics.net/access?context=smart-card-il&family=zurich&ft:locale=en-US)**

Use a physical smart card instead of a username and password for logging into a Windows machine.

You can run unattended automations on the machines that use smart cards for authentication. While configuring a robot credential, you can store the smart card username and password to allow the unattended robot to log in to machines that use smart card.

-   **[Enhanced ACLs for security measures](https://servicenow-staging.fluidtopics.net/access?context=installed-with-rpa-hub&family=zurich&ft:locale=en-US)**

Enhanced access controls for RPA bot generation skill for Now Assist for RPA Hub in compliance with AI security directives.

Access to RPA bot generation skill is now restricted to users with the RPA developer or RPA admin role. These roles contain the RPA Hub Admin user role \(sn\_nowassist\_admin.user\).


</td></tr></tbody>
</table>## Changes

Between your current release family and Zurich, some changes were made to existing RPA Hub features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   **[Process job with no logs](https://servicenow-staging.fluidtopics.net/access?context=rpa-studio-ui&family=xanadu&ft:locale=en-US)**

In the RPA Desktop Design Studio, the following process job records aren’t displayed in the Attach log window:

    -   Process job records with no logs.
    -   Process job records that are stored in the robot machine.
-   **[Credential sets are replaced by credential groups](https://servicenow-staging.fluidtopics.net/access?context=credential-management-rpa-hub&family=xanadu&ft:locale=en-US)**

In RPA Hub, the credential sets that were created for a bot process are now replaced with credential groups. You can now define the robot credentials, Time-based One-time Password \(TOTP\) authentication, and application credentials outside of the bot process and reuse them in multiple bot processes. By using credential groups, you don't have to create the same credentials for each bot process.

For upgrading customers, the existing credential sets and associated credentials are migrated seamlessly.

-   **[Changes in the Start Process UI action](https://servicenow-staging.fluidtopics.net/access?context=start-bot-process&family=xanadu&ft:locale=en-US)**

In RPA Hub, when you select the **Start Process** button, you can't view the robots that are in the **In Maintenance** life-cycle stage status.

When a bot process is either in the **In Maintenance** or **Build** life-cycle stage status and is using a robot pool, new robots aren’t deployed for dynamic allocation.

Dynamic allocation in the robot pool is only activated for published bot processes.

-   **[Changes in the Start Process action](https://servicenow-staging.fluidtopics.net/access?context=rpa-hub-actions&family=xanadu&ft:locale=en-US)**

When invoking the **Start Process** Workflow Studio action, the robots that are in the **In Maintenance** life-cycle stage status are treated as failed robots.

-   **[Changes in the Start Process subflow](https://servicenow-staging.fluidtopics.net/access?context=rpa-hub-actions&family=xanadu&ft:locale=en-US)**

If a process job isn’t in the **Running** status, the robot that is associated with the process job is treated as **Failed** in the **Start Process** subflow output.

-   **[Break component issue with loops](https://servicenow-staging.fluidtopics.net/access?context=use-loop-break&family=xanadu&ft:locale=en-US)**

An issue with the break components in the nested activities that failed to break their loops is now fixed. For more information, see [List of components compatible with latest version](https://servicenow-staging.fluidtopics.net/access?context=list-components-upgrade&family=xanadu&ft:locale=en-US).

-   **Microsoft Software Installer \(MSI\) compatibility**

Older MSIs that are related to Unattended Robot, Attended Robot, and RPA Desktop Design Studio from the RPA Hub store release versions 7.0.3 and 9.0.0 are compatible and can be used with the current store release version \(10.0.X\) of RPA Hub.

However, there are some limitations:

    -   Any new automation components available in the latest version aren’t available in the older versions. For example, the CreateFile component in the Zip category in version 10.0 doesn’t work in older versions.
    -   Components of the same name with different parameters aren’t backward compatible.
If robot machines are using older MSIs than the current version of the instance, any new features that are added in the later versions aren’t available for older MSIs. For example, the features released after version 7.0.3 don’t work in version 7.0.3 MSIs. Only those features that exist in version 7.0.3 work in that version.


</td></tr><tr><td>

Yokohama

</td><td>

-   **[Changed fields for the Unattended Robot application](https://servicenow-staging.fluidtopics.net/access?context=set-up-rpa-runtime&family=yokohama&ft:locale=en-US)**

In the Unattended Robot dialog box, the **RPA Hub** field name has been changed to **Instance URL**.

-   **[Embedded Task Automation in RPA Hub](https://servicenow-staging.fluidtopics.net/access?context=embedded-task-auto-rpa&family=yokohama&ft:locale=en-US)**

Trigger attended bot processes \(attended automations\) from the ServiceNow forms in the Workspace experience apart from initiating them from a classic UI or the Attended Robot application.

-   **[Microsoft Software Installer \(MSI\) compatibility](https://servicenow-staging.fluidtopics.net/access?context=download-installer-rpa&family=yokohama&ft:locale=en-US)**

Older MSIs that are related to Attended Robot and RPA Desktop Design Studio from the RPA Hub store release versions 7.0.3 and 9.0.0 are compatible and can be used with the current store release version \(12.0.X\) of RPA Hub. For Unattended Robot, the latest MSI must be installed, as it is not backward compatible.

However, there are some limitations:

    -   Any new automation components available in the latest version aren’t available in the older versions. For example, the SSH connector in version 12.0 doesn’t work in older versions.
    -   Components of the same name with different parameters aren’t backward compatible.
If robot machines use older MSIs than the current instance version, they won't have the new features from later versions. For example, features released after version 10.0 won't work in version 10.0 MSIs. Only features from version 10.0 are available in that version.

-   **[TerminateByName component behavior change](https://servicenow-staging.fluidtopics.net/access?context=use-sysprocess-terminatename&family=yokohama&ft:locale=en-US)**

The TerminateByName component stops processes or applications only within the current user session.


</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Removed

Between your current release family and Zurich, some RPA Hub features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

The credential set related list was removed from the bot process form in RPA Hub.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Zurich, some RPA Hub features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   The RPA Sample templates store application is deprecated and is no longer supported or available for new activation. RPA Desktop Design Studio provides the latest experience for this functionality. For more information, see [RPA Desktop Design Studio user interface](https://servicenow-staging.fluidtopics.net/access?context=rpa-studio-ui&family=xanadu&ft:locale=en-US).
-   In RPA Hub, the **Is Request Content Sensitive** field in the Queues form was deprecated.
-   In RPA Hub the **Credential Set** field in the Process Robot Credentials form was deprecated.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

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

Xanadu

</td><td>

Install RPA Hub by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://servicenow-staging.fluidtopics.net/access?context=sn-store-release-notes&family=xanadu&ft:locale=en-US).

 For cumulative release notes information on RPA Hub, see [RPA Hub release notes](https://servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/platform-app-engine/store-rn-plat-app-engine-rpa-hub.html).

 For cumulative release notes information on RPA Desktop Design Studio, see [RPA Plugin Bundle release notes](https://servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/platform-app-engine/store-rn-plat-app-rpa-plugin-bundle.html).

 If you have previously downloaded the application from the ServiceNow Store and a new version is available, you can update it in your ServiceNow AI Platform instance at **All** &gt; **System Applications** &gt; **All Available Applications**.

</td></tr><tr><td>

Yokohama

</td><td>

Install RPA Hub by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://servicenow-staging.fluidtopics.net/access?context=sn-store-release-notes&family=yokohama&ft:locale=en-US).

 Install the Now Assist for RPA Hub application to add the generative AI capability and turn on the Robotic Process Automation \(RPA\) bot generation skill to use generative AI to create automations. For more information about these tasks, see [Configure Now Assist for RPA Hub](https://servicenow-staging.fluidtopics.net/access?context=configure-now-assist-rpa-hub&family=yokohama&ft:locale=en-US) and [Turn on the RPA bot generation skill](https://servicenow-staging.fluidtopics.net/access?context=turn-rpa-bot-generation-skill&family=yokohama&ft:locale=en-US).

 For cumulative release notes information on RPA Hub, see [RPA Hub release notes](https://servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/platform-app-engine/store-rn-plat-app-engine-rpa-hub.html).

 For cumulative release notes information on RPA Desktop Design Studio, see [RPA Plugin Bundle release notes](https://servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/platform-app-engine/store-rn-plat-app-rpa-plugin-bundle.html).

 For cumulative release notes information on Now Assist for RPA Hub, see [Now Assist for RPA Hub release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/platform-app-engine/store-rn-plat-app-engine-now-assist-rpa-hub.html).

 If you have previously downloaded the application from the ServiceNow Store and a new version is available, you can update it in your ServiceNow AI Platform instance at **All** &gt; **System Applications** &gt; **All Available Applications**.

</td></tr><tr><td>

Zurich

</td><td>

Install RPA Hub by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://servicenow-staging.fluidtopics.net/access?context=sn-store-release-notes&family=zurich&ft:locale=en-US).

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for RPA Hub we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

To use the Unattended Robot application, the minimum requirements are:

-   Intel Processor \(1vCPU\).
-   4-GB RAM.
-   Minimum 20-GB free disk space after installing the OS, patches, and base software.
-   Microsoft Windows 10, Windows Server 2016, or Windows Server 2019.
-   At least .NET Framework 4.7.1.
-   DPI scaling setting must be deactivated.

 To use the Unattended Robot application, the requirements are:

-   Intel Processor \(4vCPU\).
-   8-GB RAM.
-   Minimum 50-GB free disk space after installing the OS, patches, and base software.
-   Microsoft Windows 10, Windows Server 2016, or Windows Server 2019.
-   At least .NET Framework 4.7.1.
-   DPI scaling setting must be deactivated.

 An unattended robot is mapped to only one machine.

 Virtual Machines \(VMs\) that are used for the Unattended Robot application must be persistent and constantly on.

 To use the Attended Robot application, the minimum requirements are:

-   Intel Processor \(1vCPU\).
-   4-GB RAM.
-   Minimum 20-GB free disk space after installing the OS, patches, and base software.
-   Microsoft Windows 10, Windows Server 2016, or Windows Server 2019.
-   At least .NET Framework 4.7.1.
-   DPI scaling setting must be deactivated.

 To use the Attended Robot application, the requirements are:

-   Intel Processor \(4vCPU\).
-   8-GB RAM.
-   Minimum 50-GB free disk space after installing the OS, patches, and base software.
-   Microsoft Windows 10, Windows Server 2016, or Windows Server 2019.
-   At least .NET Framework 4.7.1.
-   DPI scaling setting must be deactivated.

 An attended robot is mapped to only one user.

 To use the RPA Desktop Design Studio application, the minimum requirements are:

-   Intel Processor \(At least, Core i5\).
-   4-GB RAM.
-   20-GB free disk space.
-   Microsoft Windows 10, Windows Server 2016, or Windows Server 2019.
-   At least .NET Framework 4.7.1.
-   Monitor with 1920x1080p resolution.
-   DPI scaling setting must be deactivated.

 To use the RPA Desktop Design Studio application, the requirements are:

-   Intel Processor \(Core i7\).
-   8-GB RAM.
-   50-GB free disk space.
-   Microsoft Windows 10, Windows Server 2016, or Windows Server 2019.
-   At least .NET Framework 4.7.1.
-   Monitor with 1920x1080p resolution.
-   DPI scaling setting must be deactivated.

</td></tr><tr><td>

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

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for RPA Hub we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

ServiceNow workspaces don’t support mobile devices. For more information about the list of supported browsers, see [Browser support](https://servicenow-staging.fluidtopics.net/access?context=browser-support&family=xanadu&ft:locale=en-US).

</td></tr><tr><td>

Yokohama

</td><td>

ServiceNow workspaces don’t support mobile devices. For more information about the list of supported browsers, see [Browser support](https://servicenow-staging.fluidtopics.net/access?context=browser-support&family=yokohama&ft:locale=en-US).

</td></tr><tr><td>

Zurich

</td><td>

ServiceNow workspaces don’t support mobile devices. For more information about the list of supported browsers, see [Browser support](https://servicenow-staging.fluidtopics.net/access?context=browser-support&family=zurich&ft:locale=en-US).

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for RPA Hub, such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

-   **Accessibility improvements**

Accessibility improvements were completed to support WCAG 2.1 Level AA conformance.


</td></tr><tr><td>

Zurich

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

Xanadu

</td><td>

RPA Hub supports international languages. For more information, see [Internationalization support for RPA Hub](https://servicenow-staging.fluidtopics.net/access?context=rpa-hub-international-language-support&family=xanadu&ft:locale=en-US).

</td></tr><tr><td>

Yokohama

</td><td>

RPA Hub supports international languages. For more information, see [Internationalization support for RPA Hub](https://servicenow-staging.fluidtopics.net/access?context=rpa-hub-international-language-support&family=yokohama&ft:locale=en-US).

</td></tr><tr><td>

Zurich

</td><td>

RPA Hub supports international languages. For more information, see [Internationalization support for RPA Hub](https://servicenow-staging.fluidtopics.net/access?context=rpa-hub-international-language-support&family=zurich&ft:locale=en-US).

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for RPA Hub we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   Create the centralized credentials that you can reuse in multiple bot processes.
-   Migrate the bot process configuration and associated assets from one environment to another environment with a click of a button.
-   Rearrange the recorded actions and screens according to your preference and generate the automation flow.
-   Use the 15 new sample automations that were added in RPA Desktop Design Studio that cater to different use cases.
-   View and manage the skill versions used in packages from a central location in RPA Hub. You can override an existing skill version that was used for each bot process.
-   Manage sensitive and non-sensitive data in two separate fields of a work item.
-   Use Guided Tours to get quick instructions on how to create queues and configure bot processes.

 See [Robotic Process Automation \(RPA\) Hub](https://servicenow-staging.fluidtopics.net/access?context=rpa-main-landing-page&family=xanadu&ft:locale=en-US) for more information.

</td></tr><tr><td>

Yokohama

</td><td>

-   Use generative AI to create and edit automations, activities, and extend automation logic flow through text instructions and preview options in the RPA Desktop Design Studio.
-   Run multiple unattended robots on different user sessions at the same time on the same Windows Server machine using the high-density robots feature.
-   Use new sample automations that were added in the RPA Desktop Design Studio that cater to different use cases.
-   Leverage the communication capabilities of the SSH protocol in the automation processes with the new Secure Shell \(SSH\) connector in the RPA Desktop Design Studio.
-   Use the SAP connector to identify the screens and elements and to automate workflows on SAP graphical user interfaces \(GUI\).
-   Use Google Gemini and Anthropic Claude on AWS as AI model providers for RPA bot generation skill in addition to Now LLM Service and Azure OpenAI.
-   Enhanced access controls for RPA bot generation skill.

 See [Robotic Process Automation \(RPA\) Hub](https://servicenow-staging.fluidtopics.net/access?context=rpa-main-landing-page&family=yokohama&ft:locale=en-US) for more information.

</td></tr><tr><td>

Zurich

</td><td>

[Zurich Patch 4](https://servicenow-staging.fluidtopics.net/access?context=zurich-patch-4&family=zurich&ft:locale=en-US)

-   Promote stability with the Long-Term Support \(LTS\) model for generative AI.
-   Only the sn\_rpa\_fdn.rpa\_admin role can create, update, and delete records in the Robot License Distribution table.

 [Zurich Patch 1](https://servicenow-staging.fluidtopics.net/access?context=zurich-patch-1&family=zurich&ft:locale=en-US)

-   Use Google Gemini and Anthropic Claude on AWS as AI model providers for RPA bot generation skill in addition to Now LLM Service and Azure OpenAI.
-   Use the Python connector to execute custom Python scripts or files as part of an automation workflow.
-   Use a Smart Card authentication for enhanced security.
-   Enhanced access controls for RPA bot generation skill.

 See [Robotic Process Automation \(RPA\) Hub](https://servicenow-staging.fluidtopics.net/access?context=rpa-main-landing-page&family=zurich&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/delta-xanadu-zurich/rn-combined-intro.md)

