---
title: Recommendation contexts and templates
description: By using the Governance, Risk, and Compliance recommendations framework, you can use recommendation contexts and templates to deliver AI-driven insights directly to your users within the user interface. With these insights, your users can make informed decisions and take prompt actions.
locale: en-US
release: australia
product: GRC Common Functions
classification: grc-common-functions
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Common GRC features, Governance, Risk, and Compliance]
---

# Recommendation contexts and templates

By using the Governance, Risk, and Compliance recommendations framework, you can use recommendation contexts and templates to deliver AI-driven insights directly to your users within the user interface. With these insights, your users can make informed decisions and take prompt actions.

## Recommendation context and template overview

Use the Governance, Risk, and Compliance Recommendation Template plugin \(app-grc-reco-template\) so that you can capture, document, and submit the recommendations that your users see in the interface.

A recommendation context refers to the information and conditions that shape your user's preferences and needs. The recommendation framework provides a user with relevant suggestions by adapting the recommendation to the user's situation.

With the Governance, Risk, and Compliance recommendation contexts framework, you can create a recommendation context to define a configuration to build a template for recommending relevant records. You can also create a recommendation template to train the AI models with a data set for identifying your key business operations. Before you can create a recommendation template, you must have a recommendation context.

For more information about creating a recommendation context, see [Create a recommendation context](../task/configure-recommendation-context.md).

For more information about creating a recommendation template, see [Create a recommendation template](../task/create-a-recommendation-template.md).

## GRC Administration menu

Users with the sn\_reco\_template.recommendation\_config\_reader role can read the recommendation contexts from the GRC Administration menu while users with the sn\_reco\_template.recommendation\_config\_writer can create or edit the recommendation contexts.

Navigate to **All** &gt; **GRC Administration** &gt; **Recommendation contexts** to see the list of available recommendation contexts. The `Suggest business operations affected by regulatory alert` recommendation context \(the base recommendation context\) suggests recommendations for the following for a regulatory alert:

-   Citations
-   Control objectives
-   Controls
-   Policies

For more information about the user roles that can access this menu item, see [User roles for recommendation contexts](../reference/user-roles-for-recommendation-contexts.md).

The following example shows the GRC Administration menu.

![Navigation screen to recommendation contexts.](../image/reco-context-grc-admin-menu.png "GRC Administration menu")

You can select an item that fits the context to build a template for recommending relevant records. You can use the existing configurations as is or update them. You can also select the AI search type that matches a user's needs for recommending relevant items that are based on the context and criteria. In addition, you can configure the relationship section that displays the related items for each recommendation and specifies their titles. For more information, see [Create a recommendation template](../task/create-a-recommendation-template.md).

## Extension points

Recommendation contexts use extension points to extend the functionality of an application without altering the original application code. Your developers can use pre-existing extension points or can add extension points for custom applications. For more information about extension points, see [Extension points](extension-points.md).

-   **[User roles for recommendation contexts](../reference/user-roles-for-recommendation-contexts.md)**  
Users with different roles can read, create, or edit recommendation contexts for a regulatory alert.
-   **[Extension points](extension-points.md)**  
Use extension points to extend the functionality of an application without altering the original application code. Recommendation contexts use extension points to enable additional functionality while configuring the recommendation contexts or templates.
-   **[Create a recommendation context](../task/configure-recommendation-context.md)**  
Create a recommendation context to define a configuration that builds a template for recommending relevant records.
-   **[Create a recommendation template](../task/create-a-recommendation-template.md)**  
Create a recommendation template to train the AI models with a data set for identifying your key business operations. Key business operations include managing regulatory changes, assessing risks, and adhering to compliance guidelines.

**Parent Topic:**[Common Governance, Risk, and Compliance features](../../grc-common/concept/common-grc-features.md)

