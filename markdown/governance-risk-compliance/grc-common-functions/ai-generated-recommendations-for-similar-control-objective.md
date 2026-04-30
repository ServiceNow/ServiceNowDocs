---
title: AI-generated recommendations for similar control objectives
description: The recommendations framework is designed to deliver actionable, AI-driven recommendations for similar control objectives directly within the user interface. It provides rich contextual information about similar control objectives, empowering users to make well-informed decisions and take follow-up actions seamlessly.
locale: en-US
release: zurich
product: GRC Common Functions
classification: grc-common-functions
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Explore, Now Assist, Common GRC features, Governance, Risk, and Compliance]
---

# AI-generated recommendations for similar control objectives

The recommendations framework is designed to deliver actionable, AI-driven recommendations for similar control objectives directly within the user interface. It provides rich contextual information about similar control objectives, empowering users to make well-informed decisions and take follow-up actions seamlessly.

The Control objective deduplication and rationalization feature is designed to help compliance managers and analysts streamline their compliance processes by identifying, deduplicating, and rationalizing similar control objectives within their compliance library. This feature leverages AI to automate the identification of redundant control objectives, helping to make it easier to maintain a clean and efficient compliance library.

## Highlights of the recommendation framework

-   **Configurable recommendations and actions**
    -   Enable you to define and configure recommendations for various record types.
    -   Enable setup of follow-up actions, so you can act on recommendations directly within the workflow.
-   **Intelligent recommendations**
    -   Leverage advanced AI capabilities, including generative AI and Predictive Intelligence, to display relevant recommendations.
    -   Continuously improve insights and recommendations by incorporating machine learning models and predictive scoring.
-   **Scalable design**
    -   Support the display of multiple recommendations for a single record type.
    -   Provide flexibility for administrators to customize the layout and structure of the recommendation panel according to business needs.
    -   Adapt to a variety of record types and recommendation techniques, confirming consistency and scalability across use cases.
-   **Adoption enablement**
    -   Designed for rapid integration and adoption across upstream products.
    -   Offer a user-friendly, intuitive interface that empowers decision-makers with clear, actionable insights.

## Key benefits

-   Contextual visibility into recommendations for better decision-making.
-   A scalable, configurable framework adaptable to various use cases and record types.
-   Faster adoption for products looking to leverage AI/ML-based recommendations.
-   Customizable workflows and logic to meet specific organizational processes.
-   Improved user productivity with actionable recommendations and clear next steps built directly into the interface.

**Note:** Only users with sn\_reco\_template.rationalization\_process\_writer and sn\_grc\_shared\_genai.compliance\_gen\_ai\_user can see the option to generate recommendations for similar control objective. This role must be manually assigned to a compliance user.

To generate recommendations for a control objective, configure Now Assist for Integrated Risk Management \(IRM\). See [Configure Now Assist for Integrated Risk Management \(IRM\)](../../grc-common/concept/configure-now-assist-for-irm.md).

## Viewing recommendations

After generating recommendations for similar control objectives, the Recommendations page displays the following sections:

-   Recommendation
-   Control objectives
-   Description
-   Response actions
-   Evaluate affected associations

The following tables provide more information on the sections and the related lists that are associated with the recommendations.

<table id="table_ybw_jyk_dfc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Control objectives

</td><td>

Details of the control objective. For example, the name of the control objective and parent.

</td></tr><tr><td>

Last refreshed

</td><td>

Date and time the recommendations were last generated or refreshed. You can select the refresh icon ![Refresh icon.](../../grc-risk/image/refresh-icon.jpg) to view the latest recommendations.

</td></tr></tbody>
</table>**Note:** For more information about control objectives, see [Structural overview of Policy and Compliance Management](pc-structural-overview-policy-comp.md).

|Field|Description|
|-----|-----------|
|Description|Description and a summary of the control objective.|
|Supplemental guidance|Additional guidance on how to address the control objective.|

|Field|Description|
|-----|-----------|
|Impacted Items \(Controls, Policy exceptions, Issues, and more\)|Related lists containing items directly affected by the consolidation of new control objectives.|
|Associated Items \(Entities, Entity type, policies, citations, control objectives and more|Related lists containing all associations from accepted control objectives in a consolidated view.|

|Action|Description|
|------|-----------|
|Accept as duplicate|Acceptance of a recommendation as a duplicate by selecting Accept as duplicate and then selecting Confirm.|
|Dismiss|Removal of a recommendation from future suggestions by selecting Dismiss and then selecting Confirm.|
|Retain as primary|Retention of the control objective as the main one by selecting Retain as primary and then selecting Confirm.|
|Create common control objective|Generation of a consolidated control objective using generative AI after accepting duplicates by selecting Create.|

Feedback trail side-panel: The feedback side-panel displays the history of user interactions with recommended items. This can include what the user accepted, what they skipped or ignored, and what they dismissed.

For more information on generating recommendations, see [Use Recommendation of similar control objectives skill to generate suggestions](generate-recommendation-for-a-new-control-objective.md).

