---
title: Activate a flow for Email Interaction for CSM
description: Activate flows for customers who have the Email Interaction for CSM application configured, enabling efficient workflow automation.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
keywords: [Email Interaction for CSM]
breadcrumb: [Configure flows for incoming emails, Email Interaction, Email channel, Configure, Enable communication channels, Configure, Customer Service Management]
---

# Activate a flow for Email Interaction for CSM

Activate flows for customers who have the Email Interaction for CSM application configured, enabling efficient workflow automation.

## Before you begin

Role required: admin

## About this task

For new CSM customers, the inbound actions are activated by default. Existing CSM customers should activate email interaction related flows and deactivate the case related flows.

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  Open a flow from the available flows.

    -   Create Interaction from Email
    -   Update Interaction from Email
    -   Update Case via Reply for EaaI
3.  Select **AND**.

4.  Select the filter condition: **To** contains **customerservice@example.com**.

    **Note:** **customerservice@example.com** is a sample email address. Specify the actual email address that should be configured as the default for creating email interactions.

5.  Activate the selected flow by selecting **Activate**.


## Result

All the available flows are activated.

