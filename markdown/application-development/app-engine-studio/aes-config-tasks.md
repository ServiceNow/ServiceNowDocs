---
title: Perform AES configuration tasks
description: As you work through the App Engine Studio \(AES\) guided setup, you must perform different configuration tasks.
locale: en-US
release: australia
product: App Engine Studio
classification: app-engine-studio
topic_type: reference
last_updated: "2026-04-28"
reading_time_minutes: 4
breadcrumb: [Configure AES, Configure, App Engine Studio, Building low-code applications, Developing your application, Building applications]
---

# Perform AES configuration tasks

As you work through the App Engine Studio \(AES\) guided setup, you must perform different configuration tasks.

## Setting up environments, tools, and user access

The following table lists the tasks required for configuring App Engine Studio, including links to detailed instructions for completing the tasks.

<table id="table_lqq_1qt_rhb"><thead><tr><th>

Task

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Install App Engine Studio in your development instances.

</td><td>

You can install the App Engine Studio application \(com.snc.app-engine-studio\) if you have the admin role.

 The application installs related ServiceNow® Store applications and plugins if they are not already installed.

 For detailed instructions, see [Installing App Engine Studio](../task/install-aes.md).

</td></tr><tr><td>

Set up instance credentials.

</td><td>

For each instance that you're using, create a Connections and Credentials alias. Verify that the alias type is **Credential**, not **Connection and Credential**.

 For detailed instructions, see Set up instance credentials.

</td></tr><tr><td>

Activate Playbooks.

</td><td>

You can edit processes in App Engine Studio, but you must activate Playbooks for App Engine Studio and enable the **Process Automation Designer for App Engine \[com.glide.pad.license\]** plugin to get started. For more information, see Activate Playbooks.

</td></tr><tr id="integrationhub-spokes"><td>

Set up Integration Hub spokes.

</td><td>

Activate spokes to enhance your Workflow Studio and App Engine Studio experience with integration-specific content.

 The following spokes are available for use with App Engine Studio.

-   Gmail spoke
-   Google Sheets spoke
-   Jira Spoke
-   Microsoft 365 Excel spoke
-   Microsoft Teams spoke
-   Slack spoke
-   Twilio spoke
-   X Spoke \(formerly Twitter Spoke\)
-   Zoom spoke

</td></tr><tr><td>

Review access settings for Workflow Studio in your development instance.

</td><td>

Enable your developers to use the editing capabilities that best suit them. For detailed instructions, see Review Flow Designer access settings.

</td></tr><tr><td>

Review access settings for Catalog Builder.

</td><td>

Enable your developers to add items to the appropriate catalogs and categories.​For detailed instructions, see Review Catalog Builder access settings.

</td></tr><tr><td>

Set up an instance scan cadence.

</td><td>

Schedule regular scans of your instance so that you can identify possible issues that arise from application development in App Engine Studio.For detailed instructions, see Set up an instance scan cadence in Health Center.

</td></tr><tr><td>

In your production instance, add users to the App Engine Studio admin group.

</td><td>

Add members to the group so they can review app- and deployment-related requests. Also, define a contact email address for the group.

 For detailed instructions, see [Add users to the App Engine Admin group](../task/add-users-to-admin-grp.md).

</td></tr><tr><td>

In your development instance, add developers to the App Engine Studio users group.

</td><td>

Enable developers in your organization to build applications in App Engine Studio.

 For detailed instructions, see [Grant user access to AES](../task/grant-aes-access.md).

</td></tr><tr><td>

In your development instance, add users to the App Engine Studio User Limited group.

</td><td>

Enable developers in your organization to collaborate on applications that someone else created in App Engine Studio.

 For detailed instructions, see [Grant user access to AES](../task/grant-aes-access.md).

</td></tr><tr><td>

Set up collaboration descriptors.

</td><td>

Set up custom collaboration descriptors in the global scope for use in App Engine Studio.

 For detailed instructions, see [Set up custom collaboration descriptors](../task/set-up-custom-collaboration-descriptors.md).

</td></tr><tr><td>

In your non-production instance, specify an app template admin.

</td><td>

Grant the app\_template\_admin role to users who will manage template activation, deactivation, and sharing in App Engine Studio.

 For detailed instructions, see [Manage template access](../task/manage-template-access.md).

</td></tr></tbody>
</table><table id="table_pdv_qb1_15b"><thead><tr><th>

Learn more about AES configuration

</th><th>

Additional ServiceNow resources

</th></tr></thead><tbody><tr><td rowspan="3">

ServiceNow provides several additional resources on configuring and administering App Engine Studio.

</td><td>

![](../../../reuse/icons/brand-icons/bus-try-a-demo.svg) App Engine Studio release notes

</td></tr><tr><td>

![](../../../reuse/icons/brand-icons/bus-3-person.svg) [ServiceNow Community site](https://community.servicenow.com/community?id=community_search&q=app%20engine%20studio&spa=1)

</td></tr><tr><td>

![](../../../reuse/icons/brand-icons/bus-webinar.svg) [App Engine Studio video on adding security](https://www.youtube.com/watch?v=7qdHbzVcmoI&list=PLCOmiTb5WX3ptBi7tdjmAGwx8EhgcTp9o&index=7)

</td></tr></tbody>
</table>-   **[Add users to the App Engine Admin group](../task/add-users-to-admin-grp.md)**  
Add users to the App Engine Admin group in your production instance to give them administrative rights to App Engine Studio \(AES\). You must also identify a contact email address for the group. After you configure the email address of the App Engine Admin group, members can receive notifications for app development-related requests, including app intake requests.
-   **[Grant user access to AES](../task/grant-aes-access.md)**  
Control who has access to build applications in App Engine Studio \(AES\) by adding users to AES Users group or the AES User Limited group.
-   **[Manage template access](../task/manage-template-access.md)**  
Control who has access to templates in App Engine Studio \(AES\) using the app\_template\_admin role. App template admins activate and deactivate templates and grant other users access to share their templates.
-   **[Set up custom collaboration descriptors](../task/set-up-custom-collaboration-descriptors.md)**  
Customize the set of development collaborators you list in App Engine Studio \(AES\) using Guided Setup.

**Parent Topic:**[Configure App Engine Studio](../concept/configure-aes.md)

