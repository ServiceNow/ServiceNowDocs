---
title: Hide the attachment \[view\] link
description: Users can open an attachment by clicking either the file name or the \[view\] link. The \[view\] link opens the file from within the browser, which executes JavaScript code as part of the attachment. You can hide the \[view\] link. Users can still view attachments by clicking the file name.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Administering attachments, Administering forms, Form administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Hide the attachment \[view\] link

Users can open an attachment by clicking either the file name or the **\[view\]** link. The **\[view\]** link opens the file from within the browser, which executes JavaScript code as part of the attachment. You can hide the **\[view\]** link. Users can still view attachments by clicking the file name.

## Before you begin

Role required: Admin.

## Procedure

1.  Add the **glide.ui.disable\_attachment\_view** and **glide.ui.attachment\_popup** properties.

    For instructions on adding properties to the platform, see [Add a system property](../../reference-pages/reference/r_AvailableSystemProperties.md#).

2.  For the **glide.ui.disable\_attachment\_view** property, set the **Type** to **true/false** and set the **Value** to **true**.

3.  For the **glide.ui.attachment\_popup** property, set the **Type** to **true/false** and set the **Value** to **false**.

4.  To return to the default behavior \(enable the link\), set the **glide.ui.attachment\_popup** property **Value** to **true**.


**Parent Topic:**[Administering attachments](../reference/r_AdministeringAttachments.md)

