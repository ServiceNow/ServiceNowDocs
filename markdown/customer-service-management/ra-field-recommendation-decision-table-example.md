---
title: Example: Recommend an assignment group for a router issue
description: Learn how process analysts or business owners configure a recommended action of type field recommendation to recommend an assignment group for a router issue. This field recommendation uses a resource generator of type decision table that takes the router model and router issue as inputs and provides an assignment group as a result.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Example configurations, Recommended Actions configuration, Implement Intelligence, Configure, Customer Service Management]
---

# Example: Recommend an assignment group for a router issue

Learn how process analysts or business owners configure a recommended action of type field recommendation to recommend an assignment group for a router issue. This field recommendation uses a resource generator of type decision table that takes the router model and router issue as inputs and provides an assignment group as a result.

## Problem scenario

QuantumLink Technologies, a newcomer to the networking equipment market, places a strong emphasis on customer satisfaction and resolving customer issues promptly. The business owners are committed to provide excellent customer service so that their business can thrive.

Alisha, one of the business owners at QuantumLink Technologies, sets up a recommended action that recommends a value for the Assignment group field based on the product model and problem specified by customers.

Rohit, a customer who recently purchased a QuantumLink router, is facing intermittent connectivity issues with his router. He creates a case on QuantumLink Technologies' customer support portal. John is frustrated by the disruptions in his internet service and is seeking a swift resolution to confirm uninterrupted connectivity for his home and work needs.

John Jason, the agent assigned to this case is recommended a field value for an assignment group so that this case can be assigned to the appropriate team and the issue can be resolved quickly.

## Configuring a recommended action for recommending an assignment group for a router issue

Help Alisha configure a recommended action of type field recommendation that recommends an assignment group for a router issue.

|Task|Description|
|----|-----------|
|[Creating a decision table for recommending assignment groups](ex-decision-tree-for-assgment-grp-recommendation.md)|Configure a decision table that takes product and problem as inputs to provide the assignment group as an output. You can use this decision table in a resource generator.|
|[Configure a resource generator for providing assignment group as an outcome](../task/ex-resorce-generator-assignment-grp.md)|Configure a resource generator that you can use while configuring a field recommendation to provide the appropriate assignment group for the router issue.|
|[Create a field recommendation for recommending assignment group field value](../task/ex-create-field-recommendation-assg-grp.md)|Create an action of type field recommendation for recommending a field value for the assignment group.|
|[Create a rule from the Case context record](../task/ex-create-rule.md)|Create a rule to show recommendations for active cases that meet the condition specified in this rule.|
|[Create a recommendation with the field recommendation as an action type](../task/ex-create-recommendation-field.md)|Create a recommendation to surface the recommendation for the assignment group field value on a case record.|

