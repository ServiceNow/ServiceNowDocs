---
title: View and edit class definitions and metadata
description: Use the CI Class Manager as a central location to explore the CMDB class hierarchy, CI table definitions, and class CIs. View the details of each table such as its label and fields, relationships, and all related metadata definitions.
locale: en-US
release: zurich
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [CMDB classifications and class dependency, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# View and edit class definitions and metadata

Use the CI Class Manager as a central location to explore the CMDB class hierarchy, CI table definitions, and class CIs. View the details of each table such as its label and fields, relationships, and all related metadata definitions.

## Before you begin

Role required: none

## About this task

The [CI Class Manager](../reference/ci-class-manager-landing-page.md) shows the entire CMDB class hierarchy in a tree-view format, consolidating class definitions into a central location. It lets you display metadata information for a class, such as reconciliation rules, mandatory and recommended fields, and audit templates. You can also select a specific class to view, to modify, or to extend its definition to create a derived class. For each class, you can directly access CMDB Health settings, identification and reconciliation rules, orphan scorecard, and certificate template, defined for the class.

For more information about extending a class and how attributes are derived from a parent class in that process, see [Table extension and classes](https://www.servicenow.com/docs/access?context=table-extension-and-classes&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

## Procedure

1.  Navigate to **All** &gt; **Configuration** &gt; **CI Class Manager**.

2.  Click **Hierarchy** to expand the CI Classes list and then select a class to display details for.

3.  On the class navigation bar, expand the following items to display further details for the class.

    -   **Class Info**:
        -   **Basic Info**:Displays details for the selected class, such as the display and table name, description, and class icon. Lets you edit some of the class definitions, and prevents editing of some details such as the table name.

            Role required: itil for reading, and itil\_admin and personalize\_dictionary for writing.

        -   **Attributes**:Displays table attributes \(columns\). Lets you edit those attributes and add new ones. For description of the different attributes in the list view, see [Dictionary entry form](https://www.servicenow.com/docs/access?context=r_DictionaryEntryForm&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

            Role required: personalize\_dictionary for reading and writing

            To add an attribute:

            1.  Click the **Added** tab and scroll to the bottom of the list.
            2.  Double-click **Insert new column**, and enter details for each new class attribute. Set **Identification** to true to designate an attribute as a CI identifier for class identification.
            3.  Click **Save**, and fix any errors that appear.
        -   **Identification** and **Reconciliation**: Displays and lets you edit, create, and delete identification and [inclusion rules](create-id-inclusion-rule.md), reconciliation and [data refresh rules](create-datasource-staleness-rule.md) for the class.

            See [CMDB Identification and Reconciliation \(IRE\)](../concept/c_CMDBIdentifyandReconcile.md) for more information.

            Role required: itil for reading, and itil\_admin \(on top of itil\) for writing.

        -   **Dependent Relationships**: Displays and lets you edit, create, and delete hosting and containment relationships for the class. See [CMDB dependent relationship rules](../concept/c_ServiceRulesMetadata.md) for more information.

            Role required: itil for reading and itil\_admin \(on top of itil\) for writing.

        -   **Suggested Relationships**: Displays a diagram of all suggested relationships for the class, and lets you delete or add suggested relationships for the class. Use the navigation tools to increase or decrease the diagram, and to move the diagram on the page. Use the filter to display specific relationship types. See [Suggested class relationships](../reference/r_SuggestedRelationshipModel.md) for more information.

            Role required: itil.

    -   **All Relationship Rules**: Displays a combined diagram of all suggested relationships and all dependent relationships for the class. Use the navigation tools to zoom in or out, and to move or center the diagram on the page. Use the filter to display specific relationship categories.
    -   **Health**: Lets you review and configure CMDB Health-related system properties, scorecards, and rules and settings for all CMDB health KPI and metrics, at the class level. See [CMDB Health](../concept/c_CMDBHealth.md) for information about enabling and configuring CMDB Health, and displaying health reports.

        Role required: Itil for reading and itll\_admin \(on top of itil\) for writing.

    -   **CI List**: Displays the CIs of the selected class. Lets you create CIs of the selected class and perform other operations such as delete.

        Role required: Itil for reading. Writing requirements follow the selected table settings.


**Parent Topic:**[CMDB classifications and class dependency](../concept/c_CMDBClassifications.md)

**Related topics**  


[Dependent CIs management](../concept/manage-dependent-ci.md)

[CMDB record types](../reference/r_CMDBRecordTypes.md)

[Related Lists of CI components](../reference/r_RelatedListsOfCIComponents.md)

[Create a CI class](t_CreateCIType.md)

[Reclassify a CI](t_ManuallyReclassifyCI.md)

[Delete CIs](delete-class-records-ci-class-mgr.md)

[Update class list in the Principal Class filter](update-principal-class-filter.md)

[Create or modify map icons](../../business-service-management-map-ng/task/t_CreateModifyNGBSMMapIcons.md)

