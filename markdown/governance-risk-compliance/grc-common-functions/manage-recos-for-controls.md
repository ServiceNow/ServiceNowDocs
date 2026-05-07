---
title: Accept or dismiss recommendations for regulatory alert impacted controls
description: Accept AI-generated recommendations in Regulatory Change Management to mark specific business areas as impacted so that you can help compliance practitioners capture and address the relevant regulatory alert for controls. You can also dismiss recommendations to filter out irrelevant or unnecessary information.
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

# Accept or dismiss recommendations for regulatory alert impacted controls

Accept AI-generated recommendations in Regulatory Change Management to mark specific business areas as impacted so that you can help compliance practitioners capture and address the relevant regulatory alert for controls. You can also dismiss recommendations to filter out irrelevant or unnecessary information.

## Before you begin

**Important:** This Now Assist skill is turned on by default. The skill will be automatically available to appropriate role users for the application. For more information, see [Now Assist skills, agents, and agentic workflows on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

Role required: To view your assigned regulatory alerts, you need the sn\_grc\_reg\_change.user and sn\_grc\_comp\_genai.reg\_change\_ai\_user roles.

**Important:** Be sure to check AI-generated recommendations for accuracy. If no information is available, the generated recommendations display "No recommendations available," "None," "No records to display," and so on.

To learn about the related roles and regulatory alerts for a recommendation, see [Types of alerts, user roles, and states of regulatory alerts](../../grc-rcm/reference/user_roles_and_actions.md).

## About this task

The Recommendation Framework enables dynamic, AI-driven control recommendations by evaluating regulatory alert content against configurable control associations. This enhances impact analysis and improves compliance accuracy. When a regulatory alert is issued, the system generates relevant control suggestions. After reviewing each recommendation, compliance analysts can accept applicable controls to mark the corresponding business areas as impacted. For example, a regulatory alert related to Digital Operational Resilience Act \(DORA\) can prompt recommendations for controls such as Vendor Onboarding Procedures and Incident Response Protocols. After a compliance analyst reviews and accepts these controls, they can mark the relevant business areas as impacted and take steps to help ensure regulatory compliance while managing regulatory tasks.

You can view the related activity for each recommendation by selecting the summary icon ![](../../grc-rcm/image/summary-icon.png) to open the Feedback trail side-panel.

## Procedure

1.  Navigate to one of the following locations:

    -   **Workspaces** &gt; **Compliance Workspace**, select the list icon ![](../../grc-cam-workspace/image/ws-list-icon.png) and then navigate to **Regulatory alerts**.
    -   **Workspaces** &gt; **Compliance Workspace** select the Regulatory Change Management dashboard icon ![](../../grc-rcm/image/reg-change-icon.png) and then in the Activity overview, Tracking, or Trends section, select any segment or value in an Alerts related widget to open the list of regulatory alerts with that state.
2.  Select the regulatory alert that you want and review the recommendations by selecting the Recommendations tab.

    **Note:** If recommendations haven’t already been generated, you can generate recommendations for a regulatory alert in any state except Closed or Cancelled by completing one of the following.

    -   On the Overview tab, select **Recommend**.
    -   On the Recommendations tab, select **Show recommendations**.
    For more information, see [Generate recommendations for regulatory alert impacted citations, control objectives, controls, and policies](create-recommendation-reg-alert.md).

3.  Review potential impact areas by selecting the Controls tab in the Recommended areas of the impact section.

    The recommended controls only include controls that are part of the existing inventory.

    ![Details of the recommended control.](../../grc-rcm/image/reco-control-details.png)

    **Note:** The `Suggest business operations affected by regulatory alert recommendation context` provides the recommendations that you see here. For more information, see [Recommendation contexts and templates](../../grc-rcm/concept/recommendation-contexts.md).

    If recommendations are available, you can scroll through the generated list of control recommendation cards and review the information about each control, such as its name and compliance status.

4.  Select the control recommendation card that you want and review the following sections:

<table id="id_o2v_k4c_cfc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the control.

</td></tr><tr><td>

Status

</td><td>

Status of the control: If it’s Compliant, Non Compliant, or Not Applicable.

</td></tr><tr><td>

Function

</td><td>

Operational role of the control. For example, Standard control or Common control.

</td></tr><tr><td>

Owner

</td><td>

Owner of the control.

</td></tr><tr><td>

Entity

</td><td>

Entity associated with the control.

</td></tr><tr><td>

Category

</td><td>

Domain or grouping to which the control belongs to.

</td></tr><tr><td>

Type

</td><td>

Type of control.Specifies whether the control is Manual, Automated, or Continuous.

</td></tr><tr><td>

Description

</td><td>

Description and summary of the control.

</td></tr><tr><td>

Additional Information

</td><td>

Additional information related to the control.

</td></tr><tr><td class="sub-head" colspan="2">

**Evaluate affected associations for controls**

</td></tr><tr><td>

Risks

</td><td>

Related risks that can be associated with the control.For each risk, the following information is provided if available.

-   Name of the risk
-   Entity that the risk is associated with
-   Risk statement from which the risk is inherited
-   Risk statement


</td></tr></tbody>
</table>    For full descriptions of these fields, see [Create a control objective](../../grc-policy-and-compliance/task/t_CreateAPolicyStatement.md), [Create a policy](../../grc-policy-and-compliance/task/t_DefineAPolicy.md), [Create a control](../../grc-policy-and-compliance/task/t_CreateAControl.md), and [Create a risk manually](../../grc-risk/task/t_CreateRisk.md).

5.  To associate risks with your recommendation, navigate to the Risks tab and select the check box for each risk record you want to include as part of the impacted areas.

    Each selected risk will be added as an impacted area after you accept the recommendation.

    **Note:** The control you’re reviewing may not have any risks associated with it. Risks must be mapped to controls in the inventory for them to appear.

    ![Details of the affected associations for controls.](../../grc-rcm/image/reco-control-associations.png)

6.  View the record for a control, refresh your recommendations, or review related activity for each recommendation.

    |Option|Description|
    |------|-----------|
    |**Select the details icon ![](../../grc-privacy-management/image/details-icon.jpg).**|View the record for a control.|
    |**Select the refresh icon ![](../../grc-risk/image/refresh-icon.jpg).**|Refresh the recommendations to reflect the latest data.|
    |**Select the summary icon \(![](../../grc-rcm/image/summary-icon.png)\).**|Open the Feedback trail side-panel to review the related activity for the recommendation.|

7.  Accept or dismiss the recommendations and their associations.

    -   Select **Accept** and then **Confirm** to accept a recommendation as an impacted area.
    -   Select **Dismiss** and then **Confirm** to avoid a recommendation from being shown again.
    Before you act on a recommendation, you see a summary of the impact areas and associations that you’re accepting or dismissing.

    If you accept the recommendation, it’s marked as an impacted area and is added to the list of impacts. If you dismiss the recommendation, it’s marked as dismissed and isn't shown again for that specific regulatory alert.


## What to do next

If you accepted any recommendations, confirm the creation of an impacted area by navigating to the Impacted areas tab. If you dismissed all recommendations or must add more impacted areas, you can manually add impacted areas. For more information, see [Add impacted areas manually to a regulatory alert](add-impacted-area-reg-alert.md).

