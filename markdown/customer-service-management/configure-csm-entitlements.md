---
title: Configure entitlements
description: An entitlement defines the type of support that a customer receives as well as the supported communication channels.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Product data, Set up your environment, Configuring Customer Service Management, Customer Service Management]
---

# Configure entitlements

An entitlement defines the type of support that a customer receives as well as the supported communication channels.

## Before you begin

Role required: sn\_customerservice\_manager or admin

## About this task

You can associate an entitlement with a product, an asset, an account, or a contract. An entitlement check is performed when a case is opened. This check considers the existing cases for the specific account, product, asset, and service contract. Entitlements can also have associated workflows that drive recommended activities for a case.

Entitlements are counted on a per-unit basis. The **Unit** field on the Service Entitlement form defines the unit type, either cases or hours.

The **Total Units** field defines the total number of cases or hours available for this entitlement and the **Remaining Units** field tracks the number of units remaining. These counters are active if the **Per Unit** field is enabled.

The **Remaining Units** field is updated using business rules.

-   When using cases as the unit type, the **Update case entitlement on Close** business rule updates this field when a case for a product, asset, company, or contract that has an associated entitlement is closed.
-   To use hours as the unit type, customers must create a separate business rule. For example, create a rule that is applied to the amount of time an agent spends on a case. When a case is resolved, deduct the hours spent from the total service hours available in the entitlement.

Keep these guidelines in mind as you create entitlements.

-   Product entitlements: When creating an entitlement for a product, select the product from the **Product** field and then select an account or a consumer.
-   Asset entitlements: When creating an entitlement for an asset, first select a company. The only assets then shown belong to that company.
-   Contract entitlements: When creating an entitlement for a contract, select the contract and then the assets that are covered as a contract line item. The resulting contract entitlement is valid for the assets listed within that contract.

## Procedure

-   Create entitlements for customer service entities

-   Associate entitlements with customer service entities


