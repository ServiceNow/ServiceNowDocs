---
title: Configure a Guided Decision Playbook
description: Configure a Guided Decision Playbook to walk users through decision-driven questions and actions toward a recommended outcome, delivered as a seamless runtime experience that runs standalone or inside another playbook. The Guided Layout removes the activity and stage pickers and consolidates previous responses into an accordion.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/build-workflows/workflow-studio/configure-a-guided-decision-playbook.html
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2026-05-13"
reading_time_minutes: 6
breadcrumb: [Design Playbook Experience, Playbooks, Workflow Studio, Build workflows]
---

# Configure a Guided Decision Playbook

Configure a Guided Decision Playbook to walk users through decision-driven questions and actions toward a recommended outcome, delivered as a seamless runtime experience that runs standalone or inside another playbook. The Guided Layout removes the activity and stage pickers and consolidates previous responses into an accordion.

## Before you begin

Role required: playbook.admin, pd\_author, or playbook.write and ui\_builder\_admin or admin

## About this task

A Guided Decision Playbook uses the Guided Layout bundle to render embedded guided decisions and their supporting activities as one connected flow at runtime. Instead of agents navigating separately between a decision tree and the activities that follow each branch, the Guided Layout component sequences everything in a single experience — the agent answers a decision question, and the resulting activities for that branch appear immediately on the same page.

This workflow spans two interfaces. You build the playbook itself in Workflow Studio \(steps 1–4\), then design how it renders for end users in UI Builder \(steps 5–9\).

## Procedure

1.  Open Workflow Studio and create a playbook.

    1.  Navigate to **All** &gt; **Workflow Studio** &gt; **Playbooks**.

    2.  In the upper right corner, select **New** and select **Playbook** from the drop-down menu.

    3.  On the form, fill in the fields.

        |Field|Action|
        |-----|------|
        |Type|Select **Guided Decision**.|
        |Playbook name|Enter a unique, user-facing name for your playbook. This name appears to agents and fulfillers during runtime of your playbook.|
        |Description|Enter a short descriptive detail about your playbook.|
        |Application|Choose an application scope that you want your playbook to run in. Selecting **Global** lets your playbook run in any application scope. For more information, see [Application scope](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/building-applications/c_ApplicationScope.md).|
        |Execution type|Select **Standalone** if you want to make the Guided Decision Playbook nestable. You can't nest a record-driven playbook inside another playbook.|
        |Allow this playbook to be nestable in another playbook|Select this option to embed this playbook in another playbook.|

    The builder displays in **Diagram view** by default, but you can select **Board view** to switch views. Switch between views anytime as you build your playbook.

2.  Add activities to the stage to represent steps in your guided decision process.

    Guided Decision Playbooks are single-stage playbooks. A typical Guided Decision Playbook is composed of questionnaire activities to gather user input, decisions to branch based on responses, and guidance activities to deliver the recommended outcome at the end of each branch.

    For more information, see [Create a playbook variant](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/create-playbook-variant.md) and [Stages and activities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/process-automation-designer-lanes-activities.md).

3.  Add a decision from the mini-picker on the canvas to branch the flow based on the user's responses.

    A decision is what gives a Guided Decision Playbook its guided behavior. At runtime, the Guided Layout bundle renders the decision's branches and the activities that follow each branch as one seamless flow. Containing at least one decision is what distinguishes a Guided Decision Playbook from a standard playbook.

    \[Omitted image "playbook-add-decision.png"\] Alt text: Screenshot showing the mini-picker and the Add a decision option.

    For information on adding and configuring a Decision activity, see [Decision activities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/create-a-decision-activity.md).

4.  Activate the playbook from the playbook's header to publish it so that the Guided Layout bundle in UI Builder can find and render it.

    The bundle's playbook property only lists activated playbooks. If you change the playbook after activating, the system saves your changes but deactivates the playbook. Activate the playbook again to publish your changes.

    For information on activation states and what happens when you edit an activated playbook, see [Playbook statuses and activation states](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/process-status-activation-state.md).

5.  Go to UI Builder, and create or open an Experience to host the playbook so end users can access it from the Playbook Experience, and create a page.

    1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder** &gt; **Experiences**.

    2.  Select an existing Experience or create an Experience to work in.

    3.  Select the **+** icon next to **Pages** to create a page.

    4.  On the **Select a template** screen, select one:

        -   To use the Standard record template, select the **Standard record template** tile, then confirm by selecting **Use template**.
        -   To start with an empty page, select **Create from scratch instead**.
    Unlike the Focused and Stacked layouts, the Guided Layout does not have a matching page template.

    For information on creating a page, see [Create a page from scratch](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/ui-builder/create-page.md) and [create a page from a Standard record template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/ui-builder/reuse-page-definitions.md).

    **Note:** All playbooks require a parent table and sysId to be hardcoded on the controller or provided through a URL. You configure these in step 7 when you set up the test URL parameters for the page.

6.  Add the Guided Layout container to the page so the playbook renders as a guided experience at runtime.

    The bundle includes the controller and components needed to display the playbook. Adding the bundle wires them together automatically.

    \[Omitted image "playbook-guided-layout.png"\] Alt text: Screenshot showing the Guided Layout bundle.

    1.  Select **Add content** in the Content panel.

    2.  Select **Components**.

    3.  Select **Playbook** to bring up playbook layouts, and select the **Playbook Guided Layout** bundle.

    4.  Select **Add**.

    5.  Select either default or manual configuration for Guided Layout container.

        -   **Apply default configuration with added URL parameters**: Use this option when you want to launch the playbook from a URL that carries these values. The container reads the playbook's table, sysId, and other runtime values from the page's URL parameters. The page's URL will be modified to include the parameters. Existing links to the page may require an update.

        -   **Configure manually**: Use this option when you don't want the page's URL to carry runtime values, or when you have a specific configuration in mind.

    6.  Select **Done** to close the dialog and apply the configuration.

    For more information, see [Bind data to UI Builder pages using controllers \(advanced feature\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/ui-builder/controllers.md).

7.  Configure the Playbook Custom Layout Controller to tell the bundle which playbook to render at runtime.

    All playbooks require a parent table and sysId to be hardcoded on the controller or provided through a URL. The configuration depends on the execution type you selected in step 1.

<table id="choicetable_obq_nn3_jjc"><thead><tr><th align="left" id="d65894e534">

Type

</th><th align="left" id="d65894e537">

Action

</th></tr></thead><tbody><tr><td id="d65894e543">

**Standalone**

</td><td>

1.  On the canvas, select **Playbook Custom Layout Controller**.
2.  In the component configuration panel, select **Playbook to launch**.
3.  Select the activated playbook you want to render.


</td></tr><tr><td id="d65894e570">

**Record-driven**

</td><td>

1.  On the canvas, select **Playbook Custom Layout Controller**.
2.  In the component configuration panel, bind the parent table and record sysId to the page properties `props.table` and `props.record`.
3.  Bind the controller's sysId field to -1 to allow the system to recognize new playbook instances.
 **Note:**

The sysId=-1 binding is required for record-driven playbooks. Without it, the controller resets the record to negative 1 on every action and the playbook will never start.

</td></tr></tbody>
</table>    For more information, see [Bind data to UI Builder pages using controllers \(advanced feature\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/ui-builder/controllers.md).

    \[Omitted image "playbook-exp-binding.png"\] Alt text: Screenshot showing where to bind data to parent table.

8.  Preview the page in UI Builder to verify the playbook renders correctly at runtime.

    1.  Select **Preview**.

        The page opens in a new tab.

    2.  Step through the playbook by answering questions and following the decision branches to confirm each path renders the expected activities.

        The Guided Layout displays each activity as an accordion entry below the active one, with the current activity highlighted at the top of the page.

    3.  If the preview doesn't render as expected, return to the playbook in Workflow Studio to adjust the decisions or activities or review your configuration in UI Builder.

    **Note:** The Test feature in the Playbook Designer doesn't support the Guided Layout. To preview the runtime experience for a Guided Decision Playbook, you must use UI Builder Preview.

9.  Save and publish the page so end users can run the playbook from the Playbook Experience.

    1.  Select **Save**.

    2.  Select **Publish**.


## Result

End users see the playbook as a guided experience, moving through questions, decisions, and recommended outcomes one step at a time.

## What to do next

-   Run the Guided Decision Playbook end-to-end as an agent would to verify the runtime experience.
-   Adjust decisions, branches, or supporting activities in Workflow Studio based on feedback from end users.
-   Apply the Guided Layout pattern to other playbooks that benefit from decision-driven flows.
-   Configure access permissions so the right end users can run the playbook.

