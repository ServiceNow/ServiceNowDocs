---
title: Traversal Rules for Application Services form completion
description: To edit an existing CI relationship or add a new CI relationship during the tag-based discovery process, complete the Traversal Rules for Application Services form.
locale: en-US
release: australia
product: Service Mapping
classification: service-mapping
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Service Mapping reference, Service Mapping, ITOM Visibility, IT Operations Management]
---

# Traversal Rules for Application Services form completion

To edit an existing CI relationship or add a new CI relationship during the tag-based discovery process, complete the Traversal Rules for Application Services form.

<table id="table_ulz_55t_wlb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Rule Definition

</td><td>

To create a new CI relationship:

1.  Select **New**.
2.  Select the Lookup using list icon ![](../../event-management/image/LookupUsingList.png) and to view the available CI Relationship Type Rule Definitions.

Continue as follows, depending on your situation:

    -   If you see a CI relationship that you want to use:
        1.  Select that relationship.
        2.  Select **Submit**. The new CI relationship is added to the CI Relationship Type Rule Definitions \[cmdb\_rel\_type\_rule\_definitions\_list\] table.
    -   If you don’t see the desired CI relationship:
        1.  Select **New** in the CI Relationship Type Rule Definitions window.
        2.  Select the CI Class from the **Parent Type** list.
        3.  Begin entering the relationship in the **Relationship Type** field and select the appropriate relationship type from the list.
        4.  Select the CI Class from the **Child Type** list.
        5.  Select **Submit**.
        6.  Select **Submit** on the Traversal Rules for Application Services - New Record form. The new CI relationship is added to the CI Relationship Type Rule Definitions \[cmdb\_rel\_type\_rule\_definitions\_list\] table.

 To edit a preconfigured CI relationship:

1.  Select the preconfigured CI relationship in the **Parent Type** column.
2.  Select the Preview this record icon ![](../image/preview-connection-suggestion-icon.png), then select Open Record.
3.  Modify the **Parent Type**, **Relationship Type**, or **Child Type** as needed.
4.  Select **Update**.

 For example, to discover Linux servers hosting storage devices, select the following values:

-   Parent Type: Linux Server \[cmdb\_ci\_linux\_server\]
-   Relationship Type: Contains::Contained by
-   Child Type: Storage Device \[cmdb\_ci\_storage\_device\]

</td></tr><tr><td>

Is reverse

</td><td>

Select this check box to traverse a CI relationship starting from the child CI instead of the parent CI.Using the previous example, select this check box to begin with the storage devices and find the Linux servers that host these specific storage devices.

</td></tr><tr><td>

Used By

</td><td>

Select only **Service by Tags**.**Note:** Don’t select **Service Recomputation**. This selection helps prevent editing any existing traversal rules or adding new ones and produces an error message.

</td></tr><tr><td>

Active

</td><td>

Select this check box to use this traversal rule in the tag-based discovery.Alternatively, clear this check box to exclude this traversal rule from the tag-based discovery.

 **Note:** By default, you can have only five traversal rules participating in tag-based discovery. To change the maximum number of traversal rules, edit the value for the svc\_by\_tags.max.traversal.rules.active property in the System Property \[sys\_properties\] table.

</td></tr><tr><td>

Order

</td><td>

Enter a number for the order. The system uses traversal rules for discovery in sequence from low order to high.**Note:** When configuring traversal rules with dependencies, verify that prerequisite rules are executed before dependent ones by assigning them a lower-order number.

</td></tr></tbody>
</table>**Parent Topic:**[Service Mapping reference](service-mapping-reference.md)

