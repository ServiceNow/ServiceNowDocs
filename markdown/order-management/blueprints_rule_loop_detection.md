---
title: Circular references in rules and fields
description: Circular references in a blueprint may result in an error.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Set up blueprints, CPQ app, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Circular references in rules and fields

Circular references in a blueprint may result in an error.

CPQ Admin allows administrators to define a blueprint whose rules and fields result in a circular reference. If the end user enters configuration inputs that initiate an endless loop, an error state occurs.

For example, suppose rule 1 consists of a condition on field A and a determination action that sets field B, while rule 2 has a condition on field B and a determination action that sets field B. These interacting rules would create an endless loop.

Loops may also be composed of many fields and rules. In more complex use cases, it is common for testers and end users to successfully operate the configuration blueprint without encountering the error state. The CPQ Rule Cycle Report identifies potential loops so that the administrator can understand their risk and correct them.

To identify endless loops in a blueprint, use the Rule Cycle Report. See [Identify endless loops in blueprint rules](cpq-identify-endless-loops.md).

**Related topics**  


[Identify endless loops in blueprint rules](cpq-identify-endless-loops.md)

