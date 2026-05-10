---
title: Manage CI details using CI Form in CMDB Workspace
description: Use CI Form in CMDB Workspace or in another workspace, to view, edit, and manage a comprehensive set of details of a CI such as its attributes, related lists, and CMDB 360 records. When updating CIs, IRE rules are applied to avoid potential issues such as duplicate CIs. CI Form supports derivation of form configurations throughout the CMDB hierarchy.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 17
breadcrumb: [CMDB Workspace, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Manage CI details using CI Form in CMDB Workspace

Use CI Form in CMDB Workspace or in another workspace, to view, edit, and manage a comprehensive set of details of a CI such as its attributes, related lists, and CMDB 360 records. When updating CIs, IRE rules are applied to avoid potential issues such as duplicate CIs. CI Form supports derivation of form configurations throughout the CMDB hierarchy.

The CI Form feature is a centralized location with a comprehensive set of CI details, organized in sections. Anywhere CMDB Workspace provides a function to view a CI record, such as a list or a chart, CI Form is used for the selected CI when you select that function. Use the forms provided by CI Form to examine and edit CI attributes, relationships, tags, services and offerings, CMDB Health and CMDB 360 data associated with the CI, related lists, and activities.

General operations you can perform in CI Form:

-   Select the Now Assist for CMDB CI Summarization skill: Requires that Now Assist for CMDB is set up. For more information, see [Configure the CI summarization skill](../task/now-assist-cmdb-config-ci-summary.md).
-   Select **Open map** to open the CI map in [Unified Map](cmdb-workspace-unified-map.md). This function isn't available for a non-operational CI. For information about using the **Life cycle stage** attribute to define a CI's operational state, see [Configure CIs to appear based on life cycle stage value](../task/unified-map-confg-operational-state.md).

In general, a CMDB Admin and a CMDB Editor can view and edit CI records, and a CMDB User can view CI details on the form.

## Explore CI view

By default, CI Form uses the Explore CI view, which is stored in the UI Views \[sys\_ui\_view\] table. The Explore CI view defines the structure of the view, its sections and attributes, and related lists that appear on the form. The system provides predefined Explore CI forms for many CMDB classes. Those forms are derived by child classes, which don't have their own form definition, throughout the CMDB hierarchy.

The various sections in Explore CI view are described in this topic.

## Configuration

You can control the use and content of CI Form as follows:

-   Set system property **sn\_cmdb\_ws.explore\_ci.record.enabled**:

    This property toggles the use of CI Form when viewing CI records in CMDB Workspace, or in another workspace, if applicable. This property is set to **true** by default, enabling the experience of CI Form. For more information about this property, see [Components installed with CMDB Workspace](../reference/installed-with-cmdb-workspace.md).

-   Configure the Explore CI view:

    Select the More Actions icon \(...\) on the form and then select an option to modify the Explore CI view:

    -   Select **Configure attributes** to modify the Summary and Attributes sections on the form, in Form Builder. For example, to add sections, modify section titles or the attributes included in sections: Requires the personalize\_form user role.

        For more information about Form Builder and Table Builder, see [Forms in Table Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/form-builder-glide-family-release/form-view-configuration.md) and [Add fields to a form layout in Table Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/form-builder-glide-family-release/add-form-fields.md).

    -   Select **Configure resources** to modify the Resources section on the form. For example, to add or remove subsections or items within subsections: Requires the personalize\_list user role.

## Highlighted attributes

Several key attributes are preconfigured to be highlighted on a CI form when specific conditions are met. Those highlights are meant to draw your attention to specific states, which are either healthy, or that indicate a problem and require your attention. Attribute highlight definitions are stored in the Highlighted Values \[sys\_highlighted\_value\] ServiceNow AI Platform table, which you can search for records where **Table** is prefixed by 'cmdb\_ci'. For example, the **operational\_ status** attribute is configured as follows:

-   If the attribute value is '**Operational**', then the attribute appears with a green highlight.
-   If the attribute value is anything other than '**Operational**', then the highlight is red.

To see those preconfigured highlight records that are used in CI Form and in various other CMDB Workspace features, navigate to **All** &gt; **Workspace Experience** &gt; **Administration** &gt; **Highlighted Values**.

For more information about configuring attribute highlights in the ServiceNow AI Platform, see [Highlight list fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/highlight-list-fields-platform.md).

## Summary

By default, the Summary tile shows the most meaningful CI attributes and appears at the top of all other form sections. You can select **Show more** or **Show less** to adjust the page layout. The Summary tile shows attributes such as **Created**, key ownership attributes such as **Managed by**, and other important attributes such as **Discovery source** and **Operational status**. The attributes that appear in this section map to the first section defined in the Explore CI view.

By default, the Important attributes tile shows CI attributes such as **Operating System** and **Serial number**. The attributes that appear in this tile map to the **Important attributes** section defined in the Explore CI view, if one exists.

Role requirements for operations in this section:

-   Editing attributes by selecting the Edit icon: Permitted for attributes that you have permission to
-   Modifying this section in the Explore CI view: personalize\_form

## Attributes

This section shows all the UI sections that are configured in the Explore CI view for the class, excluding:

-   The first section \(which populates the Summary tile\).
-   The Important attributes section, if one exists \(which populates the Important attributes tile\).

Select **Attributes** to access the subsections within. By default, the Discovery and the Operational attribute subsections map to the Discovery and the Operational sections in the Explore CI view. The All subsection shows all the CI attributes. Mandatory attributes are noted on the form by an "\*" and must be set with a value.

When updating CI attributes, any Identification and Reconciliation Engine \(IRE\) rules that exist for the CI class are applied to help prevent potential problems with the update. IRE processes detect potential issues such as CI duplication and a dependent CI missing valid parent relationships. In these situations, the update is paused and you're presented with mitigation options to avoid the issue. Applying IRE processes might result in a partial update of attributes as reconciliation rules might block updates to some attributes and enable updates of others.

If there are no IRE rules for the class, the CI is updated directly without using IRE processes.

A CI that is updated in CI Form, has its **discovery\_source** attribute set to **Manual via IRE** unless you set it to a different value.

More information:

-   [Identification and Reconciliation Engine \(IRE\)](ire.md)
-   [Reconciliation rules](../reference/r_ReconciliationRulesPrinciples.md)
-   [Identification rules](c_IdentificationRules.md)
-   [Mandatory attributes](../task/t_SetCIFieldMandatory.md)

Role requirements for operations in this section:

-   Updating attributes: sn\_cmdb\_editor
-   Modifying this section in the Explore CI view: personalize\_form

## Tags

This section shows the list of tags, stored as key/value pairs in the Key Values \[cmdb\_key\_value\] table. These tags are typically associated with CIs and resources for cloud providers such as Amazon Web Services and Google Cloud Platform, and in general are referred to as cloud tags. Cloud tags are used in ITOM applications, such as Tag Governance, and function as key dependencies in Tag-based discovery in Service Mapping. Discovery and Service Graph Connectors automatically populate cloud tags, which can then be grouped and managed as needed in an organization.

The Tags section in CI Form doesn't contain details about Platform tags, which are another type of tags that are stored in the **Tags** column that exists in most platform tables.

To manage tags, select **Manage** in the Tags tile, and then, in the Manage tags dialog box you can:

-   Enter a **Key** and a **Value** pair, and then select the Add new tag \('+'\) icon.
-   Select the Delete tag icon for a tag.
-   Modify the **Key** or the **Value** fields for a tag.
-   Select **Save** to save any changes to tags.

Managing tags requires the sn\_cmdb\_editor user role.

More information:

-   [Tag-based discovery in Service Mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-mapping/tag-based-mapping.md)
-   [Data collected for Amazon AWS Cloud Discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/itom-visibility/cloud-disco-aws-data-collected.md)
-   [Data collected for Microsoft Azure Cloud Discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/itom-visibility/data-collected-azure-discovery.md)

## Resources

This section shows resources linked to the CI, and maps to the Related Lists specified in the Explore CI view. By default, resources include tables such as File Systems \[cmdb\_ci\_file\_system\], Software Installed \[cmdb\_ci\_spkg\], and Network Adapters \[cmdb\_ci\_network\_adapter\].

In this section, you can:

-   Select **Manage** to add or remove records from a resource list, which is applicable to related lists that have many-to-many relationships. If you're authorized to update in the CMDB Workspace scope, then you're navigated to a list selector for the resource where you can add or remove multiple items. If you aren't authorized, then you're navigated to the Core UI experience.

-   Select one or more related items and then select the **Delete** button, which is visible only if you have delete access to any of the related list tables.
-   Select **New** to add a related list item. The **New** button is available for all the resource tables that you have access to.

    Important notes about creating a new related list item:

    -   If the related list table is within the cmdb\_ci hierarchy, has an IRE identification rule, and isn't an excluded table, then you're navigated to the Create CI experience in CMDB Workspace or another workspace if applicable. In the Create CI experience, some CI attributes are pre-populated with the proper values for the class. For example, in the Required attributes section for dependent CIs, the **Dependent-upon CI** attribute is pre-populated with the parent of the current CI. Relationships and resources are also pre-populated according to the CI class definitions.

        For information about the Create CI experience, see [Create a CI manually in CMDB Workspace](../task/create-ci-manual-cmdb-workspace.md).

    -   If the related list table doesn't have an IRE identification rule, then you're navigated to a basic list view page instead of CI Form.
    -   The system automatically creates the matching reference back to the current class. For example, for a dependent CI the system creates the file system and the necessary relationship to connect the file system to the computer CI.
    -   For some resources such as CI IPs, **New** isn't available and the **Dependent-upon CI** isn't pre-populated. This behavior applies to CIs with scripted relationships.
    -   After creating a new related list item, select the Refresh List icon to show the new record in the list on the Resource section.
-   Configure the Resources section in the Explore CI view by selecting the More actions icon and then selecting **Configure resources**. Use the related lists slushbucket to add or remove resources and then select **Save**: Requires the personalize\_list role.

Role requirements for operations in this section:

-   Configuring resources in the Explore CI view: personalize\_list
-   Creating, updating, or deleting records in related tables included as Resources for a CI record: Requires create, update, and delete access to the resource table.

## Activity

This section shows related items such as open incidents and the activity stream for the CI on the following tabs:

-   **Related items**

    Pie charts that by default include Open incidents \(Incidents table\), Open changes \(Change Request table\), and Open problems \(Problem table\), broken down by priority or state.

    In this tab, you can:

    -   Select a chart to drill down to the records associated with different chart sections. Depending on configuration, records open in CMDB Workspace or in another workspace.
    -   Configure the list of tables for which charts appear, which is stored in the Explore CI Related Item Configurations \[sn\_cmdb\_ws\_explore\_ci\_related\_item\_config\] table. You can add records to that table, or modify behavior settings such as where a record opens when selected: Requires the sn\_cmdb\_ws.config\_editor role.
    -   Configure your preferences for which of the available charts appear when you log in. Select the Related Item Settings icon in the Related Items tab and in the Related item settings dialog box, select any charts that you prefer to hide.
-   **CI history**

    History of the activities related to the CI, such as value changes in the CI attributes, listed in chronological order.


More information:

-   [Problem Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/problem-management/c_ProblemManagement.md)
-   [Incident Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/incident-management/c_IncidentManagement.md)
-   [Change Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/change-management/c_ITILChangeManagement.md)

Role requirements for operations in this section:

-   Accessing the Explore CI Related Item Configurations \[sn\_cmdb\_ws\_explore\_ci\_related\_item\_config\] table to configure the list of charts that appear in the Related Items tab: sn\_cmdb\_ws.config\_editor
-   Configuring your preferences for which related item charts appear by selecting the Related Item Settings icon in the Related Items tab: Any logged in user

## Relationships

This section shows the CI relationships, which include:

-   Total relationships: Total number of relationships for this CI
-   Duplicate relationships: Total number of duplicate relationship for this CI
-   Stale relationships: Total number of stale relationship for this CI

In this section, you can:

-   Switch between the following view types:
    -   Tree view: Shows the downstream and upstream relationships in a tree format. You can expand and collapse any level that you want to see more or less details for.
    -   Flat view: Shows the CI relationships in a flat view. You can adjust the number of levels of relationships to show, or filter to show only specific CIs.
-   Select **Edit relationships** to open Unified Map for the CI in edit mode and with the following map settings:

    -   Home node set to the current CI.
    -   Relationship levels set to 1 level.
    -   Layers set to show Business, Service Instances, Applications, and infrastructure.
    -   Layout is set to Vertical.
    This function isn't available for a non-operational CI. For information about using the **Life cycle stage** attribute to define a CI's operational state, see [Configure CIs to appear based on life cycle stage value](../task/unified-map-confg-operational-state.md).

    If the CI class is a Service Instance \[cmdb\_ci\_service\_auto\] or a derived class, then you must either use Service Mapping \(if installed\) to edit a map for a Service Instance, or edit dependency relationships in Unified Map.

-   Select **Refresh** after saving changes in Unified Map, to reflect your updates in the Relationship section.

More information about relationships and about editing relationships in Unified Map:

-   [CI relationships in the CMDB](c_CIRelationships.md)
-   [Edit relationships in Unified Map](../task/unified-map-edit-connection.md)
-   [CI relationship editor](c_RelationshipEditor.md)
-   [Service Mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-mapping/c_ServiceMappingOverview.md)
-   [Unified Map](cmdb-workspace-unified-map.md)

Role requirements for operations in this section: **Edit relationships** requires sn\_cmdb\_editor

## Services and Offerings

This section shows cards with counts of the following services and offerings associated with the CI:

-   Service Instance: Any CI related to the Service Instance \[cmdb\_ci\_service\_auto\] table where **Service Classification** is **Application Service**.
-   Business Service Offering: Any Service Instance \(**Service Classification** is **Application Service**\) that this CI is related to, and which has a relationship to Service\_Offering where **Service Classification** is **Business Service**.
-   Technology Management Offering: Any Service Instance \(**Service Classification** is **Application Service**\) that this CI is related to, and which has a relationship to Service\_Offering where **Service Classification** is **Technical Service** or the CI is related to a Dynamic CI Group, which is part of a Technical Service Offering.
-   Technology Management Service: Parent of a Technology Management Offering.

Select a tile to drill down to the specific records associated with the tile.

More information:

-   [CSDM terms](../../csdm-implementation/reference/csdm-term-definitions.md)
-   [Service Delivery domain in the CSDM model](../../csdm-implementation/concept/manage-tech-servs-domain.md)
-   [Access CSDM features](../../csdm-implementation/concept/csdm-content-frame-using.md)
-   [CSDM implementation stage — Walk](../../csdm-implementation/concept/csdm-implement-walk-stage.md)
-   [Service instances \(Application services\)](application-services.md)

## Health

This section shows aggregations from the latest CMDB Health test results for the Completeness, Correctness, Compliance, and Relationship KPIs, and the aggregated state of attestation. Color codes are used to denote pass/fail scores.

This section shows meaningful details only if CMDB Health is set up and the associated dashboard jobs are running.

More information:

-   [CMDB Health](c_CMDBHealth.md)
-   [CMDB Health KPIs and metrics](../reference/r_CMDBHealthMetrics.md)
-   [CIs attestation](attesting-cis.md)
-   [Configuring CMDB Health](c_CMDBHealthSetupandConfig.md)

## CMDB 360

This section shows discovery sources data from the CMDB 360 data store for the CI. It shows the CI attributes and for each attribute, its current CMDB value, and any values that were reported by discovery sources for that attribute.

This section appears only if CMDB 360 is enabled and configured.

More information:

-   [CMDB 360](multisource-cmdb.md)
-   [CMDB 360 experience in CMDB Workspace and in Service Graph Workspace](cmdb360-exp-cmdb-workspace.md)
-   [Configure the CMDB 360 dashboard in CMDB Workspace or in Service Graph Workspace](../task/workspc-mltsrc-configure.md)

**Parent Topic:**[CMDB Workspace store app](cmdb-workspace.md)

