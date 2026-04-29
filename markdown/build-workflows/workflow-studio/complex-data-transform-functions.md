---
title: Complex data transform functions
description: Use complex data transform functions to serialize Complex Object data pills into an XML format.
locale: en-US
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Transform functions, Flows, subflows, and actions reference, Flows, subflows, and actions, Workflow Studio, Build workflows]
---

# Complex data transform functions

Use complex data transform functions to serialize Complex Object data pills into an XML format.

Complex data functions require a Complex Object input data pill. Make sure to use the correct input [data pill type](action-inputs-outputs.md) when applying complex data transform functions. If a complex data transform function is applied to an improper data type, the data is not transformed at runtime and the input value is returned instead. For more information on confirming your flow runtime values, see [Test a flow](../task/flow-test.md).

## To XML

Serializes the input Complex Object to XML.

|Input data pill|Output data pill|
|---------------|----------------|
|Complex Object|XML - XML document formatted as a String|

-   Input: `{ "article_id": KB3843202, "article_description": "How do I reset my Active Directory password?" }`
-   Output: `<article_id>KB3843202</article_id> <article_description>How do I reset my Active Directory password?</article_description>`

In this example, an action makes a REST call to a third-party knowledge base and retrieves KB article IDs and descriptions. The To XML transform function changes the response body's JSON text into XML format before it is integrated into the system's knowledge base.

![Knowledge base article data is transformed from JSON text to XML format.](../images/to-xml-transform-function-example.png "Data transformed from JSON text to XML format")

**Parent Topic:**[Transform functions](../concept/transform-functions.md)

