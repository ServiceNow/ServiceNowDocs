---
title: Entity class rule filter fields
description: You can create an entity class rule filter by filling out the fields that display after you click the New option in the entity class rule filters related list.
locale: en-US
release: zurich
product: GRC Common Functions
classification: grc-common-functions
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Create an entity class rule filter, Entity class rules, Explore entities, Common GRC features, Governance, Risk, and Compliance]
---

# Entity class rule filter fields

You can create an entity class rule filter by filling out the fields that display after you click the **New** option in the entity class rule filters related list.

<table id="table_fjl_gnh_g5b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Table

</td><td>

Table that is auto-filled from the associated entity class rule.

</td></tr><tr><td>

Subclass

</td><td>

Entity class to be applied for all the entities whose source record matches the class rule filter.

</td></tr><tr><td>

Filter condition

</td><td>

Condition that can filter out the records from the table. The entity class that is specified in the subclass may be applied \(as per the class assignment rules\) to the entity that is associated to any of these records.

</td></tr><tr><td>

Filter priority

</td><td>

Filter priority. If a source record of an entity satisfies a multiple class rule filters condition, the class is picked from the filter with the lowest priority.

 For example, if you have two subclass applications and departments that have priority 0 and 1, respectively, the application subclass that has the lower priority is auto-filled in the rule and control form.

</td></tr></tbody>
</table>**Parent Topic:**[Create an entity class rule filter](../task/create-new-entity-class-rule-filter.md)

