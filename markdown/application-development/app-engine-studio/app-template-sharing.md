---
title: App template sharing
description: Specify which users and groups have access to predefined and custom templates in App Engine Studio \(AES\).Share App Engine Studio \(AES\) templates globally, with groups, or with individual users to ensure users have access to the right templates.
locale: en-US
release: yokohama
product: App Engine Studio
classification: app-engine-studio
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Create your app using an application template, Create your app, Building apps in App Engine Studio, Build apps using App Engine Studio, Building low-code applications, Developing your application, Building applications]
---

# App template sharing

Specify which users and groups have access to predefined and custom templates in App Engine Studio \(AES\).

## Implicit sharing

Templates are implicitly shared with some users in your organization, meaning that no sharing record exists that determines sharing. The three rules governing implicit sharing are:

-   Instance administrators can see and use all templates.
-   App template admins \(users with the app\_template\_admin role\) can also see and use all templates.
-   App template authors \(users with the app\_template\_author role\) can see templates that are not shared with them if they have permission to edit the scope in which the template resides.

These sharing rules apply regardless of whether a template is active.

## Explicit sharing

You can share app templates with anyone in your organization by creating a sharing record for that user or group. However, regardless of sharing permissions, the user or group must have the sn\_app\_eng\_studio.user role to see and use the template. The three ways to share templates are:

-   Share globally with every user in your organization
-   Share with a specified user group
-   Share with a specified single user

**Note:** If you stop sharing a template with an individual user but that user is a part of any group the template is shared with, that user is still able to see and use the template.

**Parent Topic:**[Create your app using an application template](../task/use-app-template.md)

## Manage template sharing permissions

Share App Engine Studio \(AES\) templates globally, with groups, or with individual users to ensure users have access to the right templates.

### Before you begin

Role required: app\_template\_admin

### Procedure

1.  Navigate to **All** &gt; **App Engine** &gt; **Templates** &gt; **App Templates**.

2.  Select the template you want to modify sharing permissions for.

3.  In the Template Sharing Permissions related list, select **New**.

4.  Select a sharing option.

    |Choice|Permissions|
    |------|-----------|
    |**Global**|Shared with everyone in your organization.|
    |**User Group**|Shared with the groups you select from the list.|
    |**User**|Shared with individual users you select from the list.|

5.  Select **Submit**.


