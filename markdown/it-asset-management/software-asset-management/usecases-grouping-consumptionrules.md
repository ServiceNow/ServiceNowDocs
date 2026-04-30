---
title: Use cases for grouping and consumption rules
description: Learn how grouping and consumption rules are used during the reconciliation process through some use cases.
locale: en-US
release: xanadu
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2024-08-21"
reading_time_minutes: 2
breadcrumb: [Grouping and consumption rules in reconciliation, Software reconciliation for compliance, Exploring Software Asset Management, Software Asset Management, IT Asset Management]
---

# Use cases for grouping and consumption rules

Learn how grouping and consumption rules are used during the reconciliation process through some use cases.

The following use cases help you understand the ramifications of using only grouping, only consumption rules, or using both grouping and consumption rules during the reconciliation process.

We have two entitlements. Entitlement 1 is owned by company A and entitlement 2 is owned by company B. Each entitlement has its own consumption rule. Both the entitlements belong to the same license metric, the same product and both have five rights each. Additionally, there are 11 installations; five installations for company A, 5 installations for company B, and one installation for company C.

## Without grouping and without consumption rules use case

In this use case, no grouping or consumption rules leads to a single product result that shows the following outcomes:

![use case with no grouping and no consumption rules](../image/usecase1.png)

In this scenario, the entitlement owners are ignored and consumption is unrestricted. Available rights of the two entitlements are combined into one license metric result under one product result. Additionally, any installation can be licensed with the last one installation being unlicensed due to insufficient rights.

## With grouping and no consumption rules use case

In this use case, grouping is specified but there are no consumption rules that lead to a parent product result that shows the following outcomes:

![use case for grouping and no consumption rules](../image/usecase2.png)

In this scenario, the entitlement owner is recognized and reconciliation results are broken down. See there is a parent product result individual product results and license metric results for company A and company B. Note, however, that the five installs under the company A LMR might be any 5 installs since consumption is unrestricted. Same for company B. It will depends on the order of the devices processed which entitlement is used.

## Without grouping and with consumption rules use case

In this use case, no grouping is specified but consumption rules are specified that leads to a single product result that shows the following outcomes:

![use case for no grouping and consumption rules](../image/usecase3.png)

In this scenario, there’s a single product result but the entitlements can no longer be combined into one license metric result. Two license metric results are created that only company A and company B can consume from respectively. The company C installation is unlicensed.

## With grouping and with consumption rules use case

In this use case, both grouping and consumption rules are specified that lead to a parent product result that shows the following outcomes:

![use case with grouping and consumption rules](../image/usecase4.png)

In this scenario, consumption is restricted and the products results are broken down by company grouping. Company C also gets its own product result with no license metric result to show the unlicensed installation.

**Parent Topic:**[Grouping and consumption rules in reconciliation](grouping-consumptionrules.md)

