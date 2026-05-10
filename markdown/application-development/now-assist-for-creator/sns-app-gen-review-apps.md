---
title: Review and edit applications built using app generation
description: After app generation creates an application, review and modify it in ServiceNow Studio to verify accuracy and extend functionality.
locale: en-US
release: australia
product: Now Assist for Creator
classification: now-assist-for-creator
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
keywords: [agentic ai, app gen, app generation, now assist, application generation, app creation, application creation, servicenow studio, generative ai]
breadcrumb: [Generate apps, App generation, Use generative AI, Now Assist for Creator, Vibe coding and AI app development on the ServiceNow AI Platform, Building applications]
---

# Review and edit applications built using app generation

After app generation creates an application, review and modify it in ServiceNow Studio to verify accuracy and extend functionality.

This video shows you how to review apps created using app generation in ServiceNow Studio.

Review applications generated using app generation in ServiceNow Studio. 

## Before you begin

You must have an existing application that you created or have access to edit. The application does not need to have been created using generative AI to use the app generation skill to edit it.

Role required: now\_assist\_panel\_user

**Note:** To edit \(not create\) apps, assign users the delegated\_developer or now\_assist\_panel\_user role.

## Procedure

1.  Navigate to **App Engine** &gt; **ServiceNow Studio**.

    To learn more about the ServiceNow Studio home page, see [ServiceNow Studio](../../servicenow-studio/concept/servicenow-studio-landing.md).

2.  Select the Now Assist icon.

    ![Now Assist highlighted in banner.](../images/app-generation-task-initiation-xsr2.png)

3.  In the Now Assist panel, select **Update an app**.

    ![Now Assist panel with update an app button highlighted.](../images/app-generation-task-update-app.png)

4.  Select the app to edit.

    The apps available for editing in the Now Assist panel are custom applications you have created or to which you have access. If the application list is long, use the search box to find a specific application.

    If you have the delegated\_developer or now\_assist\_panel\_user roles but do not see the app you need, contact your App Engine admin. Ask the admin to add you to the app as a delegated developer. For more information, see [Delegated development and deployment](../../applications/concept/c_DelegatedDevelopment.md).

    To edit an application with the app generation skill, your scope must match the app scope. If your scope does not match, the app generation skill changes your scope to the app scope automatically.

5.  Select **Submit**.

6.  Describe your changes to Now Assist.

    For example:

    -   Specify additional business requirements that the application must support.
    -   Request a new table extended from an existing table.
    -   Request an additional role or roles.
    -   Add a workspace.
    -   Add a flow.
    -   Add columns to an existing table.
    **Note:** Now Assist might encounter issues while updating a very large app. Consider updating the app manually in ServiceNow Studio instead.

7.  Preview the application and continue making changes.

    If you asked Now Assist to create a workspace or flow, the workspace or flow is generated after saving the application.

8.  Select **Save and open app**.

9.  In the **Application Files** tab, open, verify, and modify items as needed.

    The following optional steps provide details about how to check some common files.

10. Review the generated tables.

    1.  On the **Application Files** tab, in the **Display name** column, select an existing table in your application.

        The table record opens in a new tab in **Table Builder**.

        **Note:** If the Now Assist panel is covering information, select the Now Assist icon ![](../../app-engine-studio/image/now-assist-sparkle-icon-dark.png) to close the panel. Select the icon again to reopen the panel and continue the conversation.

        ![ServiceNow Studio tab showing table details.](../images/app-generation-review-table-x2.png)

    2.  Confirm that the table is accurate and captures the correct data.

    3.  Make any changes, such as the following:

        -   Update table fields.
        -   Edit the table and field column properties.
        -   Verify that the generated choices are implemented correctly.
        -   Add a column.
    4.  Close the table tab.

11. Review the generated access control lists \(ACLs\).

    1.  On the **Application Files** tab, in the **Display name** column, select an existing access control in your application.

        The ACL record opens in a new tab.

        ![ServiceNow Studio tab showing access control details.](../images/app-generation-review-acl-xsr2.png)

    2.  Verify that the created ACL is accurate and requires the correct role or roles.

    3.  Close the access control tab.

12. Review the generated roles.

    1.  On the **Application Files** tab, in the **Display name** column, select an existing role in your application.

        The role record opens in a new tab.

        ![ServiceNow Studio tab showing role details.](../images/app-generation-review-role-xsr2.png)

    2.  Verify that the created role and its assigned permissions accurately represent the users of your application.

    3.  Close the role tab.

13. Review the generated record producers.

    1.  On the **Application Files** tab, in the **Display name** column, select an existing record producer in your application.

        The record producer record opens in a new tab.

    2.  Review and modify the record producer if necessary.

        For example, select **Questions**, hover over a specific question, and select the Edit icon. Confirm that the question type and options are correct. Make any changes as needed.

        For more information about record producers, see [Record Producer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-catalog/c_RecordProducer.md).

    3.  Close the record producer tab.

14. Review a generated workspace.

    1.  On the **Application Files** tab, in the **Display name** column, select the entry with a **Class** of **UX Application**.

        ![Application Files tab with workspace UX application entry highlighted.](../images/app-generation-review-workspace1.png)

        The workspace opens in UI Builder in a new tab.

    2.  On the UI Builder tab, select **Home** to preview the workspace landing page.

        ![UI Builder workspace experience page with home page highlighted.](../images/app-generation-review-workspace2.png)

    3.  Review the workspace and, after confirming that you're in the correct application scope, modify the workspace if necessary.

        For example, add additional column layouts containing more charts and graphs.

        To see the workspace from an end-user perspective, select **Preview**.

        For more information about UI Builder, see [UI Builder](../../../administer/ui-builder/concept/ui-builder-overview.md).

    4.  Close the UI Builder tab.

15. Review a generated flow.

    1.  On the **Application Files** tab, in the **Display name** column, select the flow entry with a **Class** of **Flow**.

        ![Application Files tab with flow entry highlighted.](../images/app-generation-review-flow1.png)

        The flow opens in Workflow Studio in a new tab.

        ![Workflow Studio tab with flow triggers and actions displayed.](../images/app-generation-review-flow2.png)

    2.  Review the flow and modify it if necessary.

        For example, add or change triggers, actions, or subflows.

        For more information about using Workflow Studio, see [Exploring flows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/exploring-flows.md).

    3.  Close the Workflow Studio tab.


## What to do next

Continue opening, verifying, and modifying items in the application files list as needed. For more information, see [ServiceNow Studio](../../servicenow-studio/concept/servicenow-studio-landing.md).

**Parent Topic:**[Generate apps in ServiceNow Studio](sns-app-gen-using-landing.md)

