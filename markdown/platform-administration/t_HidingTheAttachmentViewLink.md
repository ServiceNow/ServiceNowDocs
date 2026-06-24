---
title: Hide the attachment \[view\] link
description: Users can open an attachment by clicking either the file name or the \[view\] link. The \[view\] link opens the file from within the browser, which executes JavaScript code as part of the attachment. You can hide the \[view\] link. Users can still view attachments by clicking the file name.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-administration/t\_HidingTheAttachmentViewLink.html
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Attachments, Administer, Form administration, Forms, fields, and lists, Configure core features, Administer]
---

# Hide the attachment \[view\] link

Users can open an attachment by clicking either the file name or the **\[view\]** link. The **\[view\]** link opens the file from within the browser, which executes JavaScript code as part of the attachment. You can hide the **\[view\]** link. Users can still view attachments by clicking the file name.

## Before you begin

Role required: Admin.

## Procedure

1.  Add the **glide.ui.disable\_attachment\_view** and **glide.ui.attachment\_popup** properties.

    For instructions on adding properties to the platform, see [Add a system property](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/t_AddAPropertyUsingSysPropsList.md).

2.  For the **glide.ui.disable\_attachment\_view** property, set the **Type** to **true/false** and set the **Value** to **true**.

3.  For the **glide.ui.attachment\_popup** property, set the **Type** to **true/false** and set the **Value** to **false**.

4.  To return to the default behavior \(enable the link\), set the **glide.ui.attachment\_popup** property **Value** to **true**.


**Parent Topic:**[Administering attachments](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/r_AdministeringAttachments.md)

