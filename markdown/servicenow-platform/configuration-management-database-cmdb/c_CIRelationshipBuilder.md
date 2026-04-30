---
title: Legacy CI relationship builder
description: Used to define CI relationships manually, this page is a sophisticated version of the standard list collector. In the legacy CI relations formatter, click the CI relationship builder icon \( CI relationship builder icon \) to display the legacy Define Relationships page.
locale: en-US
release: xanadu
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [CI relationship editor, Relationships, Exploring CMDB, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Legacy CI relationship builder

Used to define CI relationships manually, this page is a sophisticated version of the standard list collector. In the legacy CI relations formatter, click the CI relationship builder icon \(![CI relationship builder icon](../image/CIRelationshipBuilderIcon.png)\) to display the legacy Define Relationships page.

For information about the latest CI relationship editor, see [CI relationship editor](../../../product/configuration-management/concept/c_RelationshipEditor.md).

## Select a CI relationship type

The top half of the legacy relationship editor contains a large option box that allows you to select which type of relationship you want to manipulate. Click the particular type of relationship you are interested in working with.

## Filter the list of CI relationships

In the legacy relationship editor, the check boxes along the right hand edge of the select box provide a quick way to filter down the list of available relationships.

By default, the system displays a list of all suggested relationships for the type of CI you selected. For example, if you selected a Database instance, a relationship of "Runs on" makes sense, but a relationship of "Provides HVAC for" does not. The default filter is stored in the user preferences ci\_manage\_relationships\_filter\_hint.cmdb\_cici\_manage\_relationships\_filter\_hint.sys\_user, and ci\_manage\_relationships\_filter\_hint.sys\_user\_group.

-   **Hide CI relationship** -- Hides any relationships between this CI and another CI \(e.g. "Receives data from"\).
-   **Hide user relationships** -- Hides any relationships between this CI and a user \(e.g. "Logs reviewed by"\).
-   **Hide group relationships** -- Hides any relationships between this CI and a group \(e.g. "Backups done by"\).
-   **Show all relationships** -- If you have the appropriate role \(out of the box this is itil\_admin\) you will have an additional check box labeled "Show all relationships." If you click that check box, the system will let you choose any relationship defined in the system, regardless of where it is on the "suggested" list for this type of CI.

## Select CI relationship targets

In the legacy relationship editor, users can link or unlink CIs for a relationship type.

As soon as you pick a relationship type, the system will fill in the two select boxes at the bottom of the screen with CI's that are appropriate for the relationship you suggested. The left hand select box will contain a list of CI's that might reasonably be linked via this relationship, while the right hand box contains a list of those CI's which are already linked.

1.  Link or unlink items.

<table id="table_vmy_dtb_m1b"><tbody><tr><td>

Link new items

</td><td>

Move that CI from the left hand box to the right hand box.

</td></tr><tr><td>

Unlink existing items

</td><td>

Move them from the right hand box to the left.

</td></tr></tbody>
</table>    When you make either type of change, a message appears indicating that you have pending changes.

2.  Apply or cancel your changes.

<table id="table_rjs_htb_m1b"><tbody><tr><td>

Click the Save button.

</td><td>

This will save your set of changes, and go back to the previous screen \(either a CI or the BSM map depending on how you got here\).

</td></tr><tr><td>

Click the Cancel button.

</td><td>

This causes you to exit without saving your changes.

</td></tr></tbody>
</table>
**Parent Topic:**[CI relationship editor](../../../product/configuration-management/concept/c_RelationshipEditor.md)

**Related topics**  


[CI relationships in the CMDB](../../../product/configuration-management/concept/c_CIRelationships.md)

