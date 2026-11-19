---
title: Approve contracts to allow amendments
description: Amendment requests can only be submitted for contracts in the Active state. If a contract is in Draft state and Awaiting Review substate, you need to manually approve it before submitting an amendment request.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/employee-service-management/contract-management-pro/cmpro-approve-draft-cntr.html
release: zurich
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2025-11-11"
reading_time_minutes: 1
breadcrumb: [Contract amendments, Use, Contract Management Pro, Legal and Contract Operations, Employee Service Management]
---

# Approve contracts to allow amendments

Amendment requests can only be submitted for contracts in the Active state. If a contract is in Draft state and Awaiting Review substate, you need to manually approve it before submitting an amendment request.

## Before you begin

Role required: sn\_lg\_cnt.contract\_fulfiller and contract manger

## Procedure

1.  Navigate to your workspace.

2.  Open the contract repository record that is in Draft state and Awaiting Review substate.

3.  Select **Approve Contract**.

    \[Omitted image "cmpro-amend-approve-cntr.png"\] Alt text: Contract in Draft state


## Result

The contract will move to either the Draft state-Approved substate or Active state based on its start date.

-   If the start date is in the future, the contract moves to the Draft state-Approved substate.
-   If the start date is today or in the past, the contract moves to the Active state.

**Parent Topic:**[Contract amendments](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/contract-management-pro/cmpro-amend-landing.md)

