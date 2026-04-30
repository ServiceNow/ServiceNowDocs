---
title: Assess business capability - Legacy
description: Assess the business capabilities within the indicator framework and based on the score you can make strategic decisions on the business applications that support the business capability.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Use - Legacy, Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Assess business capability - Legacy

Assess the business capabilities within the indicator framework and based on the score you can make strategic decisions on the business applications that support the business capability.

## Before you begin

Role required: sn\_apm.apm\_admin

## About this task

Each business application and business capability have a unique identity as a configuration item \(CI\). Such a distinction helps to establish a relationship between these independent configuration items. The CI relationship helps to establish a parent-child relationship between business capability and business application, and business application and business capability.

The configuration items must be associated to a set of indicators to generate a weighted score for evaluation. Preconfigured indicators such as people, process, and technology are used to assess business capability.

The indicator scoring framework also supports scoring of business capability in addition to business application. Within this framework the preconfigured indicators including people, process, and technology, as well as the indicators that you have created, are evaluated to give the indicator scores. For business applications you can create multiple scoring profiles. Each scoring profile can contain multiple indicators. But for capabilities you can create only one scoring profile and not multiple scoring profiles.

## Procedure

1.  Create CI relationships or edit the existing relationships using [CI relationships in the CMDB](https://www.servicenow.com/docs/access?context=c_CIRelationships&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).

2.  Relate business capabilities and business applications using the following pre-determined CI relationship types:

    |Parent|Type|Child|
    |------|----|-----|
    |Business Capability|Provided By::Provides|Business Application|
    |Business Application|Provides::Provided by|Business Capability|

    **Note:** Both the business capability and the business application are configuration item entities.

    The parent column of the capabilities table is used to create the capability hierarchy.


## What to do next

[Create a business capability](create-a-business-capability.md) and relate the capability to a business application using the CI relationship editor.

**Parent Topic:**[Using Enterprise Architecture \(formerly Application Portfolio Management\) - Legacy](../concept/using-apm.md)

