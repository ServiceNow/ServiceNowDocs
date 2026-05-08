---
title: Accept or dismiss recommendations for regulatory alert impacted policies
description: Accept AI-generated recommendations in Regulatory Change Management to mark specific business areas as impacted so that you can help compliance practitioners capture and address the relevant regulatory alert for policies. You can also dismiss recommendations to filter out irrelevant or unnecessary information.
locale: en-US
release: australia
product: GRC Common Functions
classification: grc-common-functions
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 6
keywords: [generative AI, GenAI, Now Assist, ServiceNow AI Platform]
breadcrumb: [Generate recommendations for regulatory alert impacted areas, Use generative AI skills, Now Assist, Common GRC features, Governance, Risk, and Compliance]
---

# Accept or dismiss recommendations for regulatory alert impacted policies

Accept AI-generated recommendations in Regulatory Change Management to mark specific business areas as impacted so that you can help compliance practitioners capture and address the relevant regulatory alert for policies. You can also dismiss recommendations to filter out irrelevant or unnecessary information.

## Before you begin

**Important:** This Now Assist skill is turned on by default. The skill will be automatically available to appropriate role users for the application. For more information, see Now Assist skills, agents, and agentic workflows on by default.

Role required: To view your assigned regulatory alerts, you need the sn\_grc\_reg\_change.user and sn\_grc\_comp\_genai.reg\_change\_ai\_user roles.

**Important:** Be sure to check AI-generated recommendations for accuracy. If no information is available, the generated recommendations display "No recommendations available," "None," "No records to display," and so on.

To learn about the related roles and regulatory alerts for a recommendation, see [Types of alerts, user roles, and states of regulatory alerts](../../grc-rcm/reference/user_roles_and_actions.md).

## About this task

The Recommendation Framework enables dynamic, AI-driven policy recommendations by evaluating regulatory alert content against configurable policy associations. This helps to enhance impact analysis and improve compliance accuracy. When a regulatory alert is issued, the system generates relevant policy suggestions. After reviewing each recommendation, compliance analysts can accept applicable policies to mark the corresponding business areas as impacted. For example, a regulatory alert related to Digital Operational Resilience Act \(DORA\) can prompt recommendations for policies such as Vendor Onboarding Procedures and Incident Response Protocols. After a compliance analyst reviews and accepts these policies, they can mark the relevant business areas as impacted and take steps to help ensure regulatory compliance while managing regulatory tasks.

You can view the related activity for each recommendation by selecting the summary icon ![](../../grc-rcm/image/summary-icon.png) to open the Feedback trail side-panel.

## Procedure

1.  Navigate to one of the following locations:

    -   **Workspaces** &gt; **Compliance Workspace**, select the list icon ![](../../grc-cam-workspace/image/ws-list-icon.png) and then navigate to **Regulatory alerts**.
    -   **Workspaces** &gt; **Compliance Workspace** and select the Regulatory Change Management dashboard icon ![](../../grc-rcm/image/reg-change-icon.png) and then in the Activity overview, Tracking, or Trends section, select any segment or value in an Alerts related widget to open the list of regulatory alerts with that state.
2.  Select the regulatory alert that you want and review the recommendations by selecting the **Recommendations** tab.

    **Note:** If recommendations haven’t already been generated, you can generate recommendations for a regulatory alert in any state except Closed or Cancelled by completing one of the following.

    -   On the **Overview** tab, select **Recommend**.
    -   On the **Recommendations** tab, select **Show recommendations**.
    For more information, see [Generate recommendations for regulatory alert impacted citations, control objectives, controls, and policies](create-recommendation-reg-alert.md).

3.  Review potential impact areas by selecting the **Policies** tab in the Recommended areas of the impact section.

    The recommended policies only include policies that are part of the existing inventory.

    ![Details of the recommended policy.](../../grc-rcm/image/reco-policy-details.png)

    **Note:** The `Suggest business operations affected by regulatory alert recommendation context` provides the recommendations that you see here. For more information, see [Recommendation contexts and templates](../../grc-rcm/concept/recommendation-contexts.md).

    If recommendations are available, you can scroll through the generated list of policies recommendation cards and review the information about each policy, such as its name and compliance status.

4.  Select the policies recommendation card that you want and review the following sections:

<table id="id_o2v_k4c_cfc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the policy.

</td></tr><tr><td>

Type

</td><td>

Type of policy.

</td></tr><tr><td>

Owner

</td><td>

Owner of the policy.

</td></tr><tr><td>

Policy categories

</td><td>

Categories that classify the policy based on its purpose, scope, or regulatory domain.

</td></tr><tr><td>

Compliance score

</td><td>

A numerical or qualitative score that reflects how well the policy aligns with regulatory requirements or internal standards.

</td></tr><tr><td>

Description

</td><td>

Description and summary of the policy.

</td></tr><tr><td>

Policy text

</td><td>

Additional guidance on how to address the policy.

</td></tr><tr><td class="sub-head" colspan="2">

**Evaluate affected associations for policies**

</td></tr><tr><td>

Control objectives

</td><td>

Related goal or requirement that can be associated with the policy.For each control objective, the following information is provided if available.

-   Reference
-   Name of the control objective
-   Category that the control objective is associated with
-   Classification for the control objective


</td></tr><tr><td>

Policies

</td><td>

Related policies that can be associated with the policy.For each policy, the following information is provided if available.

-   Number assigned to the policy
-   Name of the policy
-   Type of policy
-   State of the policy


</td></tr><tr><td>

Policy Exceptions

</td><td>

Related goal or requirement that can be associated with the policy.For each control objective, the following information is provided if available.

-   Number assigned to the policy exception
-   Name of the policy
-   Name of the control objective
-   Name of issue


</td></tr></tbody>
</table>    For full descriptions of these fields, see [Create a control objective](../../grc-policy-and-compliance/task/t_CreateAPolicyStatement.md), [Create a policy](../../grc-policy-and-compliance/task/t_DefineAPolicy.md), and [Create a control](../../grc-policy-and-compliance/task/t_CreateAControl.md).

5.  To associate control objectives or risks with your recommendation, navigate to the corresponding tab and select the check box for each record that you want to include as part of the impacted areas.

    Each selected risk will be added as an impacted area after you accept the recommendation.

    **Note:** The policy you’re reviewing may not have any risks associated with it. Control objectives or risks must be mapped to policies in the inventory for them to appear.

    ![Details of the affected associations for policies.](../../grc-rcm/image/reco-policy-associations.png)

6.  View the record for a policy, refresh your recommendations, or review related activity for each recommendation.

    |Option|Description|
    |------|-----------|
    |**Select the details icon ![](../../grc-privacy-management/image/details-icon.jpg).**|View the record for a policy.|
    |**Select the refresh icon ![](../../grc-risk/image/refresh-icon.jpg).**|Refresh the recommendations to reflect the latest data.|
    |**Select the summary icon ![](../../grc-rcm/image/summary-icon.png).**|Open the Feedback trail side-panel to review the related activity for the recommendation.|

7.  Accept or dismiss the recommendations and their associations.

    -   Select **Accept** and then **Confirm** to accept a recommendation as an impacted area.
    -   Select **Dismiss** and then **Confirm** to avoid a recommendation from being shown again.
    Before you act on a recommendation, you see a summary of the impact areas and associations that you’re accepting or dismissing.

    If you accept the recommendation, it’s marked as an impacted area and is added to the list of impacts. If you dismiss the recommendation, it’s marked as dismissed and isn't shown again for that specific regulatory alert.


## What to do next

If you accepted any recommendations, confirm the creation of an impacted area by navigating to the **Impacted areas** tab. If you dismissed all recommendations or must add more impacted areas, you can manually add impacted areas. For more information, see [Add impacted areas manually to a regulatory alert](add-impacted-area-reg-alert.md).

