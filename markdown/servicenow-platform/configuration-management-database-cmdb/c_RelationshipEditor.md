---
title: CI relationship editor
description: Use the relationship editor to view, create, modify, or delete CI relationships. Open the relationship editor from the CI Relations formatter.
locale: en-US
release: zurich
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [CI relationships in the CMDB, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# CI relationship editor

Use the relationship editor to view, create, modify, or delete CI relationships. Open the relationship editor from the CI Relations formatter.

As an alternative to the CI relationship editor, [Unified Map](cmdb-workspace-unified-map.md) in the [CMDB Workspace store app](cmdb-workspace.md) provides the latest functionality for editing CI relationships. For more information, see [Edit relationships in Unified Map](../task/unified-map-edit-connection.md).

When you use the relationship editor, the CI from which the editor was launched is designated as the base CI. You can then select one or more CIs as a second CI for the relationship. Depending on the selected relationship type, the base CI can become the parent CI or the child CI in the new relationship.

The relationship editor operates differently, depending on whether you select the **Use suggested relationship** check box.

-   With suggested relationships, the relationship editor lists all available relationship types for the base CI. To define a new relationship, select a relationship type, and then select a second CI for the relationship.

    Suggested relationships are highlighted for you. These relationships are displayed in blue with a prefix of \[Suggested\].

-   Without suggested relationships, you define a new relationship by first selecting a second CI for the relationship and then selecting a parent or a child relationship type.

**Note:** The following relationship types are used only for Service Mapping endpoints, and you cannot use them as a relationship type between two CIs:

-   **Implement End Point To:Implement End Point From**
-   **Use End Point To: Use End Point From**
-   **Applicative Flow To:Applicative Flow From**

## Suggested relationships

If you select the **Use suggested relationship** check box in the editor, the **Suggested relationship** list appears. It displays all available CI, user and group relationship types for the base CI. Relationship types have a suffix of **\(Parent\)** or **\(Child\)** to note the relationship descriptor, and suggested relationship types are displayed in blue and have a "\*" prefix.

When you select a relationship, you are also designating the base CI as being the parent or the child CI in the new relationship. For example, if you select the 'Feeds' relationship type, the base CI becomes the designated parent CI, and the second CI that you select becomes the child CI in this relationship.

## Downstream relationships

If you do not select the **Use suggested relationship** check box in the editor, the **Downstream relationships** list appears. It displays all relationships in which the base CI is the parent CI. The child CI of the relationship is displayed in the **Child** column.

## Upstream relationships

If you do not select the **Use suggested relationship** check box in the editor, the **Upstream relationships** list appears. It displays all relationships in which the base CI is the child CI. The parent CI in each relationship is displayed in the **Parent** column.

-   **[Create or edit a CI relationship](../task/t_CreateCIRelationship.md)**  
Use the relationship editor to view, create, or modify CI relationships. You can open the relationship editor from the CI Relations formatter.
-   **[Delete a CI relationship](../task/delete-ci-relationship.md)**  
Maintain the integrity of the CMDB by deleting any CI relationships that are no longer relevant or needed for a CI. Use the relationship editor to delete CI relationships.
-   **[Legacy CI relationship builder](../../../administer/form-administration/concept/c_CIRelationshipBuilder.md)**  
Used to define CI relationships manually, this page is a sophisticated version of the standard list collector. In the legacy CI relations formatter, click the CI relationship builder icon \(![CI relationship builder icon](../../../administer/form-administration/image/CIRelationshipBuilderIcon.png)\) to display the legacy Define Relationships page.

**Parent Topic:**[CI relationships in the CMDB](c_CIRelationships.md)

**Related topics**  


[Suggested class relationships](../reference/r_SuggestedRelationshipModel.md)

[Add a suggested relationship](../task/t_AddANewSuggestedRelationship.md)

[Relationship governance rules](relationship-governance.md)

[CI relations formatter](c_CIRelationsFormatterNG.md)

[Relation qualifier](c_RelationQualifier.md)

[CI relationship security](c_CIRelationshipSecurity.md)

[Create a CI relation rollup](../task/t_CreateACIRelationRollup.md)

[Add a suggested relationship](../task/t_AddANewSuggestedRelationship.md)

[Create or edit a CI relationship](../task/t_CreateCIRelationship.md)

[Legacy CI relationship builder](../../../administer/form-administration/concept/c_CIRelationshipBuilder.md)

