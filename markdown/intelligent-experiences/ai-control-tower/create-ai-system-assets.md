---
title: Create AI system assets
description: Create AI assets to track and manage the life cycles of your AI systems.
locale: en-US
release: australia
product: AI Control Tower
classification: ai-control-tower
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 7
keywords: [Now Assist, generative AI]
breadcrumb: [Creating AI assets, Use, AI Control Tower, Enable AI experiences]
---

# Create AI system assets

Create AI assets to track and manage the life cycles of your AI systems.

## Before you begin

Role required: sn\_ai\_governance\_ai\_steward or sn\_ai\_asset\_mgmt.ai\_asset\_owner

## About this task

An AI system is a software artifact that provides AI and machine learning \(ML\) capabilities to generate outputs, such as predictions, content, recommendations, and decisions, with varying levels of autonomy. Each AI system can be associated with one or more AI models, which may also be associated with one or more prompts and datasets. These AI models, prompts, and datasets enable the AI system to process data and solve complex problems with little to no human intervention.

## Procedure

1.  Navigate to **Workspaces** &gt; **AI Control Tower**.

2.  From the AI Control Tower, open the AI assets view.

3.  From the navigation menu of the AI assets view, navigate to either **AI asset inventory - Managed** &gt; **AI Systems** or **AI asset inventory - Unmanaged** &gt; **AI Systems**.

4.  Select **Add AI system**.

5.  In the Details section of the Add AI system form, fill in the fields.

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

Managed by

</td><td>

User who is assigned to manage the AI system. This field is automatically set to the user who creates the AI system asset.**Note:** This field is editable only if you have the AI steward \(sn\_ai\_governance\_ai\_steward\) role. If you have the AI asset owner \(sn\_ai\_asset\_mgmt.ai\_asset\_owner\) role, this field is read-only.

</td></tr><tr><td>

State

</td><td>

State of the AI system. The options are **Draft** and **Deployed**.

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
</table>6.  Select **Next**.

7.  In the Related assets section of the Add AI system form, associate the AI system with other AI assets that are related to it.

    1.  Depending on the type of related AI asset that you want associate the AI system with, select one of the following options from the asset type menu:

        -   To associate the AI system with any of its supported components or subsystems, select **Sub AI systems**.

            **Note:** This option is available only if you set the **Asset type** field to either **Agentic AI** or **Generative AI** in the Details section of the Add AI system form.

        -   To associate the AI system with any of its integrated AI models, select **AI models**.
        -   To associate the AI system with a dataset that is used to test an integrated AI model, select **Evaluation datasets**.
        -   To associate the AI system with a prompt that you are providing to an integrated AI model, select **Prompts**.
        -   To associate the AI system with any of its integrated AI tools, select **Tools**.

            **Note:** This option is available only if you set the **Asset type** field to **Agentic AI** in the Details section of the Add AI system form.

        The corresponding asset list opens.

    2.  Associate the AI system with the related AI asset.

        Depending on if the related AI asset is currently available in your asset inventory, proceed with one of the following options:

        -   To associate the AI system with a related AI asset that is currently available, use the following steps:

            1.  Select the Add from inventory drop-down menu on the header of the corresponding asset list.
            2.  Select **Add from inventory**.
            3.  In the Add from inventory dialog box, select the check box for the related AI asset that you want to associate the AI system with.

                **Note:** If you want to associate the AI system with multiple related AI assets, select the check box for each asset.

            4.  Select **Add**.
            The dialog box closes and the selected AI asset appears in the corresponding asset list.

        -   To associate the AI system with a related AI asset that is not currently available, use the following steps:

            **Note:** This option is not available for AI tools.

            1.  Select the Add from inventory drop-down menu on the header of the corresponding asset list.
            2.  Select **Create**.
            3.  Create the AI asset.
                -   If you are creating an AI system asset, return to [step 5](create-ai-system-assets.md#step5).
                -   If you are creating an AI model asset, follow the proceeding steps in [Create AI model assets](create-ai-model-assets.md).
                -   If you are creating a prompt asset, follow the proceeding steps in [Create prompt assets](create-prompt-assets.md).
                -   If you are creating a dataset asset, follow the proceeding steps in [Create dataset assets](create-dataset-assets.md).
            The new AI asset appears in the corresponding asset list.

8.  Select **Next**.

9.  In the Use &amp; purpose section of the Add AI system form, fill in the fields.

    This section of the Add AI system form enables you to specify the intended use and purpose of the AI system.

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
</table>    For more information on classifying AI systems based on regulatory risk at intake by applying a configured Risk Assessment Methodology \(RAM\), see Assessment templates and risk assessment methodologies and Request an AI use case.

10. Select **Submit for review**.

    **Note:** If you aren’t ready to submit the AI system for review, select **Save** instead. You can then edit it and submit it for review later by navigating to **AI assets** &gt; **Lifecycle** &gt; **Onboard** and then selecting the AI system from the list. When the AI asset record opens, continue editing the AI system details.


## Result

The AI system is added to your AI asset inventory. It automatically enters the onboard stage of the AI asset life cycle and is updated with a Lifecycle status of AI steward review.

## What to do next

Users who are assigned the AI steward \(sn\_ai\_governance.ai\_steward\) role can start the review process to begin tracking and managing the life cycle of the AI system. For detailed instructions, see [Complete AI asset lifecycle](complete-ai-asset-lifecycle.md).

**Parent Topic:**[Creating AI assets](../concept/creating-ai-assets.md)

