---
title: View and edit class definitions and metadata
description: Use the CI Class Manager as a central location to explore the CMDB class hierarchy, CI table definitions, and class CIs. View the details of each table such as its label and fields, relationships, and all related metadata definitions.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [CMDB classifications and class dependency, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# View and edit class definitions and metadata

Use the CI Class Manager as a central location to explore the CMDB class hierarchy, CI table definitions, and class CIs. View the details of each table such as its label and fields, relationships, and all related metadata definitions.

## Before you begin

Role required: Per item as specified

## About this task

The [CI Class Manager](../reference/ci-class-manager-landing-page.md) shows the entire CMDB class hierarchy in a tree-view format, consolidating class definitions into a central location. It lets you show metadata information for a class, such as reconciliation rules, mandatory and recommended fields, and audit templates. You can also select a specific class to view, to modify, or to extend its definition to create a derived class. For each class, you can directly access CMDB Health settings, identification and reconciliation rules, orphan scorecard, and certificate template, defined for the class.

For more information about extending a class and how attributes are derived from a parent class in that process, see [Table extension and classes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/table-administration-and-data-management/table-extension-and-classes.md).

## Procedure

1.  Navigate to **All** &gt; **Configuration** &gt; **CI Class Manager**.

2.  Select **Hierarchy** to expand the CI Classes list and then select a class to show details for.

3.  On the class navigation bar, expand the following items to show further details for the class.

    -   **Class Info**:
        -   **Basic Info**:Shows details for the selected class, such as the display and table name, description, and class icon. Lets you edit some of the class definitions, and prevents editing of some details such as the table name.

            Role required: sn\_cmdb\_editor or itil for reading. sn\_cmdb\_admin or itil\_admin, and personalize\_dictionary for writing.

        -   **Attributes**:Shows table attributes \(columns\). Lets you edit those attributes and add new ones. For description of the different attributes in the list view, see [Dictionary entry form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/table-administration-and-data-management/r_DictionaryEntryForm.md).

            Role required: personalize\_dictionary for reading and writing

            To add an attribute:

            1.  Select the **Added** tab and scroll to the bottom of the list.
            2.  Double-click **Insert new column**, and enter details for each new class attribute. Set **Identification** to true to designate an attribute as a CI identifier for class identification.
            3.  Select **Save**, and fix any errors that appear.
        -   **Identification** and **Reconciliation**: Shows and lets you edit, create, and delete identification and [inclusion rules](create-id-inclusion-rule.md), reconciliation and [data refresh rules](create-datasource-staleness-rule.md) for the class.

            See [CMDB Identification and Reconciliation \(IRE\)](../concept/c_CMDBIdentifyandReconcile.md) for more information.

            Role required: sn\_cmdb\_editor or itil for reading, and sn\_cmdb\_admin or itil\_admin \(on top\) for writing.

        -   **Dependent Relationships**: Shows and lets you edit, create, and delete hosting and containment relationships for the class. See [CMDB dependent relationship rules](../concept/c_ServiceRulesMetadata.md) for more information.

            Role required: sn\_cmdb\_editor or itil for reading, and sn\_cmdb\_admin or itil\_admin \(on top\) for writing.

        -   **Suggested Relationships**: Shows a diagram of all suggested relationships for the class, and lets you delete or add suggested relationships for the class. Use the navigation tools to increase or decrease the diagram, and to move the diagram on the page. Use the filter to show specific relationship types. See [Suggested class relationships](../reference/r_SuggestedRelationshipModel.md) for more information.

            Role required: sn\_cmdb\_editor or itil.

    -   **All Relationship Rules**: Shows a combined diagram of all suggested relationships and all dependent relationships for the class. Use the navigation tools to zoom in or out, and to move or center the diagram on the page. Use the filter to show specific relationship categories.
    -   **Health**: Lets you review and configure CMDB Health-related system properties, scorecards, and rules and settings for all CMDB health KPI and metrics, at the class level. See [CMDB Health](../concept/c_CMDBHealth.md) for information about enabling and configuring CMDB Health, and showing health reports.

        Role required: sn\_cmdb\_editor or itil for reading, and sn\_cmdb\_admin or itil\_admin \(on top\) for writing.

    -   **CI List**: Shows the CIs of the selected class. Lets you create CIs of the selected class and perform other operations such as delete.

        Role required: sn\_cmdb\_editor or Itil for reading. Writing requirements follow the selected table settings.


**Parent Topic:**[CMDB classifications and class dependency](../concept/c_CMDBClassifications.md)

**Related topics**  


[Dependent CIs management](../concept/manage-dependent-ci.md)

[CMDB record types](../reference/r_CMDBRecordTypes.md)

[Related Lists of CI components](../reference/r_RelatedListsOfCIComponents.md)

[Create a CI class](t_CreateCIType.md)

[Reclassify a CI](t_ManuallyReclassifyCI.md)

[Delete CIs](delete-class-records-ci-class-mgr.md)

[Update the list of classes in the Principal Class filter](update-principal-class-filter.md)

[Create or modify map icons](../../business-service-management-map-ng/task/t_CreateModifyNGBSMMapIcons.md)

