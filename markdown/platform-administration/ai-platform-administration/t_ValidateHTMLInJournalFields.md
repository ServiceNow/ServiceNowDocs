---
title: Validate HTML in journal fields
description: Prevent users from saving invalid HTML in a journal field.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/platform-administration/ai-platform-administration/t\_ValidateHTMLInJournalFields.html
release: yokohama
product: AI Platform Administration
classification: ai-platform-administration
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Render journal field entries as HTML, Journal field type, Field types reference, Field administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Validate HTML in journal fields

Prevent users from saving invalid HTML in a journal field.

## Before you begin

Role required: admin

## Procedure

1.  Add the property **glide.ui.allow\_deep\_html\_validation**.

    For instructions, see [Add a system property](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/platform-administration/ai-platform-administration/t_AddAPropertyUsingSysPropsList.md).

2.  Set the **Value** to **true**.

3.  Click **Save**.

    Users now see a warning in the activity formatter when they enter invalid HTML code in a journal field.

    \[Omitted image "InvalidHTML.png"\] Alt text: Invalid HTML message


