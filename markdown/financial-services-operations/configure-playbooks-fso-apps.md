---
title: Configure playbooks
description: Review the playbooks that are available with Financial Services Operations applications to check they align to your business processes. You may need to customize them or design new ones as needed. You can still use the playbook activity definitions.​
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure, Financial Services Operations \(FSO\)]
---

# Configure playbooks

Review the playbooks that are available with Financial Services Operations applications to check they align to your business processes. You may need to customize them or design new ones as needed. You can still use the playbook activity definitions.​

## Before you begin

Ensure that the scope is selected for the application for which you are configuring a playbook. For more information, see [Application picker](https://www.servicenow.com/docs/access?context=c_ApplicationPicker&version=zurich&pubname=zurich-application-development&ft:locale=en-US).

Role required: Based on the application that you are configuring, you need the following roles:

-   For Financial Services Card Operations: sn\_bom\_credit\_card.admin and admin
-   For Financial Services Complaint Management: sn\_bom\_compl.admin and admin
-   For Financial Services Business Lifecycle: sn\_bom\_clo\_b2b.admin and admin
-   For Financial Services Client Lifecycle: sn\_bom\_clo\_b2c.admin and admin
-   For Financial Services Business Deposit Operations: sn\_bom\_deposit\_b2b.admin and admin
-   For Financial Services Personal Deposit Operations: sn\_bom\_deposit\_b2c.admin and admin
-   For Commercial Lines Claims: sn\_ins\_claim\_cml.admin and admin
-   For Individual Life Servicing: sn\_ins\_policy\_b2c.admin and admin
-   For Group Life Servicing: sn\_ins\_policy\_b2b.admin and admin
-   For Financial Services Business Loan Operations: sn\_bom\_loan\_b2b.admin and admin
-   For Financial Services Personal Loan Operations: sn\_bom\_loan.b2c\_admin and admin
-   For Financial Services Treasury Operations: sn\_bom\_treasury.admin and admin
-   Individual Life Claims: sn\_ins\_claim\_indl.admin and admin
-   Insurance claims: sn\_ins\_gen\_claim.admin and admin

## About this task

The playbooks are built using ServiceNow Playbooks, so make sure you’re familiar with [Process Automation Designer](https://www.servicenow.com/docs/access?context=process-automation-designer&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US) basics.

For information on playbooks that are installed with Financial Services Operations applications, see [Playbooks for Financial Services Operations applications](../reference/playbooks-fso-apps.md).

**Note:** The playbooks in Financial Services Operations applications use the **CSM Configurable Workspace Playbook** playbook experience.

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Process Automation Designer**.

2.  Create or modify a playbook.

    -   To create a playbook, click **New**.
    -   To modify a predefined playbook, open the playbook from the list.
    For information on how to create or modify playbooks, see [Create a process definition](https://www.servicenow.com/docs/access?context=create-process-definition&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US).

3.  Click **Save**.

4.  Test your playbook and click **Activate**.

    For more information, see [Test a process](https://www.servicenow.com/docs/access?context=test-process&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US).


