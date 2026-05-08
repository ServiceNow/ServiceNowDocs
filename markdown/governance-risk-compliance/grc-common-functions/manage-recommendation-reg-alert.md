---
title: Accept or dismiss recommendations for regulatory alert impacted citations
description: Accept recommendations to mark specific business areas as impacted, helping compliance practitioners capture and address relevant regulatory alerts for citations. Dismiss recommendations to filter out irrelevant or unnecessary information.
locale: en-US
release: australia
product: GRC Common Functions
classification: grc-common-functions
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
keywords: [Now Assist, generative AI]
breadcrumb: [Generate recommendations for regulatory alert impacted areas, Use generative AI skills, Now Assist, Common GRC features, Governance, Risk, and Compliance]
---

# Accept or dismiss recommendations for regulatory alert impacted citations

Accept recommendations to mark specific business areas as impacted, helping compliance practitioners capture and address relevant regulatory alerts for citations. Dismiss recommendations to filter out irrelevant or unnecessary information.

## Before you begin

**Important:** This Now Assist skill is turned on by default. The skill will be automatically available to appropriate role users for the application. For more information, see Now Assist skills, agents, and agentic workflows on by default.

Role required: To view your assigned regulatory alerts, you need the sn\_grc\_reg\_change.user and sn\_grc\_comp\_genai.reg\_change\_ai\_user roles.

For more information on related roles and regulatory alerts, see [Types of alerts, user roles, and states of regulatory alerts](../../grc-rcm/reference/user_roles_and_actions.md).

**Important:** Be sure to check AI-generated recommendations for accuracy. If no information is available, the generated recommendations display "No recommendations available", "None", "No records to display", and so on.

## Procedure

1.  Navigate to one of the following locations:

    -   **Workspaces** &gt; **Compliance Workspace**, select the list icon ![](../../grc-cam-workspace/image/ws-list-icon.png) and then navigate to **Regulatory alerts**.
    -   **Workspaces** &gt; **Compliance Workspace** select the Regulatory Change Management dashboard icon ![](../../grc-rcm/image/reg-change-icon.png) and then in the Activity overview, Tracking, or Trends section, select any segment or value in an Alerts related widget to open the list of regulatory alerts with that state.
2.  Select the regulatory alert that you want and review the recommendations by selecting the Recommendations tab.

    **Note:** If recommendations haven’t already been generated, you can generate recommendations for a regulatory alert in any state except Closed or Cancelled by completing one of the following.

    -   On the Overview tab, select **Recommend**.
    -   On the Recommendations tab, select **Show recommendations**.
    For more information, see [Generate recommendations for regulatory alert impacted citations, control objectives, controls, and policies](create-recommendation-reg-alert.md).

3.  Review potential impact areas by selecting the Citations tab in the Recommended areas of the impact section.

    The recommended citations only include citations that are part of the existing inventory.

    ![Details of the recommended citation.](../../grc-rcm/image/reco-c-details.png)

    **Note:** The `Suggest business operations affected by regulatory alert recommendation context` provides the recommendations that you see here. For more information, see [Recommendation contexts and templates](../../grc-rcm/concept/recommendation-contexts.md).

    If recommendations are available, you can scroll through the generated list of citation recommendation cards and review the information about each control, such as its name and compliance status.

4.  Review potential impact areas by selecting the Citations tab in the Recommended areas of impact section.

    If recommendations are available, you can scroll through the generated list of citation recommendation cards and review information about each citation, such as its name and authority document.

5.  Select the citations recommendation card that you want and review the following sections:

<table id="id_o2v_k4c_cfc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the citation.

</td></tr><tr><td>

Reference

</td><td>

Unique numerical identifier or secondary name.

</td></tr><tr><td>

Description

</td><td>

Description and summary of the citation.

</td></tr><tr><td>

Supplemental Guidance

</td><td>

Additional guidance on how to address the citation.

</td></tr><tr><td class="sub-head" colspan="2">

**Evaluate Affected Associations**

</td></tr><tr><td>

Child citations

</td><td>

Individual requirements within an authority document that are tied to this recommended parent citation.For each child citation, the following information is provided if available.

-   Reference
-   Name of the citation
-   Authority document associated with the citation
-   Description


</td></tr><tr><td>

Control objectives

</td><td>

Related goal or requirement that can be associated with the citation.For each control objective, the following information is provided if available.

-   Reference
-   Name of the control objective
-   Category that the control objective is associated with
-   Classification for the control objective


</td></tr></tbody>
</table>    For full descriptions of these fields, see [Create or deactivate a citation](../../grc-policy-and-compliance/task/t_CreateCitations.md) and [Create a control objective](../../grc-policy-and-compliance/task/t_CreateAPolicyStatement.md).

6.  To associate child citations or control objectives with your recommendation, navigate to the corresponding tab and select the check box for each record you want to include as part of the impacted areas.

    Each selected record will be added as an impacted area after you accept the recommendation.

    **Note:** The citation you’re reviewing may not have anything associated with it. Child citations or control objectives must be mapped to citations in the inventory for them to appear.

    ![Details of the affected associations for controls.](../../grc-rcm/image/reco-citation-associations.png)

7.  View the record for a citation, refresh your recommendations, or review related activity for each recommendation.

    |Option|Description|
    |------|-----------|
    |**Select the details icon ![](../../grc-privacy-management/image/details-icon.jpg).**|View the record for a citation.|
    |**Select the refresh icon ![](../../grc-risk/image/refresh-icon.jpg).**|Refresh the recommendations to reflect the latest data.|
    |**Select the summary icon ![](../../grc-rcm/image/summary-icon.png).**|Open the Feedback trail side-panel to review the related activity for the recommendation.|

8.  Accept or dismiss the recommendations and their associations.

    -   Select **Accept** and then **Confirm** to accept a recommendation as an impacted area.
    -   Select **Dismiss** and then **Confirm** to avoid a recommendation from being shown again.
    Before you act on a recommendation, you see a summary of the impact areas and associations that you’re accepting or dismissing.

    If you accept the recommendation, it’s marked as an impacted area and is added to the list of impacts. If you dismiss the recommendation, it’s marked as dismissed and isn't shown again for that specific regulatory alert.


## What to do next

If you accepted any recommendations, confirm the creation of an impacted area by navigating to the Impacted areas tab. If you dismissed all recommendations or must add more impacted areas, you can manually add impacted areas. For more information, see [Add impacted areas manually to a regulatory alert](add-impacted-area-reg-alert.md).

