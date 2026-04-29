---
title: Approximated lifecycle and lifecycle code
description: Leverage the expanded lifecycle coverage for hardware and consumable models available in the ServiceNow Content library portal when explicit dates from the manufacturer aren’t available. Hardware models with approximated lifecycle dates contain a lifecycle code that indicates the dates are approximate.
locale: en-US
release: australia
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Exploring Hardware Asset Management, Hardware Asset Management, IT Asset Management]
---

# Approximated lifecycle and lifecycle code

Leverage the expanded lifecycle coverage for hardware and consumable models available in the ServiceNow® Content library portal when explicit dates from the manufacturer aren’t available. Hardware models with approximated lifecycle dates contain a lifecycle code that indicates the dates are approximate.

When manufacturers don’t publish official life cycle dates for certain hardware models and consumables, the  ServiceNow® Content Service generates approximated life cycle dates. The approximated lifecycle dates are derived using data-driven approximation logic to determine the most likely life cycle phase dates for the hardware and consumable models.

The estimated life cycle dates are categorized using specific lifecycle codes. These codes indicate that the lifecycle dates aren’t the explicit dates published by the manufacturer. When lifecycle dates are unavailable for any models, codes such as Exception Codes \(EXC\) and End-of-Phase Codes \(END\) are assigned to those models. These codes provide clarification regarding the absence of these dates.

The Hardware Lifecycle code \[sn\_ itam\_common\_lifecycle\_code\] table stores the approximation codes and its description for the lifecycle records that are curated through approximation logic. For a detailed explanation of lifecycle codes, see [https://support.servicenow.com/kb?id=kb\_article\_view&amp;sysparm\_article=KB2726382](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2726382).

The Lifecycle code column in the Hardware Lifecycle Definition \[sn\_hamp\_lifecycle\_definition\] table indicates the approximate code for a model's lifecycle. This column references the Lifecycle code column in the Hardware Lifecycle Code \[sn\_hamp\_lifecycle\_code\] table.

## Load approximated lifecycle date for hardware and consumable models

The scheduled job **HAM – Hardware Life cycles** retrieves the life cycles date that is published by the ServiceNow Content Service and loads them into the following tables:

-   cmdb\_hardware\_model\_lifecycle \(for hardware models\)
-   cmdb\_consumable\_model\_lifecycle \(for consumable models\)

The system property **approximate\_dates\_in\_hw\_lifecycle** determines whether only manufacturer-provided actual dates or both actual and approximated dates are loaded into the hardware and consumable life cycle tables. The default value of the system property **approximate\_dates\_in\_hw\_lifecycle** is **True**.

-   If this property is set to **False**, only the actual life cycles from the manufacturer are loaded into the hardware and consumable life cycle tables.
-   If it is set to **True**, both actual and approximated life cycles are loaded into the hardware and consumable life cycle tables.

## Identifying models with approximated lifecycle dates

In both the Hardware Model Lifecycles \[cmdb\_hardware\_model\_lifecycle\] and Consumable Model Lifecycles \[cmdb\_consumable\_model\_lifecycle\] tables, as well as in the Model management view within the Hardware Asset Workspace, the Lifecycle code column indicates if the model’s lifecycle phase and dates have been approximated.

-   If the Lifecycle code column contains a value, the model's lifecycle phase and dates are based on an approximated lifecycle code.
-   If the Lifecycle code column is empty, the model's lifecycle dates are confirmed or explicit dates published by the manufacturer.
-   If the Lifecycle code column contains a value, and the model's lifecycle phase and dates are empty, the Lifecycle code column indicates the reason for the absence of these dates.

**Note:** When manually adding a new lifecycle record, such as a custom lifecycle or calculated lifecycle, you can't add a lifecycle code value. The lifecycle code is only available for lifecycle records that come directly from the ServiceNow Content Service and can’t be set for the user created lifecycle records.

