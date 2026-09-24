---
title: Manage elements in the grid
description: Manage third-party elements in the Elements grid by adding, editing, and deleting records. You can also link AI models to AI use case elements in the Third-party Risk Management application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/third-party-risk-management/tprm-elements-grid-manage.html
release: brazil
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: task
last_updated: "2026-09-14"
reading_time_minutes: 4
breadcrumb: [Monitoring third-party elements, Monitor third-party risk, Third-party Risk Management, Governance, Risk, and Compliance]
---

# Manage elements in the grid

Manage third-party elements in the Elements grid by adding, editing, and deleting records. You can also link AI models to AI use case elements in the Third-party Risk Management application.

## Before you begin

Role required:

-   Vendor Management Workspace: sn\_vdr\_risk\_asmt.vendor\_assessor, sn\_vdr\_risk\_asmt.vendor\_risk\_manager
-   Third-party portal: vendor\_contact

For more information, see [Create a task for an internal user](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/third-party-risk-management/tprm-internal-tasks.md).

## About this task

The Elements grid is available on a third party record, on an engagement's **Elements** tab, and embedded in a collection task in the Vendor Management Workspace or third-party portal. Some fields in the grid are specific to the element's classification. For example, AI model and AI use case elements have fields that don't apply to other classifications.

The grid organizes elements into a tab for each classification. Tabs can include: **Principal**, **Facility**, **Product**, **AI model**, **AI use case**, and **Other**. If you create a classification, its tab is added automatically in the order set on the classification record.

Depending on your role, the **Classification** and **Third party** fields can be read-only when you edit or create an element in the grid. When all fields in the side panel are read-only, the **Save** button isn't shown.

Third-party portal users with the vendor\_contact role can access the Elements grid to add and edit elements as part of element collection workflows. Whether a field is read-only depends on the portal user's role and the task context.

## Procedure

1.  Open the Elements grid.

    -   From a third-party or engagement record, navigate to the **Elements** tab.
    -   From a collection task, select **Manage elements**.
2.  To add an element, select **Add** and fill in the fields for the new element.

    Some fields are static and appear for every element regardless of classification. Other fields are dynamic and appear only for certain classifications. AI use case and AI model elements have additional dynamic fields beyond the static fields shared by every element. For the complete list of dynamic fields for these classifications, see [AI use case and AI model element fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/third-party-risk-management/tprm-tpe-ai-fields-form.md).

3.  To edit an element, select it in the grid.

    A side panel opens showing the element's form.

4.  If you're adding or editing an AI model element, select or clear **Global AI model**.

    A global AI model is available for linking to AI use case elements across multiple third parties. A local AI model \(with **Global AI model** cleared\) is available only within the third party where it was created.

5.  If you're adding or editing an AI use case element, link the AI models that the use case relies on.

    You can link AI models created within the same third party and any AI model marked as global by another third party.

6.  Select **Save**.

7.  To delete or unlink and element, select the element in the grid, then select **Delete**.

    This option is not available to third-party contacts.

    On a third party's Elements grid, this permanently deletes the element record and its engagement associations. On an engagement's **Engagement elements** grid, this only unlinks the element from that engagement; the element record itself isn't deleted and remains available on the third party.


## Result

Elements you add appear in the grid. Elements linked to an engagement are available for assessment in your due diligence process.

When you open an element in the side panel, certain fields can be read-only depending on your role and the element's context:

-   For TPR assessors and managers in the Vendor Management Workspace, most fields are editable to support element management.
-   For third-party portal users with the vendor\_contact role, some fields \(such as Classification or Third party\) can be read-only to maintain data consistency during element collection tasks.
-   When all fields in a side panel are read-only, the **Save** button doesn't appear.

**Related topics**  


[Monitoring third-party elements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/third-party-risk-management/tprm-monitor-tp-elements.md)

[Create a third-party element](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/third-party-risk-management/tprm-tp-element-create.md)

[Add a third-party element record to an engagement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/third-party-risk-management/tprm-tp-element-engagement.md)

[Complete an element collection task](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/third-party-risk-management/tprm-elements-task-manage.md)

