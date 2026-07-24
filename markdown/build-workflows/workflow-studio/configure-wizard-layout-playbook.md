---
title: Configure a Wizard layout playbook
description: Build a wizard-driven Playbook to present a playbook as a guided, step-by-step experience that walks end users through a process one activity at a time. The Wizard layout adds numbered step navigation and forward and back controls to a standard playbook.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/build-workflows/workflow-studio/configure-wizard-layout-playbook.html
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2026-06-08"
reading_time_minutes: 2
breadcrumb: [Design Playbook Experience, Playbooks, Workflow Studio, Build workflows]
---

# Configure a Wizard layout playbook

Build a wizard-driven Playbook to present a playbook as a guided, step-by-step experience that walks end users through a process one activity at a time. The Wizard layout adds numbered step navigation and forward and back controls to a standard playbook.

## Before you begin

Role required: playbook.admin, pd\_author, or playbook.write and ui\_builder\_admin or admin

Have an activated playbook with the activities you want end users to complete in sequence. The activities and their order in the playbook directly map to the wizard's steps, so order the activities in Workflow Studio before you start. For more information, see [Create a playbook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/create-process-definition.md).

## About this task

A wizard-driven Playbook uses the Playbook Horizontal Wizard bundle to render a playbook as a sequential wizard at runtime. Each playbook activity is a wizard step. End users move forward and back through the activities using explicit navigation controls, and completion rules make sure that required information is provided before they proceed.

Use a wizard layout when end users benefit from explicit guidance through a multi-step process, when activities must be completed in a specific order, or when limiting distraction by focusing the user on one step at a time matters more than letting them move freely between activities.

**Note:** For complex playbooks with branching logic, consider a Guided Decision Playbook instead. For playbooks where users should see and interact with multiple activities at once, consider a Focused or Stacked layout.

\[Omitted image "playbk-wizard-layout.png"\] Alt text: Screenshot showing the runtime UI experience for the wizard layout.

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder** &gt; **Experiences**.

2.  Go to UI Builder, and create or open an Experience to host the playbook so end users can access it from the Playbook Experience, and create a page.

    For more information, see .

3.  Open the page that you created, and then in the panel select **Add content**.

4.  Add the Playbook Horizontal Wizard layout bundle to the page so the playbook renders as a wizard experience at runtime.

    1.  Select **Components**.

    2.  Search for **Playbook**.

    3.  Select the **Playbook Horizontal Wizard** layout bundle.

    4.  Select **Add**.

    \[Omitted image "playbk-wizard-component.png"\] Alt text: Screenshot showing the Playbook horizontal wizard layout bundle.

5.  Select the Playbook Wizard component on the canvas.

6.  Update step titles or descriptions in the component configuration panel to match the intended end user flow.

    1.  Select the Playbook Wizard component on the canvas.

    2.  Set the **Playbook** property to the playbook you created earlier.

    3.  Review the generated wizard steps, which are created from the playbook activities.

    4.  Update step titles or descriptions as needed to match the intended end user flow.

7.  Verify navigation behavior.

    1.  Confirm that users can move between steps using the provided navigation controls.

    2.  Verify that required fields or completion rules are enforced before users proceed.

8.  Select **Preview** to review the wizard layout as an end user.

9.  Select **Save** and then select **Publish** to publish the UI Builder page.


## Result

End users see the playbook as a guided wizard, with clear step-by-step guidance and navigation that walks them through the process from start to completion.

## What to do next

-   Test the wizard layout as an end user.
-   Refine step labels or layout configuration based on feedback.
-   Reuse the wizard layout pattern for other multi-step playbooks.

