---
title: Update a conditions field to use condition builder v2
description: In Core UI, you can update a conditions field to display the version 2 condition builder.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/ai-platform-administration/configure-condition-builder.html
release: australia
product: AI Platform Administration
classification: ai-platform-administration
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Condition field types, Reference, Field administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Update a conditions field to use condition builder v2

In Core UI, you can update a conditions field to display the version 2 condition builder.

## Before you begin

Role required: admin

## About this task

You add a dictionary attribute to the Conditions field to enable condition builder version 2 \(v2\).

\[Omitted image "condition-builder-v2.png"\] Alt text: Condition builder v2 on Approval Rules form

## Procedure

1.  Open the form with the condition builder to configure.

2.  Right-click the **Conditions** label and click **Configure Dictionary**.

3.  In the **Attributes** field, enter `condition_builder=v2`.

    If attributes exist, add this string at the end separated by a comma.

4.  Select **Update**.

    The form reloads with the v2 version of the condition builder.


