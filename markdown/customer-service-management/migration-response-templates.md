---
title: Configure response templates
description: Response templates let agents insert standard, prewritten replies into email and chat responses. They aren't available in CSM Agent Workspace, so there's nothing to migrate. Configure them in CSM Configurable Workspace to help agents respond faster and more consistently.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/customer-service-management/migration-response-templates.html
release: australia
topic_type: task
last_updated: "2026-11-12"
reading_time_minutes: 1
breadcrumb: [Migrate to CSM Configurable Workspace, Migrating to CSM Configurable Workspace, CSM Configurable Workspace, Organize agent workspaces, Configure, Customer Service Management]
---

# Configure response templates

Response templates let agents insert standard, prewritten replies into email and chat responses. They aren't available in CSM Agent Workspace, so there's nothing to migrate. Configure them in CSM Configurable Workspace to help agents respond faster and more consistently.

## Before you begin

Role required: admin

## About this task

Response templates give agents a library of approved, reusable replies, such as an acknowledgment message or a standard set of troubleshooting steps. Agents can add a template to an email or chat in one click, which reduces typing and keeps customer messages consistent.

**Note:** Response templates are different from form templates. Form templates prefill fields on a record and carry over from CSM Agent Workspace. Response templates insert text into the email or chat composer and are new in CSM Configurable Workspace.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Response Template Configuration**.

2.  Select **New**.

3.  Enter a **Name** and **Short Name** for the template, and in the **Table** field, select the table that the template applies to, such as Case.

4.  In the **Template body** field, enter the template text.

    To insert record values automatically, such as the customer name or case number, select fields from the **Select variables** panel.

5.  In the **Condition** field, set any conditions that control when the template is available to agents.

6.  Select **Submit**.


## Result

Open a case in CSM Configurable Workspace and confirm that the response template is available in the email and chat composer.

