---
title: Accept or dismiss recommendations for regulatory alert impacted control objectives
description: Accept recommendations to mark specific business areas as impacted, helping compliance practitioners capture and address relevant regulatory alerts for control objectives. Dismiss recommendations to filter out irrelevant or unnecessary information.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/governance-risk-compliance/grc-common-functions/manage-recommend-co-reg-alert.html
release: zurich
product: GRC Common Functions
classification: grc-common-functions
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 5
keywords: [Now Assist, generative AI]
breadcrumb: [Generate recommendations for regulatory alert impacted areas, Use generative AI skills, Now Assist, Common GRC features, Governance, Risk, and Compliance]
---

# Accept or dismiss recommendations for regulatory alert impacted control objectives

Accept recommendations to mark specific business areas as impacted, helping compliance practitioners capture and address relevant regulatory alerts for control objectives. Dismiss recommendations to filter out irrelevant or unnecessary information.

## Before you begin

**Important:** This Now Assist skill is turned on by default. The skill will be automatically available to appropriate role users for the application. For more information, see .

Role required: To view your assigned regulatory alerts, you need the sn\_grc\_reg\_change.user and sn\_grc\_comp\_genai.reg\_change\_ai\_user roles.

For more information on related roles and regulatory alerts, see [Types of alerts, user roles, and states of regulatory alerts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/regulatory-change-management-service-portal/user_roles_and_actions.md).

**Important:** Be sure to check AI-generated recommendations for accuracy. If no information is available, the generated recommendations display "No recommendations available", “None", "No records to display", and so on.

## Procedure

1.  Navigate to one of the following locations:

    -   **Workspaces** &gt; **Compliance Workspace**, select the list icon \[Omitted image "ws-list-icon.png"\] Alt text: and then navigate to **Regulatory alerts**.
    -   **Workspaces** &gt; **Compliance Workspace** select the Regulatory Change Management dashboard icon \[Omitted image "reg-change-icon.png"\] Alt text: and then in the Activity overview, Tracking, or Trends section, select any segment or value in an Alerts related widget to open the list of regulatory alerts with that state.
2.  Select the regulatory alert that you want and review the recommendations by selecting the Recommendations tab.

    **Note:** If recommendations haven’t already been generated, you can generate recommendations for a regulatory alert in any state except Closed or Cancelled by completing one of the following.

    -   On the Overview tab, select **Recommend**.
    -   On the Recommendations tab, select **Show recommendations**.
    For more information, see [Generate recommendations for regulatory alert impacted citations, control objectives, controls, and policies](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/grc-common-functions/create-recommendation-reg-alert.md).

3.  Review potential impact areas by selecting the Control objectives tab in the Recommended areas of the impact section.

    The recommended control objectives only include control objectives that are part of the existing inventory.

    \[Omitted image "reco-co-details.png"\] Alt text: Details of the recommended control objective.

    **Note:** The `Suggest business operations affected by regulatory alert recommendation context` provides the recommendations that you see here. For more information, see [Recommendation contexts and templates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/grc-common-functions/recommendation-contexts.md).

    If recommendations are available, you can scroll through the generated list of control objectives recommendation cards and review the information about each control, such as its name and compliance status.

4.  Select the control objectives recommendation card that you want and review the following sections:

<table id="id_o2v_k4c_cfc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the control objective.

</td></tr><tr><td>

Category

</td><td>

Business or technical domain for the control objective.

</td></tr><tr><td>

Classification

</td><td>

Functional intent of the control objective.

</td></tr><tr><td>

Type

</td><td>

Operational nature or domain of the control objective.

</td></tr><tr><td>

Description

</td><td>

Description and summary of the control objective.

</td></tr><tr><td>

Supplemental Guidance

</td><td>

Additional guidance on how to address the control objective.

</td></tr><tr><td class="sub-head" colspan="2">

**Evaluate Affected Associations**

</td></tr><tr><td>

Child Control Objectives

</td><td>

Specific goal or requirement that is tied to this recommended parent control objective.For each child control objective, the following information is provided if available.

-   Reference
-   Name of the control objective
-   Category that the control objective is associated with
-   Classification for the control objective


</td></tr><tr><td>

Policies

</td><td>

Related policies that can be associated with the control objective.For each policy, the following information is provided if available.

-   Number assigned to the policy
-   Name of the policy
-   Type of policy
-   State of the policy


</td></tr><tr><td>

Controls

</td><td>

Related controls that can be associated with the control objective.For each control, the following information is provided if available.

-   Name of the control
-   Number assigned to the control
-   Entity that the control is associated with
-   Function of the control


</td></tr><tr><td>

Risk Statements

</td><td>

Related risk statements that can be associated with the control objective.For each risk statement, the following information is provided if available.

-   Name of the risk statement
-   Framework that the risk is associated with
-   Risk statement category
-   Description of the risk statement.


</td></tr></tbody>
</table>    For full descriptions of these fields, see [Create a control objective](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/policy-and-compliance-management/t_CreateAPolicyStatement.md), [Create a policy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/policy-and-compliance-management/t_DefineAPolicy.md), [Create a control](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/policy-and-compliance-management/t_CreateAControl.md), and [Create a risk manually](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/grc-risk-management-workspace/t_CreateRisk.md).

5.  To associate child control objectives, policies, controls, or risk statements with your recommendation, navigate to the corresponding tab and select the check box for each record you want to include as part of the impacted areas.

    Each selected record will be added as an impacted area after you accept the recommendation.

    **Note:** The control objective that you’re reviewing may not have anything associated with it. Child control objectives, policies, controls, or risk statements must be mapped to control objectives in the inventory for them to appear.

    \[Omitted image "reco-co-associations.png"\] Alt text: Details of the affected associations for control objectives.

6.  View the record for a control objective, refresh your recommendations, or review related activity for each recommendation.

    |Option|Description|
    |------|-----------|
    |**Select the details icon \[Omitted image "details-icon.jpg"\] Alt text:.**|View the record for a control objective.|
    |**Select the refresh icon \[Omitted image "refresh-icon.jpg"\] Alt text:.**|Refresh the recommendations to reflect the latest data.|
    |**Select the summary icon \[Omitted image "summary-icon.png"\] Alt text:.**|Open the Feedback trail side-panel to review the related activity for the recommendation.|

7.  Accept or dismiss the recommendations and their associations.

    -   Select **Accept** and then **Confirm** to accept a recommendation as an impacted area.
    -   Select **Dismiss** and then **Confirm** to avoid a recommendation from being shown again.
    Before you act on a recommendation, you see a summary of the impact areas and associations that you’re accepting or dismissing.

    If you accept the recommendation, it’s marked as an impacted area and is added to the list of impacts. If you dismiss the recommendation, it’s marked as dismissed and isn't shown again for that specific regulatory alert.


## What to do next

If you accepted any recommendations, confirm the creation of an impacted area by navigating to the Impacted areas tab. If you dismissed all recommendations or must add more impacted areas, you can manually add impacted areas. For more information, see [Add impacted areas manually to a regulatory alert](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/grc-common-functions/add-impacted-area-reg-alert.md).

