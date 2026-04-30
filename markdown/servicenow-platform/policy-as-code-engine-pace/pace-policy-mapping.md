---
title: PaCE Static and Dynamic Mapping
description: Static Mapping enables you to map a set of policies to a record or object such as an incident or deployable. Dynamic Mapping enables you to map a set of policies on a dynamic set of records or objects such as a set of incidents or a set of deployables.
locale: en-US
release: zurich
product: Policy as Code Engine \(PaCE\)
classification: policy-as-code-engine-pace
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Manage PaCE policies, Administer PaCE policies, Policy as Code Engine \(PaCE\), Extend ServiceNow AI Platform capabilities]
---

# PaCE Static and Dynamic Mapping

Static Mapping enables you to map a set of policies to a record or object such as an incident or deployable. Dynamic Mapping enables you to map a set of policies on a dynamic set of records or objects such as a set of incidents or a set of deployables.

## Static Mappings

Static Mapping enables you to map multiple policies that you want to validate against a specific deployable or incident. For example, if you need to map a policy to multiple deployables, you’ll need to map it multiple times to each deployable.

## Dynamic Mappings

Dynamic Mapping enables you to map multiple policies that you want to validate against specified conditions. You can configure the conditions set to a specific table, each condition can return multiple records or objects. The condition is applied at a runtime where the set of policies will be mapped to the set of returned records by the condition. Multiple conditions can be defined in the condition fields in the Conditions tab.

