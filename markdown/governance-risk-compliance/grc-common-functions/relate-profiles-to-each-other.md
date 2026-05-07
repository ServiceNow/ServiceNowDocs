---
title: Relate entities to each other
description: Create relationships between entities to understand how controls and risks affect each other and how they affect the enterprise.
locale: en-US
release: australia
product: GRC Common Functions
classification: grc-common-functions
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Entity scoping, Explore entities, Common GRC features, Governance, Risk, and Compliance]
---

# Relate entities to each other

Create relationships between entities to understand how controls and risks affect each other and how they affect the enterprise.

## Before you begin

Role required:

-   sn\_compliance.admin or sn\_compliance.manager
-   sn\_risk.admin or sn\_risk.manager
-   sn\_audit.admin or sn\_audit.manager

## Procedure

1.  Navigate using any of these options.

    -   **Policy and Compliance** &gt; **Scoping** &gt; **All Entities**.
    -   **Risk** &gt; **Scoping** &gt; **All Entities**.
    -   **Audit** &gt; **Scoping** &gt; **All Entities**.
2.  Open the entity record from the list.

3.  Perform one of the following actions.

<table id="choicetable_cyx_ljg_lw"><tbody><tr><td id="d294566e128">

**To specify that the current entity is downstream of another entity**

</td><td>

Click the **Add** button in the **Upstream entities** related list.

</td></tr><tr><td id="d294566e143">

**To specify that the current entity is upstream of another entity**

</td><td>

Click the **Add** button in the **Downstream entities** related list.

</td></tr></tbody>
</table>4.  Select the desired entities to relate the current entity to and click **Create Relationship**.


## Result

The entities displayed after clicking **Add** on the **Upstream entities** or **Downstream entities** related lists are limited based on the current entity's class and the tier it belongs to.

**Note:** If there are no eligible entities which can be related to the current entity, then the **Add** button is not displayed on the **Upstream entities** or **Downstream entities** related lists.

**Parent Topic:**[Entity scoping in GRC](../concept/c_Scoping.md)

