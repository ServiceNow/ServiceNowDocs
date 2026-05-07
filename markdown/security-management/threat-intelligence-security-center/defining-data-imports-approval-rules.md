---
title: Defining Data Imports Approval Rules
description: Use this section to define the approval rules and integrate the approval flow within the Import Intelligence section after submitting the data import.
locale: en-US
release: australia
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [About Rules Engine in TISC, Administer, Threat Intelligence Security Center, Security Operations]
---

# Defining Data Imports Approval Rules

Use this section to define the approval rules and integrate the approval flow within the Import Intelligence section after submitting the data import.

## Before you begin

Role required: sn\_sec\_tisc.admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Threat Intelligence Security Center**.

2.  Click on **Administration** icon on the workspace.

3.  Go to **Rules Engine** &gt; **Data Imports Approval Rules**.

4.  Select **Approval Rule for Data Imports**.

    Within the base system, **Approval Rule for Data Imports** is the default approval rule provisioned to allow the users to activate the approval workflow.

5.  Enter at least one user name or user group for each of **Select User or Groups requiring approval** and **Select approver\(s\)** section.

6.  Click on **Enable** button to enable the approval flow for the data imports.

    When enabled, the data imports will be in the approval queue for the approver to approve or reject the data processing. The approver will review the changes made by the analyst and then approve or reject the data import request.

    **Note:** An email notification is sent to the user\(s\) or user group\(s\) that the import job is processed and approved or rejected.


