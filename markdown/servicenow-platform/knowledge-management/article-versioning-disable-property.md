---
title: Disable the article versioning feature
description: Users with the system administrator role can disable the article versioning feature by setting a property.
locale: en-US
release: australia
product: Knowledge Management
classification: knowledge-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Use article versioning, Using Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Disable the article versioning feature

Users with the system administrator role can disable the article versioning feature by setting a property.

## Before you begin

Role required: admin

## About this task

The **Enable article versioning feature**\(glide.knowman.versioning.enabled\) property controls the article versioning feature. Setting this property to **false** disables the article versioning feature. Once disabled:

-   The **Version** field is removed from the Knowledge form. The **Version** column remains on the Knowledge list and can be removed manually.
-   The **Article Versions** related list is removed from the Knowledge form.
-   The **Recall**, **Checkout**, and **Make this current** buttons are removed from the Knowledge form.
-   Outdated articles are removed from Knowledge list views.
-   The version history does not appear on the article view page.

Articles continue to be versioned in the background. Minor versions are incremented until an article is published and then the version number is increased to the next major version.

Users can still access outdated articles that have been attached to incidents. Outdated articles include a message that an updated article is available.

## Procedure

1.  Navigate to **All** &gt; **Knowledge** &gt; **Administration** &gt; **Properties**.

2.  Locate the **Enable article versioning feature** property in the Article Versioning Properties section.

3.  Click the check box to disable the property.

4.  Click **Save**.


**Parent Topic:**[Use article versioning](../concept/use-article-versioning_0.md)

