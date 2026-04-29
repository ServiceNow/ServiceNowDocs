---
title: Assign permissions to publish custom templates
description: Assign permissions for developers to publish a custom template to the application repository or the ServiceNow Store. You can grant permissions to publish either a specific custom template or publish all existing custom templates in App Engine Studio \(AES\).Assign permissions to developers so they can publish an individual App Engine Studio \(AES\) custom template to the application repository or ServiceNow Store.Assign permissions for developers to publish custom App Engine Studio \(AES\) templates and applications to the app repository or ServiceNow Store.
locale: en-US
release: australia
product: App Engine Studio
classification: app-engine-studio
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Build a custom template, Use an app template, Create your app, Build, App Engine Studio, Building low-code applications, Developing your application, Building applications]
---

# Assign permissions to publish custom templates

Assign permissions for developers to publish a custom template to the application repository or the ServiceNow Store. You can grant permissions to publish either a specific custom template or publish all existing custom templates in App Engine Studio \(AES\).

**Parent Topic:**[Build a custom template](build-custom-template.md)

## Assign permissions to publish an individual custom template

Assign permissions to developers so they can publish an individual App Engine Studio \(AES\) custom template to the application repository or ServiceNow Store.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **App Engine** &gt; **Templates** &gt; **App Templates**.

2.  Select the personalize List icon \(![Personalize list icon.](../../../administer/ui-builder/image/gear-icon.png)\).

3.  Add the Package column by moving the **Package** value from the **Available** list to the **Selected** list and select **OK**.

4.  From the Package column, select the package link for your custom template.

5.  Under the **Related links** heading, select **Manage Collaborators**.

6.  Assign permissions to new or existing collaborators.

<table id="choicetable_zyx_htt_qsb"><thead><tr><th align="left" id="d100210e198">

Choice

</th><th align="left" id="d100210e201">

Action

</th></tr></thead><tbody><tr><td id="d100210e207">

**Assign permissions to a new user or group**

</td><td>

1.  In the **Invite people by name or group** field, enter a user name or group name to add as a collaborator.
2.  From the collaboration descriptor, select **Editor**.
3.  Select **Send**.

After the collaboration request is approved, the user or group is added as a collaborator for the custom template.

4.  From the collaboration descriptor, select **Customize**.
5.  On the Manage Collaborators window, select the **Publish To App Repo** and **Publish To App Store** check boxes.
6.  Select **Save**.


</td></tr><tr><td id="d100210e261">

**Assign permissions to an existing user or group**

</td><td>

1.  From the list of collaborators, select a user or group.
2.  Select **Customize**.
3.  On the Manage Collaborators window, select the **Publish To App Repo** and **Publish To App Store** check boxes.
4.  Select **Save**.


</td></tr></tbody>
</table>
### Result

The specified user or group now has permission to publish an individual custom template.

## Assign permissions to publish custom templates and apps

Assign permissions for developers to publish custom App Engine Studio \(AES\) templates and applications to the app repository or ServiceNow Store.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **App Engine** &gt; **Collaboration** &gt; **Descriptors**.

2.  In the **Name** field of the All Collaboration Descriptors page, search for and select **Owner**.

3.  From the **Development Permission Sets** tab, select **Edit**.

4.  Move the **Publish To App Repo** and **Publish To App Store** values from the **Collection** list to the **Development Permission sets** list.

5.  Select **Save**.


### Result

Developers who own applications now have permissions at a platform level to publish all custom templates to their application repository or ServiceNow Store.

