---
title: Set up the Next Experience email client in the Core UI
description: Access email features from the Next Experience in the Core UI.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Forms in the classic environment, Working in the classic environment, Working in Core UI, Configure UIs and portals, Configure user experiences]
---

# Set up the Next Experience email client in the Core UI

Access email features from the Next Experience in the Core UI.

## Before you begin

Role required: admin

## About this task

The **glide.ui.load\_seismic\_email\_client** system property provides access to the latest email client features from the Next Experience in the Core UI.

**Note:** You may need to rewrite on-load business rules related to the email client table. For example, if any business rules affect UI, you must rewrite those business rules and tag them to the **sys\_email\_draft** table.

There's two places you can access the Next Experience email client from the Core UI.

-   Access the email client from the More Actions menu \(![More Actions icon](../image/x-more-actions-icon.png)\).
-   Access the email client from an Activity stream email card by selecting **Reply**, **Reply All**, or **Forward**.

The Next Experience email client provides these features in the Core UI.

-   Draft management and automatic draft saving
-   Email templates, response templates, and quick messages
-   Now Assist features

These Core UI email client features aren’t available after enabling the Next Experience email client.

-   Downloading or removing multiple attachments at once
-   Sending S/MIME and SMS
-   Customized email components

## Procedure

1.  Navigate to `sys_properties.list`.

2.  Add a system property named **glide.ui.load\_seismic\_email\_client**.

    For more information on adding system property, see [Add a system property](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/r_AvailableSystemProperties.md).

3.  Set the Value field to **true**.

4.  Select **Submit**.


**Parent Topic:**[Forms in the classic environment](../../../use/using-forms/concept/c_UsingForms.md)

