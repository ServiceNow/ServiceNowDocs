---
title: Embed an assessment in a record page
description: Embedded assessments lets an upstream application surface the Smart Assessment Engine responder experience inside its own UI rather than as a separate page. This task describes the configuration that must be done on the SAE and UI Builder page where the assessment is embedded
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/smart-assessment-engine/embed-assessment-in-record-page.html
release: australia
product: Smart Assessment Engine
classification: smart-assessment-engine
topic_type: task
last_updated: "2026-06-01"
reading_time_minutes: 3
keywords: [embedded assessments, UI Builder, compact mode]
breadcrumb: [Embedded assessments, Use template designer, Manage, Smart Assessment Engine, Governance, Risk, and Compliance]
---

# Embed an assessment in a record page

Embedded assessments lets an upstream application surface the Smart Assessment Engine responder experience inside its own UI rather than as a separate page. This task describes the configuration that must be done on the SAE and UI Builder page where the assessment is embedded

## Before you begin

To restrict access to the embedded assessment based on the parent record's audience, enable the **Inherit read access for embedded assessment** field on the template category. Then set the **Embedded assessment parent table** to the table whose records act as the parent. For field details and guidance on choosing the parent table, see [Create an assessment template category](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/smart-assessment-engine/sae-asmnt-template-category-create.md).

Role required: sn\_smart\_asmt.template\_manager. To configure the template category, which is a prerequisite for this task, the sn\_smart\_asmt.assessment\_admin role is also required.

## Procedure

1.  Navigate to **Workspaces** &gt; **Assessment Workspace** to access the Assessment Workspace landing page.

2.  Create a template by selecting **New template**, and then fill in the template details form.

    **Note:** You can also copy an existing template including all questions, sections, instructions, and existing configurations. For more information on how to copy an existing template refer to [Copy an assessment template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/smart-assessment-engine/sae-asmnt-template-duplicate.md).

3.  Create or open the assessment template under the template category that has the embedded assessment fields configured.

4.  Configure the trigger so that an assessment is created against each record in the parent table that needs evaluation.

5.  Open the UI Builder page where the embedded assessment will appear, and add the Smart Assessment component to it.

    **Note:** For information on adding a component to a UI Builder page, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/work-components.md). If a UI Builder page does not yet exist for the host context, see [Create a page in UI Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/create-page.md).

6.  Configure the Smart Assessment component's properties to match the layout of the host page.

    The component exposes properties that control which parts of the standard responder UI are shown. These include the assessment mode \(single or combined\) and the header mode \(standard or compact\). Additional properties control show/hide toggles for the Submit, Reassign, and Cancel actions, and a hide-all-actions toggle. You can also control visibility of the right reference pane and whether the navigation pane is pinned by default.

    -   For information on configuring component properties in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/work-components.md)
    -   For details on what each property hides or affects, including the combined-mode constraints, see [Embedded assessments](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/smart-assessment-engine/embedded-assessments.md).
7.  Save and publish the UI Builder page.

8.  Open a record in the parent table and confirm that the embedded assessment appears as configured.

    Verify that the visibility properties hide or show the expected elements. Confirm that the progress indicator remains visible when the navigation pane is not pinned. Confirm that users with read access to the parent record can view the embedded assessment.


## What to do next

If the embedded view hides assessment-level actions, the upstream application must provide equivalent controls on the host page.

-   **Submit**

    Use the **Change Assessment State** Flow Designer action to transition the assessment to the Submitted state. The action performs the minimum required validations — state eligibility and required questions answered — before transitioning. Implement any additional business-specific validations in the upstream application before invoking the action.

-   **Cancel**

    Use the same **Change Assessment State** action to transition the assessment to the Cancelled state. Implement custom pre-cancellation validations in the upstream application before calling the action.

-   **Reassign**

    Build a Reassign UI in the upstream application. The custom UI must use the Reassign Filter extension point that the built-in Reassign dialog consumes, so that the same allowed-user list is applied. After the user confirms the reassignment, call the corresponding flow action or public API to apply the change.


If the embedded view also hides the right reference pane, the upstream application must build its own contributor management UI. Call the Smart Assessment responder public API to persist contributor changes.

**Related topics**  


[Embedded assessments](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/smart-assessment-engine/embedded-assessments.md)

[UI Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/ui-builder-overview.md)

