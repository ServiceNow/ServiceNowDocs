---
title: Configure a wizard layout for a playbook
description: Configure a wizard layout that presents a playbook as a guided, step-by-step experience for end users.
locale: en-US
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Wizard layout, Design Playbook Experience, Playbooks, Workflow Studio, Build workflows]
---

# Configure a wizard layout for a playbook

Configure a wizard layout that presents a playbook as a guided, step-by-step experience for end users.

## Before you begin

Role required: admin, playbook.admin

Before you configure a wizard layout, ensure that you:

-   Have an existing playbook with the activities you want end users to complete. For more information, see [Create a playbook](create-process-definition.md).
-   Have access to UI Builder and can edit or create a UI Builder page to host the playbook that you created. For more information, see [Create a page in UI Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/ui-builder/create-page.md).

## Procedure

1.  In UI Builder, open the page that you created, and then in the panel, select **Add content**.

2.  In the **Add content** panel:

    1.  Select **Components**.
    2.  Expand **Playbook**.
    3.  Select the **Playbook Horizontal Wizard** layout bundle.
    4.  Select **Add**.
3.  Select the Playbook Wizard component on the canvas.

4.  In the component configuration panel:

    1.  Set the **Playbook** property to the playbook you created earlier.
    2.  Review the generated wizard steps, which are created from the playbook activities.
    3.  Update step titles or descriptions as needed to match the intended end user flow.
5.  Verify navigation behavior:

    1.  Confirm that users can move between steps using the provided navigation controls.
    2.  Verify that required fields or completion rules are enforced before users proceed.
6.  Select **Preview** to review the wizard layout as an end user.

7.  Select **Save** and then select **Publish** to publish the UI Builder page.


## Result

End users see the playbook displayed as a guided wizard, with clear step-by-step guidance and navigation that walks them through the process from start to completion.

## What to do next

-   Test the wizard layout as an end user.
-   Refine step labels or layout configuration based on feedback.
-   Reuse the wizard layout pattern for other multi-step playbooks.

**Parent Topic:**[Wizard layouts for playbooks](../concept/wizard-layouts-playbooks.md)

