---
title: Amendment and renewal interactions
description: Understand how amendment and renewal requests interact on the same contract, and the messages that guide you when they occur in sequence or in parallel.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/contract-management-pro/cncore-amend-renewal-int.html
release: brazil
product: Contract Management Pro
classification: contract-management-pro
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 2
keywords: [Amendment and renewal, Renewal interactions, Hierarchy boundary, Overlapping contracts]
breadcrumb: [Contract renewals, Use, Contract Management Pro, Legal and Contract Operations, Employee Service Management]
---

# Amendment and renewal interactions

Understand how amendment and renewal requests interact on the same contract, and the messages that guide you when they occur in sequence or in parallel.

## Hierarchy

When a renewal request is linked to a previous contract, the renewal does not inherit the previous contract's parent-child hierarchy or related-contract family structure. The renewed contract is a new contract connected to the previous one through the renewal link, not a child of it.

## Amendment and renewal in sequence

When an amendment and a renewal happen one after the other on the same contract, the contract record shows messages that reflect the current situation:

-   When an amendment is completed first and a renewal is initiated later, the contract shows that the amendment is applied, and then that a renewal is in progress. When the renewal is executed, the contract shows that it has been renewed as the new contract.
-   When a renewal is completed first and an amendment is initiated later, a new renewed contract already exists. Before submitting the amendment, you are warned to review dates and terms for overlap between the amended contract and the renewed contract, and to correct them manually if needed. You can still proceed, and the warning is also shown on the amendment request.

## Amendment and renewal in parallel

An amendment and a renewal can be in progress at the same time on the same contract. When you submit one while the other is in progress, both the amendment request and the renewal request show a warning to check dates and terms for overlap and to reconcile them manually if needed. Both requests can proceed and be executed. When one request completes while the other is still in progress, the contract stops showing the parallel message and shows the sequential message that applies.

When both requests are active on the same contract, review the following to avoid conflicts:

-   Contract dates to prevent overlapping effective periods between the amended contract and the renewed contract
-   Terms and pricing changes in both requests
-   Effective dates and expiration dates

You must manually reconcile any conflicts between the amended original contract and the renewed contract.

**Parent Topic:**[Contract renewals](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/contract-management-pro/cmpro-renewal-landing.md)

**Related topics**  


[Work on a renewal request]()

[View renewal details]()

