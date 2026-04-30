---
title: Sample use case scenarios
description: Use case scenarios offer a clear and comprehensive explanation of why you would use the Entity Based Access application.
locale: en-US
release: yokohama
product: GRC Common Functions
classification: grc-common-functions
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Entity Based Access, Common GRC features, Governance, Risk, and Compliance]
---

# Sample use case scenarios

Use case scenarios offer a clear and comprehensive explanation of why you would use the Entity Based Access application.

## Use case scenario overview

ExampleCo is a multinational organization with operations that span the American and Asian continents. The company specializes in the insurance and banking industries. The following example shows the organizational hierarchy of this company.

![Organizational hierarchy of ExampleCo.](../image/eba-hierarchy.png "Organizational hierarchy of ExampleCo")

## Use case scenario 1

Abel Tutor, the Head of Asia Operations, needs access to records that are specific to the Asian continent.

To achieve this result, you use the Entity Based Access application to configure an entity-based access restriction that applies to users. Then, you apply an entity-based access restriction at a record level by using the bulk access update configuration.

You would then select ExampleCo Asia and map it to Abel in the entity configuration. Alternatively, you could map it to a user group that Abel is a part of. The following example shows that Abel is granted with access to all the records in the Asian continent.

![Entity configuration screen for a user.](../image/usecase1.png "Entity configuration for a user")

## Use case scenario 2

A second use case scenario involves granting Beth Anglin, the Operations Head of the Banking domain, with access exclusively to banking-related records.

To achieve this result, you use the Entity Based Access application to configure the entity class configuration and applicable users. The entity class denotes a group of records that the access restriction can be applied to. Then, you apply an entity-based access restriction at a record level by using the bulk access update configuration.

You select the Banking entity class and map it to Beth. Alternatively, you could map it to a user group where Beth is a part of. The following example shows that the Banking entity class is mapped to Beth.

![Entity class configuration screen for a user.](../image/usecase2.png "Entity class configuration for a user")

**Parent Topic:**[Entity Based Access](entity-based-access.md)

