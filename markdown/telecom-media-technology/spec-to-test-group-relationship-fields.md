---
title: Specification to Test Group Relationship form fields
description: Review the fields on the Specification To Test Group Relationship form and the rules that govern which combinations the system saves.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/telecom-media-technology/spec-to-test-group-relationship-fields.html
release: australia
topic_type: reference
last_updated: "2026-10-13"
reading_time_minutes: 1
keywords: [specification to test group relationship, product model, product inventory table, conditions]
breadcrumb: [Reference, Service Test Management, Telecommunications, Media, and Technology \(TMT\)]
---

# Specification to Test Group Relationship form fields

Review the fields on the Specification To Test Group Relationship form and the rules that govern which combinations the system saves.

To create a relationship, see [Associate a test group to a specifications or product model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/define-relationship-test-group-specifications.md). A relationship can be created only for a published test group.

<table id="table_gcm_vrp_qbc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Specification

</td><td>

Name of the specification.**Note:** Provide either a specification or a product model. The system doesn't save a relationship that has both a specification and a product model, or neither.

</td></tr><tr><td>

Product model

</td><td>

Name of the inventory.**Note:** Provide either a specification or a product model. The system doesn't save a relationship that has both a specification and a product model, or neither.

</td></tr><tr><td>

Product inventory table

</td><td>

Table that contains the product inventory records that the conditions apply to. This field appears after you select a specification, and only when the Product Inventory plugin is active.

</td></tr><tr><td>

Conditions

</td><td>

Conditions that a product inventory record must meet for the test group to apply. You can't set conditions when you select a product model. Conditions are available only when the Product Inventory plugin is active. For details, see [Define conditions for a test group relationship](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/define-conditions-for-test-group-relationship.md).

</td></tr><tr><td>

Test Group

</td><td>

Auto-populated name of the test group for which you’re specifying a relationship.

</td></tr></tbody>
</table>## Rules

-   Provide exactly one of **Specification** or **Product model**. The system doesn't save a relationship that has both or neither.
-   Without the Product Model plugin, a product model is required.
-   You can't set conditions together with a product model.
-   The same test group and specification, or the same test group and product model, can't be related twice. With the Product Inventory plugin, relationships that differ by conditions or by product inventory table count as different.

