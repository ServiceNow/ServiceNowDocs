---
title: Composite Fields
description: A composite field combines information from two fields in a table to form a single field.
locale: en-US
release: yokohama
product: Demand Management
classification: demand-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Reference, Demand Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Composite Fields

A composite field combines information from two fields in a table to form a single field.

For example, the **Task** field on the Project Tasks list displays the short description and the project task number. The short description appears above the project task number. The project task number appears and is a link to the Project Task form.

![Composite field](../../project-management/image/CompositeField.png "Composite field")

## Use a composite field

-   Editing a composite field changes the short description. Editing the short description changes the composite field.
-   Sorting on a composite field is based only on the short description and not the number.
-   Searching on a composite field is enabled for both the short description and the number:
    -   To search by the number using the list header, enter an asterisk \(\*\) before the search term. For example, \*PRJTASK0010016.
    -   To search by the number using the filter, create a condition similar to: \[Task\] \[contains\] \[PRJTASK0010016\].

**Parent Topic:**[Demand Management reference](../../service-portfolio-management2/concept/demand-management-reference.md)

