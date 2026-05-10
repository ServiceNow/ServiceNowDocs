---
title: Configuring needs analysis
description: As a product catalog administrator, you can create needs templates, which are questionnaires that agents use to find product offers to add to a lead or opportunity. Questionnaires function as product selection guides. When agents complete a questionnaire based on customer input, they get product recommendations that they can add to a lead or opportunity.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configuring product offerings and catalogs, Lead-to-cash foundation apps, Configure, Sales Customer Relationship Management]
---

# Configuring needs analysis

As a product catalog administrator, you can create needs templates, which are questionnaires that agents use to find product offers to add to a lead or opportunity. Questionnaires function as product selection guides. When agents complete a questionnaire based on customer input, they get product recommendations that they can add to a lead or opportunity.

## Overview of needs analysis

When agents create a lead in the Lead Management application or an opportunity in the Opportunity Management application, a product selection guide is displayed in the product catalog. The product selection guide lists the needs templates that agents can choose to get product offer recommendations.

![Product catalog page with needs template, needs questionnaire and product recommendations in Opportunity Management, and decision tree start node in Decision Tree Builder](../image/needs-analysis-elements.png "Elements of needs analysis")

-   **Needs template**

    Product selection guides associated with the product catalog display one or more needs templates. Each needs template is a questionnaire that has a set of guided questions that agents answer to get product recommendations for a customer. Each template is associated with a needs decision tree.

-   **Needs decision tree**

    A multi-step, guided decision process that presents a series of questions to the agent. You use Decision Tree Builder to create and build the decision tree.The decision tree defines the question nodes, expected answers, connection points, decision logic, and guidance for decision paths in the questionnaire.

-   **Product recommendations**

    The product offerings suggested for an opportunity or lead, based on the results of the needs questionnaire.


## Working with decision trees

You configure decision trees by adding nodes, defining paths, and attaching guidances in Decision Tree Builder. This tool is a canvas for diagramming the basic elements in a decision tree, such as the question nodes and decision paths. Needs analysis provides a default guidance, the Product Offering Recommendation guidance, which references information from the Needs Based Offering Recommendation \[sn\_prd\_pm\_product\_offering\_recommendation\] table as you create the question nodes and guidances in the decision tree.

Before creating decision trees for needs templates, review how decision trees work:

-   [Decision trees in Guided decision](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/decision-trees-in-guided-decisions.md) - Learn the basic elements of a decision tree, such as node types, linking inputs in nodes, and decision tree paths.
-   [Example configuration of a decision tree](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/example-decision-tree.md) - Review an example decision tree, including preparations for creating a decision tree, to understand the end-to-end configuration of a decision tree.
-   [Answer types for questions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/type-of-answer.md) - Learn about the various types of answers to questions, such as Choice, Date, or Integers.

## Setting up needs analysis

Follow these steps to configure needs analysis:

1.  [Create a needs-based product offering recommendation](../task/create-product-recommendations.md).
2.  [Create a decision tree for a needs template](../task/configure-needs-decision-tree.md).
3.  [Build a needs decision tree](../task/build-needs-decision-tree.md).
4.  [Create a needs template and set the catalog relationship](../task/create-publish-needs-template.md).

