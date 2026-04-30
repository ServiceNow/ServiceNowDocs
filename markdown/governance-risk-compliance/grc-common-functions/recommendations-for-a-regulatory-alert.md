---
title: AI-generated recommendations for a regulatory alert skill
description: The recommendations framework is designed to deliver actionable, AI-driven insights directly within the user interface. It provides rich contextual information about recommendations, empowering users to make well-informed decisions and take follow-up actions seamlessly. The scalable and flexible design supports multiple recommendation types and complex business scenarios.
locale: en-US
release: yokohama
product: GRC Common Functions
classification: grc-common-functions
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Explore, Now Assist, Common GRC features, Governance, Risk, and Compliance]
---

# AI-generated recommendations for a regulatory alert skill

The recommendations framework is designed to deliver actionable, AI-driven insights directly within the user interface. It provides rich contextual information about recommendations, empowering users to make well-informed decisions and take follow-up actions seamlessly. The scalable and flexible design supports multiple recommendation types and complex business scenarios.

Enhancing the recommendations framework empowers regulatory change managers to use the AI-driven recommendations for better identification of impactful business operations based on regulatory changes.

A default recommendation context named `Suggest business operations affected by regulatory alert` powered by Now Assist for IRM is shipped along with the Regulatory Change Management product. This recommendation context is used for generating recommended citations and control objectives for a regulatory alert.

**Note:** Only users with the sn\_grc\_comp\_genai.reg\_change\_ai\_user role are able to see the option to generate recommendations for a regulatory alert. This role must be manually assigned to an RCM user.

## Highlights of the recommendation framework

-   **Configurable recommendations and actions**
    -   Enable you to define and configure recommendations for various record types.
    -   Enable setup of follow-up actions, so users can act on recommendations directly within the workflow.
-   **Intelligent recommendations**
    -   Leverage advanced AI capabilities, including generative AI and Predictive Intelligence, to display relevant recommendations.
    -   Continuously improve insights and recommendations by incorporating machine learning models and predictive scoring.
-   **Scalable design**
    -   Support the display of multiple recommendations for a single record type.
    -   Provide flexibility for administrators to customize the layout and structure of the recommendation panel according to business needs.
    -   Adapt to a variety of record types and recommendation techniques, ensuring consistency and scalability across use cases.
-   **Adoption enablement**
    -   Designed for rapid integration and adoption across upstream products.
    -   Offer a user-friendly, intuitive interface that empowers decision-makers with clear, actionable insights.
-   **Rationalization support**

    Enable customization of deduplication logic, enabling businesses to define their own rules and criteria for identifying duplicate records.


## Key benefits

-   Contextual visibility into recommendations for better decision-making.
-   A scalable, configurable framework adaptable to various use cases and record types.
-   Faster adoption for products looking to leverage AI/ML-based recommendations.
-   Customizable workflows and logic to meet specific organizational processes.
-   Improved user productivity with actionable recommendations and clear next steps built directly into the interface.

**Note:** Only users with the sn\_grc\_comp\_genai.reg\_change\_ai\_user role can see the option to generate recommendations for a regulatory alert. This role must be manually assigned to an RCM user.

To understand how you can create recommendations for a regulatory alert and activate the Regulatory alert impacted citations and Regulatory alert impacted control objectives skills, refer to [Activate Regulatory alert recommendation skills](../../now-assist-irm/task/configure-recommendation-skill-for-a-regulatory-alert.md), and [Generate recommendations for regulatory alert impacted citations, control objectives, controls, and policies](../../now-assist-irm/task/create-recommendation-reg-alert.md).

## Viewing a recommendation

After generating recommendations for a regulatory alert, the Recommendations page displays the following sections:

-   Recommended areas of impact
-   Citations
-   Control objectives
-   Description
-   Evaluate affected associations

The following tables provide more information on the sections and the related lists that are associated with the recommendations.

<table id="table_wlj_4q5_nqb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Last refreshed

</td><td>

Date and time the recommendations were last generated or refreshed. You can select the refresh icon ![](../../grc-risk/image/refresh-icon.jpg) to view the latest recommendations.

</td></tr><tr><td>

Citations

</td><td>

Details of the citations.For example, the name of the citation, the parent of the citation, and authority document.

</td></tr><tr><td>

Control objectives

</td><td>

Details of the control objective. For example, the name of the control objective and parent.

</td></tr></tbody>
</table>**Note:** For more information about citations and control objectives, see [Structural overview of Policy and Compliance Management](../../grc-policy-and-compliance/concept/pc-structural-overview-policy-comp.md).

|Field|Description|
|-----|-----------|
|Description|Description and a summary of the citation or control objective.|
|Supplemental guidance|Additional guidance on how to address the citation or control objective.|

|Field|Description|
|-----|-----------|
|Child citations, Control objectives|Related lists containing potential affected areas for a citation that you can add as part of the recommendation.|
|Child control objectives, Policies, Controls, Risk statements|Related lists containing potential affected areas for a control objective that you can add as part of the recommendation.|

Feedback trail side-panel: The feedback side-panel displays the history of user interactions with recommended items. This can include what the user accepted, what they skipped or ignored, and what they dismissed.

For more information on generating recommendations, see [Generate a regulatory alert summary](../../now-assist-irm/task/create-a-summary-of-a-reg-alert.md).

**Related topics**  


[Activate Regulatory alert recommendation skills](../../now-assist-irm/task/configure-recommendation-skill-for-a-regulatory-alert.md)

[Generate recommendations for regulatory alert impacted citations, control objectives, controls, and policies](../../now-assist-irm/task/create-recommendation-reg-alert.md)

