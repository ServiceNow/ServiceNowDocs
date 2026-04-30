---
title: Add a Generate Resolution Plan declarative action to the Service Operations Workspace
description: Enable access to the Platform Generate resolution plan agentic workflow for users in the Service Operation Workspace for active Incidents.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-08-06"
reading_time_minutes: 2
breadcrumb: [Generate resolution plan, Platform agentic workflows, Now Assist agentic workflows, Now Assist AI assets, Enable AI experiences]
---

# Add a Generate Resolution Plan declarative action to the Service Operations Workspace

Enable access to the Platform Generate resolution plan agentic workflow for users in the Service Operation Workspace for active Incidents.

## Before you begin

Role required: admin

## About this task

The following procedure adds a **Generate Resolution Plan** button and agentic workflow status card to the Service Operations Workspace. This declarative action enables your users to execute the agentic workflow without having to use the Now Assist panel.

For additional context and help, see [this Community article](https://www.servicenow.com/community/now-assist-articles/now-assist-for-csm-handling-custom-scenarios-around-now-assist/ta-p/3018803).

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.

2.  Select the **Experiences** tab, then search for `Service Operations Workspace`.

3.  Open **Record** &gt; **SRP Record**.

4.  In the Content panel, find **Ribbon Container**, select the Configure icon ![](../image/three-dots-icon.png), then select **Add before**.

    The following steps add the collapsible section on the top of the page that includes the processing messages as the agentic workflow executes.

5.  Add the **AI Agent Status Card** component.

    1.  In the **Controller** dropdown, select **UXC Gen AI Controller**, select the **AI-Agent-Status-Card**.

    2.  Select **Apply**.

    ![The content pane with an AI Agent Status Card component before the Ribbon Container](../image/add-grp-sow-content-pane.png)

6.  Bind data to the **AI Agent Status Card** component.

    1.  In the Edit modal Configure tab next to the **Table** field, select the bind data icon ![](../image/bind-data-icon.png).

    2.  Select **props** &gt; **table**, then select **Apply**.

    3.  Next to the **sys\_id** field, select the bind data icon ![](../image/bind-data-icon.png).

    4.  Select **props** &gt; **sys\_id**, then select **Apply**.

    ![The Edit component modal with the Table and sys_id fields with bound data](../image/add-grp-sow-bind.png)

7.  Assign events to the **AI Agent Status Card** component.

    1.  In the Events tab of the data drawer, select **Add event mapping**.

        If you do not see the Events tab, refresh the page.

    2.  Select the Execution completed event.

        After each selection, select **Continue** to add a new event mapping.

    3.  Select the \[Record Page\] Refresh Action Bar handler.

    4.  Select **Add**.

    5.  Repeat for the Execution started event, using the same handler.

    ![The data drawer with the events and handlers shown](../image/add-grp-sow-events.png)

8.  Select **Save** to save your page with the new component.

9.  Add an icon component.

    The following steps add a sparkle icon to indicate that the form action uses agentic AI.

    1.  In the Content panel, find **Top Right** &gt; **Form record presence**, select the Configure icon ![](../image/three-dots-icon.png), then select **Add before**.

    2.  In the Icon dropdown, select an AI sparkle icon.

    3.  In the Size dropdown, select **Extra large**.

    4.  Select **Save** to save your page with the new component.

    ![The data drawer for the icon component](../image/add-grp-sow-icon.png)

10. Add the declarative action to the form.

    1.  From your instance homepage, navigate to **All** &gt; **Now Experience Framework** &gt; **Declarative Actions** &gt; **Form Actions**

    2.  In the Action label field, search `*generate resolution plan` and open the record.

    3.  Set **Active** to `true`.

    4.  Save or submit the record to make your changes.

    ![The Action Assignment record for the Generate resolution plan declarative action with active set to true](../image/add-grp-sow-form-action.png)


## Result

The **Generate Resolution Plan** button is enabled for users with the correct role in the Service Operation Workspace. When the button is selected, the AI agent execution processing messages appear in a section at the top of the record.

![SOW with Incident open and GRP button at the top](../image/add-grp-sow-result-button.png)

![SOW with Incident open and agentic workflow execution steps at the top](../image/add-grp-sow-result-card.png)

![Complete agentic workflow with review button highlighted and modal displayed](../image/add-grp-sow-complete.png)

