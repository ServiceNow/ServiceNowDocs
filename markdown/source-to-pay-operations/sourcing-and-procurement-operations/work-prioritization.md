---
title: Work prioritization
description: Priority is automatically assigned to purchase requisitions, sourcing requests, and procurement cases that your procurement specialists must work on, based on decisions configured by your administrators through decision tables.
locale: en-US
release: zurich
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Procurement Case Management, Explore, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Work prioritization

Priority is automatically assigned to purchase requisitions, sourcing requests, and procurement cases that your procurement specialists must work on, based on decisions configured by your administrators through decision tables.

This enables your procurement specialists to view their work, sorted by priority, and get started with the highest priority records first, followed by the ones that have lower priority. Procurement specialists can view this from the Procurement Specialist list page as well as from the transaction records on Platform.

This automatic assignment of priority is governed by these three decision tables:

-   Priority defaulting for Purchase Requisition: Defines the priority on purchase requisitions.​
-   Priority defaulting for Sourcing Request​: Defines the priority on sourcing requests.​
-   Priority defaulting for Procurement Cases​: Defines the priority on procurement cases.​

Your administrators can define the logic for defaulting priority in the above decision tables based on your organization's standardized policy of classifying requisitions, sourcing requests, and procurement cases as high, medium, and low priority. Some examples are dollar value of purchases, executive or leadership purchases, type of spend, and so on. This can be achieved by using any of the attributes available in the transaction header, lines, or even related records. They can configure the decision labels and answers on these decision tables based on your organizational requirements, which will in turn decide the priority of the purchase requisitions, sourcing requests, and procurement cases. By default, the priority is set to **5 - Planning**.

The priority logic is retriggered and priority is automatically reevaluated if any subsequent updates are made to the respective records​.

For information on how to work with decision tables, see [Decision Tables](https://www.servicenow.com/docs/access?context=decision-table&version=zurich&pubname=zurich-application-development&ft:locale=en-US).

**Parent Topic:**[Procurement Case Management](../concept/psd-overview.md)

