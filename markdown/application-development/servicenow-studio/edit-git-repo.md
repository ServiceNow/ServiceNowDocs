---
title: Legacy - Edit a Git repository configuration
description: You can edit a Git repository to change the network protocol selection, credentials or other field entries.
locale: en-US
release: australia
product: ServiceNow Studio
classification: servicenow-studio
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Legacy - Source Control integration, Legacy - ServiceNow Studio, Building pro-code applications, Developing your application, Building applications]
---

# Legacy - Edit a Git repository configuration

You can edit a Git repository to change the network protocol selection, credentials or other field entries.

## Before you begin

**Important:** Starting with the Xanadu release, the legacy version of ServiceNow Studio is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. For details on the deprecation process, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

Try building and editing apps in the current version of ServiceNow Studio instead. For more information, see [ServiceNow Studio](../../servicenow-studio/concept/servicenow-studio-landing.md).

Role required: admin

## Procedure

1.  In Studio, select **Edit Repository Configuration**.

    ![Edit Repository Configuration menu item](../image/edit-git-repo.png)

2.  Choose **https** or **ssh** Network protocol and enter the URL address of your repository.

    ![Choose the http network protocol](../image/edit-repo-config.png) ![Choose the ssh network protocol](../image/edit-repo-ssh.png)

3.  Change your credential or MID Server name if you wish.

    **Note:** If you have no MID server name, you can select a new one from the drop-down list. If you choose a new MID server, [Legacy - Apply remote changes](t_ApplyRemoteChanges.md) in the Source Control menu before making any further Source Control operations to avoid errors.

    For the default email field, the committer email address is defined by the sys\_user record if available. But if a committer's sys\_user record email field is empty, the system generates an alternate email \(username@instancename.service-now.com\). You can also enter a default email address and change it later. To use that default email address in all cases, select the check box.

4.  Click **Save**.


**Parent Topic:**[Legacy - Source Control integration](../concept/c_SourceControlIntegration.md)

