---
title: Create a third-party element
description: Create a third-party element directly in the Elements grid in the Third-party Risk Management application. Third-party elements are assessed as part of the due diligence workflow.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/third-party-risk-management/tprm-tp-element-create.html
release: brazil
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 4
breadcrumb: [Monitoring third-party elements, Monitor third-party risk, Third-party Risk Management, Governance, Risk, and Compliance]
---

# Create a third-party element

Create a third-party element directly in the Elements grid in the Third-party Risk Management application. Third-party elements are assessed as part of the due diligence workflow.

## Before you begin

Role required: sn\_vdr\_risk\_asmt.vendor\_assessor or sn\_vdr\_risk\_asmt.vendor\_risk\_manager

## About this task

You can create a third-party element directly in the Elements grid, either from the third party record or from an engagement's **Elements** tab. An element you create from the third-party record isn't linked to any engagement by default. An element you create from an engagement's **Elements** tab is linked to that engagement automatically. For more information about monitoring third-party elements, see [Monitoring third-party elements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/third-party-risk-management/tprm-monitor-tp-elements.md).

## Procedure

1.  Navigate to **Workspaces** &gt; **Vendor Management Workspace**.

2.  Navigate to the third party or engagement where you want to create the element.

    -   To create an element that isn't linked to an engagement, select the list icon \[Omitted image "ws-list-icon.png"\] Alt text: and then navigate to **Third parties** &gt; **All third parties**, and select the third party you want.
    -   To create an element that's linked to an engagement automatically, select the list icon \[Omitted image "ws-list-icon.png"\] Alt text: and then navigate to **Third parties** &gt; **All engagements**, and select the engagement you want.
3.  Navigate to the **Elements** tab.

4.  Select **New**.

5.  Fill in the fields for the new element.

    For the complete list of fields on the third-party element record, see [Third-party element form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/third-party-risk-management/tprm-tpe-form.md).

    **Note:** The classification determines which scoring model is applied to the element. To create additional classifications, navigate to **All** &gt; **Third-party Risk Management** &gt; **Third-party Elements** &gt; **Classifications**.

    On an engagement's **Elements** tab, the grid also displays a non-editable **Risk rating** column showing the element's current risk rating for that engagement. Because this rating is calculated using the scoring rule and business service criticality of the engagement it's linked to, the same element can show a different risk rating on different engagements.

    Depending on the classification you select, more fields specific to that classification appear. For example, selecting **AI model** as the classification for an AI use case element enables you to link one or more AI models to that use case. For more information, see [Manage elements in the grid](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/third-party-risk-management/tprm-elements-grid-manage.md).

6.  Select **Save**.


## What to do next

If you created the element from the third-party record, link it to an engagement before you assess it. For information about linking elements to engagements, see [Add a third-party element record to an engagement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/third-party-risk-management/tprm-tp-element-engagement.md).

To manage elements, including linking AI models to AI use cases, see [Manage elements in the grid](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/third-party-risk-management/tprm-elements-grid-manage.md).

You can also create elements through the due diligence workflow. For information about element collection tasks, see [Complete an element collection task](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/third-party-risk-management/tprm-elements-task-manage.md) and [Create a task for an internal user](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/third-party-risk-management/tprm-internal-tasks.md).

After you link the elements to an engagement, you can start the due diligence process. For information about monitoring third-party elements, see [Monitoring third-party elements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/third-party-risk-management/tprm-monitor-tp-elements.md).

**Related topics**  


[Third-party element form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/third-party-risk-management/tprm-tpe-form.md)

[Add a third-party element record to an engagement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/third-party-risk-management/tprm-tp-element-engagement.md)

[Monitoring third-party elements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/third-party-risk-management/tprm-monitor-tp-elements.md)

[Manage elements in the grid](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/third-party-risk-management/tprm-elements-grid-manage.md)

[Complete an element collection task](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/third-party-risk-management/tprm-elements-task-manage.md)

[Create a task for an internal user](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/third-party-risk-management/tprm-internal-tasks.md)

