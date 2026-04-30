---
title: Approval Engine for Reserves and Payments
description: Insurance claims core includes a claim reserve and payment approval rules engine. It can be found in the decision table Claim reserve and payment approval rules.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Insurance Claims Core, Data Model, Learning and exploring, Financial Services Operations \(FSO\)]
---

# Approval Engine for Reserves and Payments

Insurance claims core includes a claim reserve and payment approval rules engine. It can be found in the decision table **Claim reserve and payment approval rules**.

This decision table is executed by two subflows:

-   Claim reserve approval flow
-   Claim payment approval flow

You can review these subflows by navigating to **All** &gt; **Process Automation** &gt; **Workflow Studio** &gt; **Subflows**.

The inputs to the decision table are:

-   Activity: Reserve/Payment
-   Product: The insurance product model
-   Amount: The amount being less then or greater than a set value

The output of the decision table is the title of the persona that can approve the amount.

## Approval engine properties

The reserve and payment approval process is controlled by the properties located at **All** &gt; **Insurance claim operations** &gt; **Properties**. For a detailed description of each property, see [Insurance Claims Core roles and properties](../reference/insurance-claims-core-roles-and-properties.md).

**Parent Topic:**[Insurance Claims Core](../reference/insurance-claims-core-data-model.md)

