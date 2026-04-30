---
title: Example: Link the similar major case to the current case
description: Learn how process analysts or business owners configure a recommended action of type guidance to propose a major case that can be linked to the current case. This guidance uses a resource generator of type similarity with trend to recommend the similar case that has a common trend.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Example configurations of recommended actions, Recommended Actions configuration, Implement Intelligence, Configuring Customer Service Management, Customer Service Management]
---

# Example: Link the similar major case to the current case

Learn how process analysts or business owners configure a recommended action of type guidance to propose a major case that can be linked to the current case. This guidance uses a resource generator of type similarity with trend to recommend the similar case that has a common trend.

## Problem scenario

Isabella owns a thriving E-commerce business that specializes in selling handmade artisanal products. As the business grows, Isabella recognizes the increasing importance of providing exceptional customer service to maintain customer satisfaction and loyalty. Isabella understands that addressing customer issues effectively and promptly is crucial for the success of the business.

Daniel, a process analyst on the Isabella's team identifies the most common and critical issues that their customers report and create major cases for them. So that whenever a customer creates a case, it can be linked to the similar major case. This process helps them understand the pattern, identify the root cause, take corrective actions, and apply similar solutions.

Daniel identifies the following major issues:

-   Missing items in the order
-   Wrong items received
-   Damaged or defective products
-   Refund requests
-   Billing discrepancies or errors
-   Difficulty applying discount codes
-   Difficulty reaching customer support

Now, Daniel configures a guidance that recommends a similar major case to the agent who is working on a new case created by a customer. The guidance provides an action to the agent to link the recommended major case to the current case.

## Configuring a recommended action for linking the similar major case to the current case

Help Daniel configure a recommended action of type guidance that uses Similarity with Trend resource generator to link the major case to the current case.

|Task|Description|
|----|-----------|
|[Configuring a subflow for the guidance action automation](ex-ra-config-subflow-link-major-case.md)|Configure a subflow that you can use in a guidance to link the proposed major case to the current case automatically on a click of an action button.|
|[Configure a resource generator for providing a similar major case to the current case](../task/ex-ra-resource-generator-similarity-trend.md)|Configure a resource generator of type similarity with trend that provides a similar major case to the current case.|
|[Create a guidance for linking the similar major case to the current case](../task/ra-ex-guidance-link-major-case.md)|Create a guidance to link the similar major case to the current case by configuring guidance inputs, preview experience, and guidance action.|
|[Create a rule from the Case context record](../task/ex-create-rule.md)|Create a rule to show recommendations for active cases that meet the condition specified in this rule.|
|[Create a recommendation with guidance as an action type](../task/ex-create-recommendation-guidance.md)|Create a recommendation to select the Guidance as an action type for linking a major case to the current case record.|

