---
title: Create a model to predict similar cases
description: Test and edit the pre-trained similar cases model for predicting similarity in customer service cases and create a new model for custom cases.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-10-21"
reading_time_minutes: 3
breadcrumb: [Configure Task Intelligence for Customer Service, Task Intelligence for Customer Service, Machine learning solutions for Customer Service Management, Implement Intelligence, Configuring Customer Service Management, Customer Service Management]
---

# Create a model to predict similar cases

Test and edit the pre-trained similar cases model for predicting similarity in customer service cases and create a new model for custom cases.

-   **Before you begin**

    Role required: ml\_admin, admin

-   **About this task**

    Base system models: Task Intelligence for Customer Service includes 3 base system models for predicting similar records for cases:

    -   Major Case identifier
    -   Similar Open Cases
    -   Similar Resolved Cases
    To get recommendations for major case identifier that includes propose major cases and similar major cases, install the [Major Issue Management plugin](https://servicenow.com/docs/bundle/xanadu-customer-service-management/page/product/customer-service-management/task/activate-major-issue-mgmt.html) and activate the feature as needed to get recommendations. When you install the Task Intelligence for CSM plugin in your production instance, the similar open cases, similar resolved cases, and major case identifier models are automatically installed and trained using your data. These models are then auto-deployed. The similar open case and similar resolved case models show predictions on recommended actions on case form. However, recommendations are not enabled for the major case identifier model in the base system.


## Steps to activate Major Case identifier recommendation

1.  Navigate to **All** &gt; **Recommended Actions** &gt; **Recommendations.**.
2.  Select **Propose major issue** under the Application scope **Task Intelligence for Customer Service**.
3.  Check the **Active** checkbox.

4.  Select **Update**.

    Repeat the steps for **Similar major cases**.


**Note:**

Propose major issue and similar major cases are inactive in the base system.

## Enable Suggested Actions on front line case page record

-   **Before you begin**

    Role required: workspace\_admin, ui\_builder\_admin, admin, next\_best\_action\_author

    Recommended Actions component should be added to the specific record page. \(Front line or CSM default record page\)

-   **About this task**

    To enable **Suggested Actions** tab, the admin should activate the **Recommended actions** feature on two specific pages: **Front line case page** and **CSM default record page**. Once activated, agents can view the recommendations on these pages.

    **Note:** For CSM default record page, first wire Recommended actions on this CSM default record page first, and then enable the **Suggested Actions** tab in UIB via the component property.


To enable **Suggested Actions** feature in the Recommended Actions component, follow the below steps:

1.  Navigate to **All**&gt; **Now Experience Framework** &gt;**Experiences**.
2.  Select the UX application **CSM/FSM Configurable Workspace**.
3.  Select **Open in UI Builder**.
4.  Navigate to **Record** under **Pages and variants**.
5.  Select **Front-line Case page**.

    **Note:** Ensure that you are in the right scope to be able to edit.

6.  Select **Recommended Actions 1** under Tabs.
7.  In the Configure tab, turn off the toggle for **Hide recommended actions**.
8.  Select **Save**.

By following these steps, you will successfully activate the Recommended Actions feature, allowing agents to view suggestions under Recommendations in the CSM/FSM Configurable Workspace. When you open a case, you will find the recommendations section with two tabs: **Search** and **Suggested Actions**. The recommendations are displayed under **Suggested Actions**.

## Enable Recommended actions in the CSM default record page

1.  Navigate to **All**.
2.  In the search box, enter sys\_ux\_screen\_condition.list and press Enter.
3.  Select the filter icon, enter **\[Screen\] \[contains\] \[Recommeded Actions default\]** and **\[Application\] \[is\] \[Recommeded Actions\]**, and select **Run**.
4.  Select the **true** link under **Active**.
5.  On the **UX Screen Condition** page in the Script, replace the return value with **true**.
6.  Select **Update**.

Result: When you open a case, you will find the recommendations section with two tabs: Search and Suggested Actions. The recommendations are displayed under Suggested Actions.

Find out how to [Create a custom similar case model](create-a-custom-similar-case-model.md), [Edit a model](../task/edit-a-case-prediction-model.md), and [Export a model](../task/export-a-task-intelligence-model.md)

