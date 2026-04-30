---
title: Enable the Show more link in the Activity stream
description: Enable the Show more link in Activity stream to configure the details you want to see in emails displayed in the Activity stream. You can select the email details you want to see, for example sent/received emails.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Administering Activity stream for Configurable Workspace, Administering Configurable Workspace, Configurable Workspace UI, Configure UIs and portals, Configure user experiences]
---

# Enable the Show more link in the Activity stream

Enable the Show more link in Activity stream to configure the details you want to see in emails displayed in the Activity stream. You can select the email details you want to see, for example sent/received emails.

## Before you begin

Ensure the **glide.ui.activity.email\_roles**property value is updated with the user's role so they can view the email option.

Role required: admin

## About this task

The Show email details link enables you to select or deselect the following details: Assigned to, attachments, configurations items, impact, incident state, opened by, priority, relationship changes, resolution code, resolution notes, sent/received emails, and work notes.

The **Show more** link appears at the bottom of a post in Activity stream.

## Procedure

1.  Enter `sys_properties.list` in the filter navigator.

2.  Select **glide.email.smtp.active** from the list.

3.  Set the Value field to `true`.

4.  Select **Update**.


## What to do next

If you're testing on an OOB instance, set the testing email address in the glide.email.test.user system property.

