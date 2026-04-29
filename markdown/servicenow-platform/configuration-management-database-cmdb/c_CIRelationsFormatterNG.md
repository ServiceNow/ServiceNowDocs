---
title: CI relations formatter
description: The default CI form includes a CI relations formatter from which you can examine a CI and its relationships in various views. From the CI relations formatter, you can also launch the CI relationship editor for the CI.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [CI relationships in the CMDB, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# CI relations formatter

The default CI form includes a CI relations formatter from which you can examine a CI and its relationships in various views. From the CI relations formatter, you can also launch the CI relationship editor for the CI.

If the domain separation plugin is activated, then only relationships in which the logged on user is authorized to view both CIs, are displayed.

The CI relations formatter contains a list of related CIs and a toolbar with controls for viewing the relationships between the current CI and related CIs. You can configure the controls in this formatter to modify varying aspects of the view. For more information about formatters, see [Create a formatter and add it to the form](https://www.servicenow.com/docs/access?context=t_CreateAFormatter&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

**Note:**

-   If an endpoint is a child in one relationship and the same endpoint is a parent in another relationship, then that endpoint is hidden and does not appear in the relations formatter view. Similarly, relationship qualifier chains are also hidden and do not appear in the relationship formatter view.
    -   Example: CI1 &gt; endpoint &gt; CI2

        In this example, CI1 is related to CI2 through relationships with endpoint. A single relationship appears in the relations formatter:

        CI1 &gt; CI2 \(These relationships appear as a direct relationship without endpoint, because endpoint is a parent in one relationship and a child in another relationship\).

    -   Example: CI1 &gt; endpoint1 &gt; CI2 &gt; endpoint2

        Two relationships appear in the relations formatter:

        CI1 &gt; CI2 \(endpoint1 is hidden because it is a parent in one relationship and a child in another relationship\).

        CI1 &gt; CI2 &gt; endpoint2 \(appears as level 2 relationship – endpoint1 is hidden and endpoint2 appears as it a child and not a parent in any other relationship\).

-   On instances that do not meet the internet browser requirements for the CI relations formatter, the default CI form includes the legacy CI relations formatter instead. For more information, see [Legacy CI relations formatter](../../../administer/form-administration/reference/r_LegacyCIRelationsFormatter.md).
-   CIs not extended from the Configuration Item \[cmdb\_ci\] table, are not displayed in Dependency Views maps and in CI relation formatters.
-   The **Applicative Flow To::Application Flow From** relationship is a special relationship type used only between Service Mapping endpoints. This relationship type is not intended for use in the CMDB as a relationship between CIs and therefore it is not displayed in the relations formatter.

<table id="table_v4g_n21_1s"><thead><tr><th>

Control

</th><th>

Definition

</th></tr></thead><tbody><tr><td>

Add CI relationship

</td><td>

Starts the relationship editor to manually create CI relationships. For more information \(including about roles required for the '+' control to appear\), see [Create or edit a CI relationship](../task/t_CreateCIRelationship.md).

</td></tr><tr><td>

Show dependency views

</td><td>

Launches a Dependency Views map in another window or tab. The CI is the central node in the map, with a configurable number of levels above and below that node in the hierarchy. Map indicators next to the nodes indicate the number of tasks, incidents, problems, changes, or outages related to that node. Right-click to expand collapsed nodes or display a list of related tasks or problems. For more information, see [Dependency Views map](../../business-service-management-map-ng/concept/c_NextGenBSMMaps.md).

</td></tr><tr><td>

Search for CI

</td><td>

Filters the CIs included in the display.

</td></tr></tbody>
</table>Select the Settings icon to configure additional view settings that filter the data displayed. Settings are preserved through logging out and logging back in.

<table id="table_zsl_qw4_ms"><thead><tr><th>

Setting

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Show Relations in Flat/Tree Layout

</td><td>

To view a flat list of related CIs that are grouped by relationship type in alphabetical order, click **Flat** \(default value\).

 To view groups of related CIs in a hierarchical tree, click**Tree**. If you select the tree view, you cannot configure any other settings for viewing related CIs. A single list of upstream and downstream relationships is displayed.

</td></tr><tr><td>

Show Relations in Split/Merge Layout

</td><td>

To view a single list that includes both upstream and downstream relationships, click **Merge** \(default value\). Relationships are grouped by relationship type.

 To view separate lists for upstream and downstream relationships, click **Split**.

</td></tr><tr><td>

Filter Relations by Max Level

</td><td>

Select the number of downstream and upstream levels in the hierarchy to include when displaying CIs in a flat view.

 Default value is 3.

</td></tr><tr><td>

Filter Relations by Relationship Type

</td><td>

Select the types of relationships to view.

 Default value is 'All Relationship Types'.

</td></tr><tr><td>

Filter Relations by CMDB View

</td><td>

Filter by tables specified in CMDB views, if any relationship filters exist.

</td></tr></tbody>
</table>The relations formatter uses the following icons to provide additional information about changes, problems, and outages related to CIs in the relationship:

|Icon|
|----|
|Recently closed changes|
|Planned changes|
|Currently open changes|
|Recently closed outages|
|Problems|
|Incidents|
|Planned outages|
|Currently open outages|

In large networks, a list of related CIs might be excessively long, which can slow performance when a CI form is rendered. You can configure these properties to control the amount of data that is displayed. To find a property, enter `sys_properties.list` in the left navigation filter and search for the property.

<table id="table_z34_syd_5s"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

glide.ecmdb.find\_relationship\_issues

</td><td>

Hides or displays an icon in the CI relations formatter that links to open issues for the CI. This property defaults to true \(displays the icon\).

</td></tr><tr><td>

glide.ui.max\_relation\_levels

</td><td>

Specifies the maximum level for displaying CIs in flat view before reaching the maximum relations limit. The default value is 5.

</td></tr><tr><td>

glide.ui.max\_relations

</td><td>

Specifies the maximum number of related CIs to display.

 When exceeded:

-   A notification appears indicating that the limit has been reached, and that not all relations are displayed. The default value is 1000.
-   Flat layout reverts to the tree layout view.

</td></tr></tbody>
</table>-   **[Domain separation](domain-separation-relationship-formatter-editor.md)**  
Domain separation is supported in the relations formatter and the CI relationship editor. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
-   **[Create or edit a relationship filter](../task/t_CreateRelationshipFilter.md)**  
Create a custom relationship filter to display CI relationships from selected tables in the CI relations formatter.
-   **[Exclude relationships from the relations formatter view](../task/exclude-relationship.md)**  
Create a list of relationships that should not appear in the relations formatter view on CI forms.
-   **[Legacy CI relations formatter](../../../administer/form-administration/reference/r_LegacyCIRelationsFormatter.md)**  
On instances that do not meet the internet browser requirements for the latest CI relations formatter, the default CI form includes the legacy CI relations formatter instead.

**Parent Topic:**[CI relationships in the CMDB](c_CIRelationships.md)

**Related topics**  


[Suggested class relationships](../reference/r_SuggestedRelationshipModel.md)

[Add a suggested relationship](../task/t_AddANewSuggestedRelationship.md)

[Relationship governance rules](relationship-governance.md)

[CI relationship editor](c_RelationshipEditor.md)

[Relation qualifier](c_RelationQualifier.md)

[CI relationship security](c_CIRelationshipSecurity.md)

[Create a CI relation rollup](../task/t_CreateACIRelationRollup.md)

[Create a formatter and add it to the form](https://www.servicenow.com/docs/access?context=t_CreateAFormatter&version=australia&pubname=australia-platform-administration&ft:locale=en-US)

[Create or edit a relationship filter](../task/t_CreateRelationshipFilter.md)

