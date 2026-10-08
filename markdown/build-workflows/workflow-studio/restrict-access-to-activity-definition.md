---
title: Restrict access to an activity definition
description: Limit which users can add a specific activity definition to a playbook.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/build-workflows/workflow-studio/restrict-access-to-activity-definition.html
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Content access filtering, Managing playbook permissions, Configure, Playbooks, Workflow Studio, Build workflows]
---

# Restrict access to an activity definition

Limit which users can add a specific activity definition to a playbook.

## Before you begin

Role required: playbook.admin

## About this task

Set **Required Roles** when an activity is sensitive and only certain roles should use it. Required roles override content access filtering, so a user without the required role can't use the activity definition even when a content filtering rule grants access to it.

**Note:** Both the playbook.admin and pd\_content\_author roles can edit activity definitions, but only the playbook.admin role can edit the **Required Roles** field.

## Procedure

1.  Navigate to **Process Automation** &gt; **Playbook Administration** &gt; **Activity Definition**.

2.  Select the activity definition you want to restrict access to.

3.  In the **Required Roles** field, add the roles that a user must have to use this activity definition.

4.  Select **Update**.


## Result

Users without one of the required roles can't select the activity definition when they build a playbook. Playbooks that already contain the activity definition open read-only for those users.

**Parent Topic:**[Content access filtering](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/build-workflows/workflow-studio/content-access-filtering-playbooks.md)

