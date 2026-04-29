---
title: Create or edit a CI relationship
description: Use the relationship editor to view, create, or modify CI relationships. You can open the relationship editor from the CI Relations formatter.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [CI relationship editor, CI relationships in the CMDB, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Create or edit a CI relationship

Use the relationship editor to view, create, or modify CI relationships. You can open the relationship editor from the CI Relations formatter.

## About this task

As an alternative to the CI relationship editor, [Unified Map](../concept/cmdb-workspace-unified-map.md) in the [CMDB Workspace store app](../concept/cmdb-workspace.md)or in [Service Graph Workspace store app](../concept/sg-workspace.md) provides the latest functionality for editing CI relationships. For more information, see [Edit relationships in Unified Map](unified-map-edit-connection.md).

## Before you begin

Role required:

-   To create relationships: sn\_cmdb\_editor, asset, or itil
-   To view relationships, depending on the state of the Table API ACL:

    -   If inactive \(default\): sn\_cmdb\_editor, asset, or itil
    -   If active: sn\_cmdb\_editor, asset, or itil, and snc\_platform\_rest\_api\_access
    For more information, see [CI relationship security](../concept/c_CIRelationshipSecurity.md), [REST API](https://www.servicenow.com/docs/access?context=c_RESTAPI&version=australia&pubname=australia-api-reference&ft:locale=en-US), and [Table API](https://www.servicenow.com/docs/access?context=c_TableAPI&version=australia&pubname=australia-api-reference&ft:locale=en-US).


## About this task

The relationship editor operates differently, depending on whether you check the **Use suggested relationship** option or not.

## Procedure

1.  Launch the relationship editor:

    1.  Open a CI form.

        For example:

        1.  Navigate to **All** &gt; **Configuration** &gt; **CI Class Manager**.
        2.  On the CI Class Manager page, select **Open Hierarchy**.
        3.  On the CI Class panel search and select the class of the CI for which you want to create or edit relationships.
        4.  Select **CI List** in the left-side panel and then in the list view, select the CI.
    2.  On the CI form, scroll down as needed to select the Add CI relationship icon \(+ sign\) in the Related Items section.

2.  To use suggested relationships, first select a relationship type, and then select one or more CIs to be the child CIs in the relationship:

    ![Create a new relationship using suggested relationships.](../image/RelationshipEditorwithSuggestedRelationships.png)

    1.  Select **Use suggested relationship**.

    2.  From the **Suggested relationship type** list, select a relationship type.

        You can filter the list of suggested relationships by using the filter check boxes.

        |Filter option|Description|
        |-------------|-----------|
        |Hide CI relationship|Hides any relationships between the base CI and another CI \(such as "Receives data from"\). Default filter is stored in the ci\_manage\_relationships\_filter\_hint.cmdb\_ci user preference.|
        |Hide user relationship|Hides any relationships between the base CI and a user \(such as "Logs reviewed by"\). The default filter is stored in the ci\_manage\_relationships\_filter\_hint.sys\_user preference.|
        |Hide group relationship|Hides any relationships between the base CI and a group \(such as "Backups done by"\). Default filter is stored in the ci\_manage\_relationships\_filter\_hint.sys\_user\_group user preference.|

        The **Configurations Items** list displays all the CIs that are appropriate for the base CI and the selected relationship type. The **Relationships** list at the bottom of the editor, displays all existing relationships of the selected relationship type, in which the base CI is a parent CI or a child CI.

    3.  From the **Configuration Items** list, select one or more CIs as a second CI for the relationship.

        You can filter the list of **Configurations Items** by adding conditions in the **Filter** section and clicking **Run filter**.

        If you selected a parent relationship type, these CIs becomes the child CI in the relationship, and if you selected a child relationship type, then the selected CIs become the parent CI in the relationship.

    4.  In the **Relationships** section, click the plus icon \(+\) to add the new relationships.

        Alternatively, you can drag the selected CIs to the **Relationships** list. Each new relationship will consist of the base CI, the selected relationship type, and a selected second CI.

3.  To not use suggested relationships, first select one or more CIs to be the child CIs in the relationship, and then select the relationship type:

    ![Create a relationship without using suggested relationships.](../image/RelationshipEditornoSuggestedRelationships.png)

    1.  Clear **Use suggested relationship**.

    2.  In the **Configuration Items** list, select one or more CIs as a second CI for the relationship.

        You can filter the list of **Configurations Items** by adding conditions in the **Filter** area and clicking **Run filter**. Depending on the relationship type that you will select, the selected CIs might become a parent or a child CI in the relationship.

    3.  With at least one CI selected in the **Configuration Items** list, click the '+' sign in the **Downstream Relationships** section or the **Upstream Relationships** section to create the relationship.

        -   Add the relationship to **Downstream Relationships** to create a relationship in which the base CI is the parent CI and the selected CI is the child CI.
        -   Add the relationship to **Upstream Relationships** to create a relationship in which the base CI is the child CI and the selected CI is the parent CI.
    4.  For each newly created relationship in either the **Downstream Relationships** or the **Upstream Relationships** lists, click **Please select a relationship** and select a relationship type.

        -   The list of available relationship types in the **Downstream Relationships** list contains parent relationships only, in which the base CI is the parent CI.
        -   The list of available relationship types in the **Upstream Relationships** list contains child relationships only, in which the base CI is the child CI.
    5.  Click **Save** or **Save and Exit**.

        Only after you enter all the information that is necessary for creating the relationship, these buttons light up indicating that there are pending updates that require saving.


**Parent Topic:**[CI relationship editor](../concept/c_RelationshipEditor.md)

**Related topics**  


[Suggested class relationships](../reference/r_SuggestedRelationshipModel.md)

[CI relationships in the CMDB](../concept/c_CIRelationships.md)

[CI relationship security](../concept/c_CIRelationshipSecurity.md)

