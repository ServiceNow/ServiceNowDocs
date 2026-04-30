---
title: RPA Hub release notes
description: The ServiceNow RPA Hub application enables end-to-end automation for your organization. RPA Hub was enhanced and updated in the Xanadu release.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 13
---

# RPA Hub release notes

The ServiceNow® RPA Hub application enables end-to-end automation for your organization. RPA Hub was enhanced and updated in the Xanadu release.

## RPA Hub highlights for the Xanadu release

-   Create the centralized credentials that you can reuse in multiple bot processes.
-   Migrate the bot process configuration and associated assets from one environment to another environment with a click of a button.
-   Rearrange the recorded actions and screens according to your preference and generate the automation flow.
-   Use the 15 new sample automations that were added in RPA Desktop Design Studio that cater to different use cases.
-   View and manage the skill versions used in packages from a central location in RPA Hub. You can override an existing skill version that was used for each bot process.
-   Manage sensitive and non-sensitive data in two separate fields of a work item.
-   Use Guided Tours to get quick instructions on how to create queues and configure bot processes.

See [Robotic Process Automation \(RPA\) Hub](https://www.servicenow.com/docs/access?context=rpa-main-landing-page&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US) for more information.

**Important:** RPA Hub is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Important information for upgrading RPA Hub to Xanadu

Upgrade any of these currently installed Microsoft Software Installers \(MSIs\) by downloading the RPA applications:

-   RPA Desktop Design Studio
-   Attended Robot
-   Unattended Robot
-   Unattended Robot Login Agent

For more information, see [Download the RPA applications from RPA Hub](https://www.servicenow.com/docs/access?context=download-installer-rpa&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US).

The following upgrade information is applicable only when you’re upgrading from San Diego or Tokyo to Xanadu.

Based on the number of records in the application file table, you could experience a potential delay while upgrading the RPA Hub applications from Tokyo or earlier releases to Xanadu.

Before upgrading RPA Hub to Xanadu, you must set the value of the **glide.rollback.blacklist.TableParentChange.change** system property to **false**. If this property doesn't exist in the System Property \[sys\_properties\] table, add the property and set its value to false. For more information on how to add a property, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=xanadu&pubname=xanadu-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

After you upgrade to Xanadu, the bot process definitions change to the new structure, which is the bot process configuration.

Although the bot process configuration doesn't replace the bot process completely, most fields are moved from the bot process to the bot process configuration. If you upgrade to Xanadu without updating the system property value, the tables don’t extend the Application File table. To update the table changes manually, see the [Restructuring RPA Hub tables to sys\_metadata in Utah and beyond release](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1223629) article in the Now Support knowledge base.

## New in the Xanadu release

-   **[Credential Management in RPA Hub](https://www.servicenow.com/docs/access?context=credential-management-rpa-hub&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US)**

    Create application credentials, robot credentials, and Time-based One-time Password \(TOTP\) authentications and reuse them in multiple bot processes through a credential group.

-   **[Migration of a bot process configuration in RPA Hub](https://www.servicenow.com/docs/access?context=bot-process-migration&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US)**

    Migrate the bot process configuration and associated assets from one environment to another environment.

    For example, when the bot process is ready to be migrated from a developer’s environment to a UAT environment, an RPA developer or RPA administrator can select the **Ready for Migration** button on a published bot process. This action enables the **Migrate** button to appear. This button is only visible when the bot process migration isn’t in progress. Then, the RPA release manager or RPA administrator can initiate the migration process by selecting the **Migrate** button. After the bot process and associated assets are migrated, a release manager can make any necessary changes, create and associate credentials, create an associated bot process record, and publish the bot process on the UAT \(target\) environment.

-   **[Enhanced element interrogations using the recorder feature](https://www.servicenow.com/docs/access?context=recording-automations&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US)**

    In the RPA Desktop Design Studio application, while using the recorder feature, you can move and position your recorded actions and screens in the Recorded actions pane. You can also edit a recorded action and element name.

-   **[New sample automations](https://www.servicenow.com/docs/access?context=rpa-studio-ui&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US)**

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

-   **[Skill enhancements](https://www.servicenow.com/docs/access?context=override-skill-version-rpahub&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US)**

    View a skill package version for an associated package in a bot process or attended and unattended packages in RPA Hub. As an RPA release manager, you can override a skill version to use a specific skill package version for your bot process.

    For example, to use a latest version of the skill package, you can override the skill package version in RPA Hub without publishing the attended or unattended package again. You can either override a skill version for a bot process or select the bot processes to override in the skill package version.

    You can use the different versions of the same skill for different bot processes depending on your specific requirements. When the bot process executes, it uses the selected version instead of the version that was defined in the automation.

    The following tabs were added:

    -   Use the **Skill Overrides** tab on the bot process form to view the skill version that was used. You can also use this tab to override the skill version for a specific bot process.
    -   Use the **Skills** tab on the package version of either the type attended or unattended to see the skills that were used in the package version.
    -   Use the **Bot process** tab on the skill package version to override the skill version for one or more bot processes.
    In the RPA Desktop Design Studio, the Assign Bot Process feature is enabled for Skills automation projects. It shows both attended and unattended bot processes in the **Bot process** field. For the unattended processes, the associated robots are listed in a drop-down menu. For more information, see [Assign bot process to an automation project](https://www.servicenow.com/docs/access?context=assign-bot-process&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US).

    If any skills are overridden in the bot process, use the Assign Bot Process feature in the RPA Desktop Design Studio to use the revised skill version during the current execution.

    If a skill is overridden while the robot is in execution, the robot doesn't use the overridden skill for the current execution. Instead, the robot considers the updated skill version starting from the next execution.

-   **[Sensitive request content in queues](https://www.servicenow.com/docs/access?context=work-queue-form&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US)**

    Pass both sensitive data and non-sensitive data separately in work items.

    In the Work item form, the **Sensitive Request Content** field was added to store the sensitive content. For more information, see [Work item form in RPA Hub](https://www.servicenow.com/docs/access?context=work-queue-form&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US).

    In the RPA Desktop Design Studio, RPA developers can handle the sensitive data in the Queue connector methods:

    -   For the **CreateJSONWorkItem**, **PickWorkItem**, and **UpdateWorkItem** methods, RPA developers can identify and mark specific JSON fields as sensitive.
    -   For the **CreateStringWorkItem** method, RPA developers have an option to include both sensitive and non-sensitive request content. A new parameter **Sensitive Request Content** was added to capture those details. The data that is passed in the sensitive request content is stored as encrypted data and the data that is passed in the request content field is stored as plain data.
    For more information about these methods, see [Queue connector methods](https://www.servicenow.com/docs/access?context=connectors-queues-methods&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US).

-   **[New CreateFile component in the Zip category](https://www.servicenow.com/docs/access?context=use-zip-createfile&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US)**

    Zip an existing folder or create a zip file by using the CreateFile component in RPA Desktop Design Studio.

-   **[Robot user mapping in RPA Hub](https://www.servicenow.com/docs/access?context=create-unattended-robot&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US)**

    Map an authorized user to an unattended robot to make the robot credentials accessible only to the mapped user.

    In the Unattended robot form, the **User** field was added.

    For upgrading customers, the **User** fields are automatically mapped with the user names who have recently created the process jobs for the selected unattended robots. If no process jobs are found for a selected robot, the RPA release managers must manually map the appropriate users to the robots.

-   **[Guided Tours in RPA Hub](https://www.servicenow.com/docs/access?context=use-guided-tour-rpa-hub&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US)**

    The following guided tours are available in the classic environment:

    -   Queues: Get step-by-step quick instructions in your instance on how to create queues.
    -   Bot process: Get step-by-step quick instructions in your instance on how to do an end-to-end configuration of the bot process and its related lists. You can select the tour to create an unattended bot process, attended bot process, or Embedded Task Automation.
-   **[What's New tab in the Help Center for RPA Hub](https://www.servicenow.com/docs/access?context=whats-new&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US)**

    Learn about the newly released features of RPA Hub in your instance.

    If new content is available for you, the blue indicator on the **Help Center** button notifies that the feature content is new and unread by you on your instance.


## Changed in this release

-   **[Process job with no logs](https://www.servicenow.com/docs/access?context=rpa-studio-ui&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US)**

    In the RPA Desktop Design Studio, the following process job records aren’t displayed in the Attach log window:

    -   Process job records with no logs.
    -   Process job records that are stored in the robot machine.
-   **[Credential sets are replaced by credential groups](https://www.servicenow.com/docs/access?context=credential-management-rpa-hub&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US)**

    In RPA Hub, the credential sets that were created for a bot process are now replaced with credential groups. You can now define the robot credentials, Time-based One-time Password \(TOTP\) authentication, and application credentials outside of the bot process and reuse them in multiple bot processes. By using credential groups, you don't have to create the same credentials for each bot process.

    For upgrading customers, the existing credential sets and associated credentials are migrated seamlessly.

-   **[Changes in the Start Process UI action](https://www.servicenow.com/docs/access?context=start-bot-process&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US)**

    In RPA Hub, when you select the **Start Process** button, you can't view the robots that are in the **In Maintenance** life-cycle stage status.

    When a bot process is either in the **In Maintenance** or **Build** life-cycle stage status and is using a robot pool, new robots aren’t deployed for dynamic allocation.

    Dynamic allocation in the robot pool is only activated for published bot processes.

-   **[Changes in the Start Process action](https://www.servicenow.com/docs/access?context=rpa-hub-actions&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US)**

    When invoking the **Start Process** Workflow Studio action, the robots that are in the **In Maintenance** life-cycle stage status are treated as failed robots.

-   **[Changes in the Start Process subflow](https://www.servicenow.com/docs/access?context=rpa-hub-actions&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US)**

    If a process job isn’t in the **Running** status, the robot that is associated with the process job is treated as **Failed** in the **Start Process** subflow output.

-   **[Break component issue with loops](https://www.servicenow.com/docs/access?context=use-loop-break&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US)**

    An issue with the break components in the nested activities that failed to break their loops is now fixed. For more information, see [List of components compatible with latest version](https://www.servicenow.com/docs/access?context=list-components-upgrade&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US).

-   **Microsoft Software Installer \(MSI\) compatibility**

    Older MSIs that are related to Unattended Robot, Attended Robot, and RPA Desktop Design Studio from the RPA Hub store release versions 7.0.3 and 9.0.0 are compatible and can be used with the current store release version \(10.0.X\) of RPA Hub.

    However, there are some limitations:

    -   Any new automation components available in the latest version aren’t available in the older versions. For example, the CreateFile component in the Zip category in version 10.0 doesn’t work in older versions.
    -   Components of the same name with different parameters aren’t backward compatible.
    If robot machines are using older MSIs than the current version of the instance, any new features that are added in the later versions aren’t available for older MSIs. For example, the features released after version 7.0.3 don’t work in version 7.0.3 MSIs. Only those features that exist in version 7.0.3 work in that version.


## Removed in this release

The credential set related list was removed from the bot process form in RPA Hub.

## Deprecations

-   The RPA Sample templates store application is deprecated and is no longer supported or available for new activation. RPA Desktop Design Studio provides the latest experience for this functionality. For more information, see [RPA Desktop Design Studio user interface](https://www.servicenow.com/docs/access?context=rpa-studio-ui&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US).
-   In RPA Hub, the **Is Request Content Sensitive** field in the Queues form was deprecated.
-   In RPA Hub the **Credential Set** field in the Process Robot Credentials form was deprecated.

## Activation information

Install RPA Hub by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

For cumulative release notes information on RPA Hub, see [RPA Hub release notes](https://servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/platform-app-engine/store-rn-plat-app-engine-rpa-hub.html).

For cumulative release notes information on RPA Desktop Design Studio, see [RPA Plugin Bundle release notes](https://servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/platform-app-engine/store-rn-plat-app-rpa-plugin-bundle.html).

If you have previously downloaded the application from the ServiceNow Store and a new version is available, you can update it in your ServiceNow AI Platform instance at **All** &gt; **System Applications** &gt; **All Available Applications**.

## Additional requirements

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

## Browser requirements

ServiceNow workspaces don’t support mobile devices. For more information about the list of supported browsers, see [Browser support](../../administer/navigation-and-ui/reference/browser-support.md).

## Localization information

RPA Hub supports international languages. For more information, see [Internationalization support for RPA Hub](https://www.servicenow.com/docs/access?context=rpa-hub-international-language-support&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US).

## Related ServiceNow applications and features

-   **[Workflow Studio](https://www.servicenow.com/docs/access?context=workflow-studio&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US)**

    ServiceNow® Workflow Studio integrates with RPA Hub for a seamless robot execution. You can use the Workflow Studio design environment to author flows and actions, as well as view the results they produce.


**Parent Topic:**[Hyperautomation and Low-code release notes](build-automate-rn-landing.md)

