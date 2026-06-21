---
title: Validate HTML in journal fields
description: Prevent users from saving invalid HTML in a journal field.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/platform-administration/t\_ValidateHTMLInJournalFields.html
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Render journal field entries as HTML, Journal field type, Field types, Field administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Validate HTML in journal fields

Prevent users from saving invalid HTML in a journal field.

## Before you begin

Role required: admin

## Procedure

1.  Add the property **glide.ui.allow\_deep\_html\_validation**.

    For instructions, see [Add a system property](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/platform-administration/r_AvailableSystemProperties.md).

2.  Set the **Value** to **true**.

3.  Click **Save**.

    Users now see a warning in the activity formatter when they enter invalid HTML code in a journal field.

    \[Omitted image "InvalidHTML.png"\] Alt text: Invalid HTML message


**Parent Topic:**[Render journal field entries as HTML](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/platform-administration/render-journal-field-entries-as-html.md)

