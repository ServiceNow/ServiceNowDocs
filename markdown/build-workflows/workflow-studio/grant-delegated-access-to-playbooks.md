---
title: Grant delegated access to playbooks
description: Assign a user as a delegated developer so they can build playbooks within one application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/build-workflows/workflow-studio/grant-delegated-access-to-playbooks.html
release: brazil
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Delegated development access, Managing playbook permissions, Configure, Playbooks, Workflow Studio, Build workflows]
---

# Grant delegated access to playbooks

Assign a user as a delegated developer so they can build playbooks within one application.

## Before you begin

Role required: admin

Each user assignment covers one application. Configure the application scope before you assign delegated access.

## About this task

Grant delegated development access when a user should build playbooks inside a single application rather than across the instance. For more information, see [Delegated development access](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/build-workflows/workflow-studio/delegated-development-access.md).

## Procedure

1.  Navigate to the application record.

2.  Under Related Links, select **Manage Developers**.

    \[Omitted image "pb-perm-delegates.png"\] Alt text: Screenshot showing the Manage Developers option.

3.  Search for the user.

4.  In the Developers list, locate the user row and enable the **Process Automation Designer** permission set.

    To grant all application permissions instead, enable delegated admin access.

5.  Save the record.


## Result

The user receives the delegated\_developer role and an application-specific role. To build playbooks, the user must switch from the Global application scope to the scope of this application.

**Parent Topic:**[Delegated development access](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/build-workflows/workflow-studio/delegated-development-access.md)

