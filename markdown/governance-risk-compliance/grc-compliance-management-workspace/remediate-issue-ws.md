---
title: Remediate an issue using the Compliance Workspace
description: After an issue has been identified, triaged, and investigated using the Compliance Workspace, you can remediate it.
locale: en-US
release: australia
product: GRC: Compliance Management Workspace
classification: grc-compliance-management-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Manage issues using the Compliance Workspace, Use, GRC Compliance workspace, Policy and Compliance Management, Governance, Risk, and Compliance]
---

# Remediate an issue using the Compliance Workspace

After an issue has been identified, triaged, and investigated using the Compliance Workspace, you can remediate it.

## Before you begin

Role required: \(per product\)

-   In Policy and Compliance Management: compliance\_admin, compliance\_manager, or sn\_compliance.user
-   In Risk Management: risk\_admin, risk\_manager, or sn\_risk.user
-   In Audit Management: audit\_admin, audit\_manager, audit\_admin, or sn\_audit.user

## About this task

Remediating an issue marks an intention to fix the underlying issue causing the control failure or risk exposure. Accepting an issue marks an intention to create an exception for a known control failure or risk. Controls that are **Accepted** remain in a non-compliant state until the control is reassessed. In this way, the issue can be used to document observations during audits.

## Procedure

1.  Open the issue you want to remediate.

2.  Click the **Remediation Tasks** tab.

    **Note:** You have two options for creating a remediation task:

    -   Click **Suggested Remediation Tasks** and click **Copy** to use an existing task as a basis for creating this task. A copy of the selected remediation task is created with certain information from that task copied to the new task. You can manually complete the other fields.
    -   Clicking **New** and manually creating the task.
3.  On the form, fill in or modify the fields.

    |Field|Description|
    |-----|-----------|
    |Number|Unique identification number.|
    |Assigned to|Select the user responsible for working this task.|
    |Issue|The issue for which this task was created.|
    |State|The current state of the task.|
    |Priority|Select the priority or sequence this task needs to be resolved, based on its impact and urgency.|
    |Watch list|Select users who want to be notified when changes occur.|
    |Created/Updated|Displays the date/time when the task was created and updated.|
    |Short description|Enter a brief description of the task. This will appear in lists of tasks.|
    |Description|Enter a complete description of the task.|
    |Notes and Comments|
    |Additional comments|As needed, enter any customer-facing comments related to this task.|
    |Work notes|Enter any non-customer-facing notes related to the remediation of the issue.|
    |Task Schedule|
    |Planned duration|Estimated amount of work time. Calculated using the **Planned start date** and **Planned end date**.|
    |Planned start date|Date and time that work on the task is expected to begin.|
    |Planned end date|Date and time that work on the task is expected to end.|
    |Actual duration|Amount of actual work time. Calculated using the **Actual start date** and **Actual end date**.|
    |Actual start date|Time when work began on this task.|
    |Actual end date|Time when work on this task was completed.|

4.  Click **Submit**.


