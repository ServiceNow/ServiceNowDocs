---
title: Create a child alias for Jira Spoke alias for SPW Jira Integrations
description: Create a child connection &amp; credential alias that will be used to connect to Jira later, to enable integration between Strategic Planning and Jira.
locale: en-US
release: yokohama
product: Strategic Planning
classification: strategic-planning
topic_type: task
last_updated: "2025-12-08"
reading_time_minutes: 1
breadcrumb: [Set up a Jira instance, Configure, SPW Jira Integrations, Strategic Planning, Strategic Portfolio Management]
---

# Create a child alias for Jira Spoke alias for SPW Jira Integrations

Create a child connection &amp; credential alias that will be used to connect to Jira later, to enable integration between Strategic Planning and Jira.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Connection &amp; Credentials** &gt; **Connection &amp; Credential Aliases**.

2.  From the list of aliases, open the alias based on your Jira instance type.

    -   For Jira Cloud, open **sn\_jira\_spoke.Jira**.
    -   For Jira Server/Data Center, open **sn\_jira\_int.Jira**.
3.  Create a child alias.

    1.  From the Child Aliases related list, select **New**.

    2.  Enter a name.

        For example, **Jira instance – GenAI team**.

    3.  Select **Submit**.


## What to do next

-   For Jira Cloud: .
-   For For Jira Server/Data Center: [Create PAT for Jira Server](create-personal-access-token-pat-in-jira-server-data-center.md).

**Parent Topic:**[Setting up a Jira instance for SPW Jira Integrations](../concept/setting-up-jira-instance-spw.md)

