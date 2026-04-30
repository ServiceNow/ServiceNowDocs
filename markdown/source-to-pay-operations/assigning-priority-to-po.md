---
title: Assigning priority to a purchase order
description: Purchase order exceptions are automatically assigned a priority level to indicate the most urgent issues.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [assign priority, exception priority, automatic priority assignment, impact, urgency]
breadcrumb: [Configure, Purchase Order Management, Source-to-Pay Operations, Finance and Supply Chain]
---

# Assigning priority to a purchase order

Purchase order exceptions are automatically assigned a priority level to indicate the most urgent issues.

Priority assignment calculation is done by using the **Set Impact and Urgency fields for Priority** business rule. A business rule is a server-side script that runs when a record is displayed, inserted, deleted, or when a table is queried. Admins can use business rules to change values in form fields automatically when the specified conditions are met.

Priority is calculated by using the time remaining to resolve the exception before the requested delivery date \(urgency\) and the supplier's proposed delivery deviation from the order request \(impact\).

The Priority field for purchase order exceptions can have one of the following values: Critical, High, Moderate, and Low.

As an admin, you can configure the **Set Impact and Urgency fields for Priority** business rule to fit your business practices. To calculate impact and urgency level automatically based on the product model and supplier, use this business rule to create your own advanced configurations.

**Parent Topic:**[Configure Purchase Order Management](configure-purch-order-mgmt.md)

**Related topics**  


[Install Purchase Order Management](../task/install-purch-order-mgmt.md)

[Assigning purchase order exceptions to buyers](assigning-po-exceptions-to-buyers.md)

[Domain separation and Purchase Order Management](domain-separation-pom.md)

