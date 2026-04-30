---
title: Create Personal Access Token in Jira Server/Data Center for SPW Jira Integrations
description: Create a Personal Access Token \(PAT\) for your Jira Server/Data Center instance, which is later used to create a connection between Strategic Planning and Jira.
locale: en-US
release: yokohama
product: Strategic Planning
classification: strategic-planning
topic_type: task
last_updated: "2025-12-08"
reading_time_minutes: 1
breadcrumb: [Set up a Jira instance, Configure, SPW Jira Integrations, Strategic Planning, Strategic Portfolio Management]
---

# Create Personal Access Token in Jira Server/Data Center for SPW Jira Integrations

Create a Personal Access Token \(PAT\) for your Jira Server/Data Center instance, which is later used to create a connection between Strategic Planning and Jira.

## Before you begin

-   [Create a child alias for Jira Spoke alias for SPW Jira Integrations](create-child-alias-for-jira-spoke-alias.md).
-   Set up a MID server. See [Tips to set up your MID Server](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0535145).

Role required: NA

## About this task

This task is performed outside the ServiceNow instance.

**Important:** A Jira Server account is used to create the PAT. After establishing the integration, any updates that are made in Strategic Planning Workspace will show up in Jira as done by this logged-in user. So, it is recommended that this account that is used to generate the PAT is either an admin or a placeholder user profile that is not used to make any updates in Jira once the integration is complete. If this user makes any updates in Jira, it may result in cyclic changes.

## Procedure

1.  Log into your Jira Server instance.

2.  Navigate to your profile.

3.  From your profile details, select **Personal Access Tokens** from the left navigation menu.

4.  Select **Create token**.

5.  Enter the details of name and expiry period.

6.  Select **Create**.

7.  Copy the created token and store it securely to retrieve it for later steps.


## What to do next

Use this PAT as password while creating connection and credential for your Jira alias. See [Create connection and credentials for SPW Jira Integrations](create-connection-and-credentials.md).

**Parent Topic:**[Setting up a Jira instance for SPW Jira Integrations](../concept/setting-up-jira-instance-spw.md)

