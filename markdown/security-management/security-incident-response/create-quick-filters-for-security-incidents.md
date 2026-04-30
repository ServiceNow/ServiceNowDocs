---
title: Create quick filters for Security Incidents and Response Tasks lists
description: Create quick filters to create reusable, predefined filters that appear on the security incidents and response tasks list pages enabling security analysts to filter the list items without adding the filter conditions each time.
locale: en-US
release: yokohama
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-02-04"
reading_time_minutes: 2
breadcrumb: [Configure, Security Incident Response Workspace, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Create quick filters for Security Incidents and Response Tasks lists

Create quick filters to create reusable, predefined filters that appear on the security incidents and response tasks list pages enabling security analysts to filter the list items without adding the filter conditions each time.

## Before you begin

Role required: sn\_si.admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Security Incident Response Workspaces** &gt; **Administration**.

2.  Navigate to **Quick Filters** &gt; **Filters**.

3.  On the Filters page, select **New**.

4.  On the Create New Quick Filters, fill in the fields.

    | | |
    |---|---|
    |Name|Name for the filter.|
    |Active|Option to set the filter active.|
    |Table|The table on this filter is to be applicable.|
    |Order|Controls the display order of this filter. Lower sequence numbers appear first.|
    |Conditions|Use the [condition builder](https://www.servicenow.com/docs/access?context=c_ConditionBuilder&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US) to define the criteria to be filtered.|

5.  Select **Save**.


## Result

The newly created filter is saved and appears on the Filter page.

**Parent Topic:**[Configuring SIR Workspace](../reference/configuring-security-incident-response-workspace.md)

**Related topics**  


[Set up view of SIR Records](../concept/set-up-view-of-sir-records.md)

[Configure SI design time investigation](../concept/configure-investigation-canvas-records.md)

[SIR Workspace Related Records](../concept/sir-records.md#)

[Define the new Risk Score Calculator Rules](define-risk-score-calculator-rules-sir.md)

[Configure Shift Handover](../concept/config-shift-handover.md)

[Security Incident Response conference call integration](../concept/sir-conf-call-capability.md)

[Configure report templates in Security Incident Response](../concept/daily-status-sir.md)

[On-Call scheduling in Security Incident Response](../concept/on-call-schedule-sir.md)

[Category management in Security Incident Response](../concept/category-management-sir.md)

[View and update Security Incident Response system properties](../concept/view-update-sirw-system-properties.md)

