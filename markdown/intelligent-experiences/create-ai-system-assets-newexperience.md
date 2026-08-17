---
title: Create AI system assets
description: Create AI assets to track and manage the life cycles of your AI systems
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/create-ai-system-assets-newexperience.html
release: australia
topic_type: task
last_updated: "2026-04-09"
reading_time_minutes: 7
breadcrumb: [Creating AI assets manually, Managing your AI asset inventory, Discover and manage AI assets, AI Control Tower, Enable AI experiences]
---

# Create AI system assets

Create AI assets to track and manage the life cycles of your AI systems

## Before you begin

Role required: AI steward \[sn\_ai\_governance\_ai\_steward\] or AI asset owner \[sn\_ai\_asset\_mgmt.ai\_asset\_owner\]

**Note:** Users with the AI asset owner \[sn\_ai\_asset\_mgmt.ai\_asset\_owner\] role can only create AI assets and submit them for life-cycle review. They can't start or complete any life-cycle reviews.

## About this task

An AI system is a software artifact that provides AI and machine learning \(ML\) capabilities to generate outputs, such as predictions, content, recommendations, and decisions, with varying levels of autonomy. Each AI system can be associated with one or more AI models, which may also be associated with one or more prompts and datasets. These AI models, prompts, and datasets enable the AI system to process data and solve complex problems with little to no human intervention.

When you manually create an asset, the asset defaults to a **Design** state.

## Procedure

1.  Navigate to **All** &gt; **Al Control Tower** &gt; **Home** &gt; **Inventory**.

2.  On the Inventory page, select **Add AI asset**.

    The Add AI asset dialog box opens.

3.  In the dialog box, select **Enter asset details**.

4.  From the list of available asset types, select **AI system**.

    The dialog box closes and you're automatically redirected to the Add AI system asset form.

5.  In the Details section of the form, fill in the fields.

<table id="table_xhd_l25_bfc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the AI system.

</td></tr><tr><td>

Provider

</td><td>

People or organization that developed the AI system.

</td></tr><tr><td>

Version

</td><td>

Version of the AI system.

</td></tr><tr><td>

Description

</td><td>

Brief description of the AI system.

</td></tr><tr><td>

Documentation

</td><td>

Additional information about the AI system, such as the method used to evaluate the efficacy of the AI system.

</td></tr><tr><td>

Asset state

</td><td>

Current state of the AI system. Select one of the following options:-   **Design**
-   **Build**
-   **Available**
-   **Deployed**


</td></tr><tr><td>

Managed by

</td><td>

User who is assigned to manage the AI system. This field is automatically set to the user who creates the AI system asset.**Note:** This field is editable only if you have the AI steward \[sn\_ai\_governance\_ai\_steward\] role. If you have the AI asset owner \[sn\_ai\_asset\_mgmt.ai\_asset\_owner\] role, this field is read-only.

</td></tr><tr><td>

License details

</td><td>

License that you are using for the AI system.

</td></tr><tr><td>

Asset type

</td><td>

Type of AI that your AI system is. Select one of the following options:-   **Agentic AI**
-   **Classic AI**
-   **Generative AI**


</td></tr><tr><td>

Department

</td><td>

Department that the AI system belongs to.

</td></tr><tr><td>

Supported locations

</td><td>

Locations in which the AI system is supported.

</td></tr></tbody>
</table>6.  Select **Next** to move to the next section of the form.

    You can also select **Save draft** to save the details in the form or select **Cancel** that provides you with the following options:

    -   **Keep editing**: to continue editing the form.
    -   **Save draft and exit**: saves the form and you exit the form.
    -   **Discard and exit**: your unsaved changes are discarded and you exit the form.
7.  In the Relationships section of the Add AI system asset form, associate the AI system with other AI assets that are related to it.

    1.  Depending on the type of related AI asset that you want associate the AI system with, select one of the following options from the asset type menu:

        -   To associate the AI system with any of its supported components or subsystems, select **Sub AI systems**.

            **Note:** This option is available only if you set the **Asset type** field to either **Agentic AI** or **Generative AI** in the Details section of the Add AI system form.

        -   To associate the AI system with any of its integrated AI models, select **AI models**.
        -   To associate the AI system with a dataset that is used to test an integrated AI model, select **Evaluation datasets**.
        -   To associate the AI system with a prompt that you are providing to an integrated AI model, select **Prompts**.
        -   To associate the AI system with any of its integrated AI tools, select **Tools**.

            **Note:** This option is available only if you set the **Asset type** field to **Agentic AI** in the Details section of the Add AI system form.

        -   To associate the AI system with a business application, select **Business applications**.
        -   To associate the AI system with a configuration item \(CI\), select **Configuration items**
        The corresponding asset list opens.

    2.  Associate the AI system with a related AI asset.

        1.  Select **Add from inventory**.
        2.  In the dialog box, select the check box for the related AI asset that you want to associate the AI system with.

            **Note:** If you want to associate the AI system with multiple related AI assets, select the check box for each asset.

        3.  Select **Add**.
8.  Select **Next**.

9.  In the Use &amp; purpose section of the form, fill in the fields.

    This section enables you to specify the intended use and purpose of the AI system.

<table id="table_a3v_q3r_g3c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Intended outcome of the AI system

</td><td>

Primary business outcome that the AI system is expected to achieve. Select one of the following options:-   **Not Applicable**
-   **Efficiency Boost**
-   **Quality Enhancement**
-   **Decision Guidance**
-   **Automation of Tasks**
-   **Customer Experience Upgrade**
-   **Insight Generation**


</td></tr><tr><td>

Interaction type with end users

</td><td>

Type of interaction between end users and the AI system, including whether outputs are visible, actionable, or interactive. Select one of the following options:-   **Not Applicable**
-   **No Direct Interaction**
-   **Background Support**
-   **Notifications &amp; Prompts**
-   **User-Facing Recommendations**
-   **Chat-Based Interaction**
-   **Interactive Experience**


</td></tr><tr><td>

Level of human involvement

</td><td>

Capacity at which users can guide, review, and accept AI system activities during operation. Select one of the following options:-   **Not Applicable**
-   **Full User Control**
-   **User-Guided with AI Support**
-   **Shared Control**
-   **AI-Initiated with User Approval**
-   **Full Automated Workflow**


</td></tr><tr><td>

System autonomy level

</td><td>

Extent to which the AI system can initiate actions or decisions without human intervention. Select one of the following options:-   **None**
-   **Assistive \(AI suggests\)**
-   **Semi-Automated \(acts with confirmation\)**
-   **Condition-Based Automation**
-   **Event-Triggered Automation**
-   **Fully Automated Execution**


</td></tr><tr><td>

Type of output produced

</td><td>

Type of output that the AI system produces for users, systems, or downstream processes. Select any of the following options:-   **Automated Decisions**
-   **Generated Content**
-   **Insight &amp; Summaries**
-   **Ranking &amp; Scores**
-   **Recommendations**
-   **Simple Alerts**
-   **System Actions**


</td></tr><tr><td>

Area where the AI system is used

</td><td>

Business or operational areas where the AI system is used or provides value. Select any of the following options:-   **Customer services**
-   **External Partner Ecosystem**
-   **Finance &amp; Accounting**
-   **HR &amp; Workforce**
-   **Internal Operations**
-   **IT &amp; Security**
-   **Sales &amp; Marketing**
-   **Supply Chain**


</td></tr><tr><td>

People affected by the AI system

</td><td>

Users who may be directly or indirectly affected by the AI system outputs or decisions. Select any of the following options:-   **External Partners**
-   **General Customer Base**
-   **Internal Team**
-   **Public or Large Audiences**
-   **Specific Customer Groups**


</td></tr><tr><td>

Data used by the system

</td><td>

Types of data that the AI system uses to process inputs and generate outputs. Select any of the following options:-   **Behavioral or Usage Data**
-   **Business Operational Data**
-   **Customer Interaction Data**
-   **Profile or Account Data**
-   **Public or General Info**
-   **Sensitive Business Data**


</td></tr><tr><td>

Additional use and purpose details

</td><td>

Additional information or context that helps clarify the specific use and purpose of the AI system.

</td></tr></tbody>
</table>    For more information on classifying AI systems based on regulatory risk at intake by applying a configured Risk Assessment Methodology \(RAM\), see [Request an AI use case](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/request-ai-system.md).

10. Select **Submit for review**.

    The Asset record page opens and your asset is in an unmanaged state. You can edit details related to your asset on the **Details** tab by using the pencil icon in the sections titled **About this asset** and **Use and purpose**.

11. If you have the AI steward \[sn\_ai\_governance\_ai\_steward\] role, select the **Actions** menu and then select **Start lifecycle review**.

    **Important:** Only users with the AI steward \[sn\_ai\_governance\_ai\_steward\] role can start the life-cycle review.

    The Start AI steward review dialog box opens.

12. In the **Managed by** field of the dialog box, search for and select the user that you want to assign the life-cycle review to.

    **Important:** You must select a user with the AI steward \[sn\_ai\_governance\_ai\_steward\] role.

13. Select **Start review**.

    The asset automatically changes from an unmanaged asset to a managed asset and starts the onboarding workflow. The Lifecycle tab now contains three sub tabs: **Onboard**, **Maintain**, and **Retire**. The **Maintain**, and **Retire** are disabled and are enabled once onboarding is complete.

    The **Onboard** sub tab contains the Onboarding playbook with tasks displayed. If tasks are not already present in the Onboarding playbook, users with the AI steward \[sn\_ai\_governance\_ai\_steward\] role can create tasks by selecting **New** and assign them to other AI stewards.

14. If you're assigned to the life-cycle review, select **Mark complete** to complete each activity in the onboarding playbook.

    If your tasks are open and you select **Mark complete**, those tasks automatically get closed with the **Closed skipped** state and you move to the next stage of onboarding. Once you move forward, you can no longer create tasks in the previous stage.

    You can select the **Actions** menu and select **Reject request** to cancel the onboarding playbook and mark this asset as unmanaged.

    When all stages in the onboarding playbook are marked as complete, the playbook status updates to **Complete**. The **Maintain** and **Retire** tabs show a status of **Not Started**.

    **Note:** The end-to-end onboarding process from start to finish may take a few days.


