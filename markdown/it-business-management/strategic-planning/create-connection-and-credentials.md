---
title: Create connection and credentials for SPW Jira Integrations
description: Using your Jira instance details, create a connection and credential for the child alias, which is used to enable the two-way sync of work item updates between Strategic Planning Workspace and Jira.
locale: en-US
release: australia
product: Strategic Planning
classification: strategic-planning
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Set up a Jira instance, Configure, SPW Jira Integrations, Strategic Planning, Strategic Portfolio Management]
---

# Create connection and credentials for SPW Jira Integrations

Using your Jira instance details, create a connection and credential for the child alias, which is used to enable the two-way sync of work item updates between Strategic Planning Workspace and Jira.

## Before you begin

1.  [Create a child alias for Jira Spoke alias for SPW Jira Integrations](create-child-alias-for-jira-spoke-alias.md).
2.   or [Create Personal Access Token in Jira Server/Data Center for SPW Jira Integrations](create-personal-access-token-pat-in-jira-server-data-center.md).

Role required: admin or sn\_jira\_int.admin

## About this task

This task is performed for Jira Server/Data Center type instances only. For Jira Cloud, follow the steps of OAuth authentication. For more information, see [Option 1: Using OAuth authentication \(Authorization Code grant type\)](https://www.servicenow.com/docs/access?context=setup-jira-spk-opt2&version=australia&pubname=australia-integrate-applications&section=setup-jira-spk-oauth&ft:locale=en-US).

## Procedure

1.  Navigate to **All** &gt; **Connection &amp; Credentials** &gt; **Connection &amp; Credential Aliases**.

2.  From the list of aliases, open **sn\_jira\_int.Jira**

3.  From the Child Aliases related list, open the child alias record that you created earlier.

4.  From the Connection &amp; Credential Aliases form, select **Create New Connection &amp; Credential** related link.

5.  On the form, fill in the fields.

    For field information, see [Create Connection &amp; Credential form](../reference/create-connection-credential-form.md).

6.  Select **Create**.


## What to do next

[Create Jira instance for SPW Jira Integrations](create-jira-instance.md).

**Parent Topic:**[Setting up a Jira instance for SPW Jira Integrations](../concept/setting-up-jira-instance-spw.md)

