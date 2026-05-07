---
title: Legacy - Commit changes
description: Application developers can commit their changes on the instance to the linked Git repository. You can either select a few changes to commit, or commit all changes on the instance at once.
locale: en-US
release: australia
product: ServiceNow Studio Classic
classification: servicenow-studio-classic
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Legacy - Source Control integration, Legacy - ServiceNow Studio, Building pro-code applications, Developing your application, Building applications]
---

# Legacy - Commit changes

Application developers can commit their changes on the instance to the linked Git repository. You can either select a few changes to commit, or commit all changes on the instance at once.

## Before you begin

**Important:** Starting with the Xanadu release, the legacy version of ServiceNow Studio is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. For details on the deprecation process, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

Try building and editing apps in the current version of ServiceNow Studio instead. For more information, see [ServiceNow Studio](../../servicenow-studio/concept/servicenow-studio-landing.md).

-   Role required: admin
-   [Legacy - Link an application or application-customization to source control](t_LinkAnApplicationToSourceControl.md)

## Procedure

1.  Navigate to **All** &gt; **Source Control** &gt; **Commit Changes**.

    The system displays the **Select files to commit to source control** window. The file changes from all the updates sets display. By default, the file changes from the current update set display.

    ![Select files to commit](../image/selective-commit.png)

2.  Select the file changes you wish to commit.

3.  To include untracked changes, select the **Include changes not tracked via the Customer Update \[sys\_update\_xml\] table** check box.

    -   The default for this check box is set via the **glide.sourcecontrol.default\_commit\_mode** property.
        -   Property can be set to **include\_untracked** or **exclude\_untracked**.
        -   The **include\_untracked** mode commits the updates to the application that do not generate sys\_update\_xml records, as well as any user-selected updates.
        -   The **exclude\_untracked** mode commits only updates selected by the user in the **Select files to commit to source control** dialog.
    -   The base system setting for the property is **exclude\_untracked**.
    -   Prior to the ServiceNow Rome release, only the **include\_untracked** mode is used.
    To hide the check box and use the value of the **glide.sourcecontrol.default\_commit\_mode** property, create the **sn\_devstudio.vcs.allow\_commit\_mode\_selection** property and set it to false. Checking this check box may incur a performance penalty.

    **Note:**

    Commits always occur in **include\_untracked** mode in the following cases:

    -   Linking to Source Control for the first time. \(To learn more, see [Legacy - Link an application or application-customization to source control](t_LinkAnApplicationToSourceControl.md).\)
    -   Publishing an application that's linked to Source Control from ServiceNow Studio. \(To learn more, see [Legacy - Publish an application from ServiceNow Studio when linked to Source Control](publish-app-from-studio.md).\)
    -   Selective commit mode is disabled.
4.  Click **Continue**.

5.  In **Commit comment**, enter a comment for the changes.

6.  Click **Commit Files**.

    The following operations occur:

    -   The system identifies all local changes.
    -   The system commits all local changes to the remote repository.
    **Note:** For list of known files that don’t have customer update records and are untracked, see [Customer Updates table](https://www.servicenow.com/docs/access?context=r_CustomerUpdatesTable&version=australia&pubname=australia-platform-security&ft:locale=en-US).


**Parent Topic:**[Legacy - Source Control integration](../concept/c_SourceControlIntegration.md)

