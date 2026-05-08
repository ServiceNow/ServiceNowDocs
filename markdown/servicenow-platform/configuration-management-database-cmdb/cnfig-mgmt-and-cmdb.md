---
title: Overview of CMDB
description: The Configuration Management Database \(CMDB\) creates and maintains the logical configurations your network infrastructure needs to support a ServiceNow service.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Explore, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Overview of CMDB

The Configuration Management Database \(CMDB\) creates and maintains the logical configurations your network infrastructure needs to support a ServiceNow service.

CMDB Overview 

In CMDB, the logical service configurations are mapped to the physical layout data of the supporting network and application infrastructure in each of your respective domains. They track the physical and logical state of IT service elements and associate incidents to the state of service elements, which helps in analyzing trends and reducing problems and incidents.

The configurations are stored in a configuration management database \(ServiceNow CMDB\) which consists of entities, called Configuration Items \(CI\), that are part of your environment. A CI may be:

-   A physical entity, such as a computer or router
-   A logical entity, such as an instance of a database
-   Conceptual, such as a Requisition Service

In each case, there are attributes about the CI that you want to maintain, and there is control you want to have over the CI. There are changes that may need to be made and tracked against the CI. Also, a CI does not exist on its own. CIs have dependencies and relationship with other CIs. For example, the loss of disk drives may take a database instance down, which affects the requisition service that the HR department uses to order equipment for new employees.

It is this relationship data that makes the CMDB a powerful decision support tool. Understanding the dependencies and other relationships among your CIs can tell you, for example, exactly who and what is affected by the loss of that bank of disk drives. When you find out that a router has failed, you will be able to assess the effect of that outage. When you decide to upgrade the processor in a server, you can tell who or what will be affected during the outage.

Configuration items differ from environment to environment because each customer has unique needs. Details about the exact physical attributes of a computer may be needed by one customer, but may represent meaningless data to another. The NOW Platform provides a mechanism to easily define new classes of configuration items and new relationships that may exist between CIs. New classes can be defined that extend other classes. For example, a laptop class exists that extends the computer class. The computer class itself extends the base CI class. Customer class extensions are automatically part of the ServiceNow environment and blend seamlessly into the integration points for other ITIL processes.

You can for example, set the **Used for** attribute in the cmdb\_ci\_server table to a value such as ‘development’, ‘test’, or ‘production’. These values indicate the environment that the CI is supporting, and serve as a way of tracking a CI through its life cycle in a changing environment.

## Extended CMDB

In base systems, CMDB provides core functionality for the configuration management database, including modules for hardware and configuration items. The separate Extended CMDB plugin includes a collection of modules for specialized configuration items, such as radio hardware, test equipment, and voice system hardware.

To extend the CMDB you can activate the following plugins to access the modules for specialized configuration items.

-   CMDB Mainframe \(com.snc.cmdb.mainframe\)
-   CMDB Radio Category \(com.snc.cmdb.radio.category\)
-   CMDB Telecom Category \(com.snc.cmdb.telecom.category\)
-   CMDB Test Equipment \(com.snc.cmdb.test.equipment\)

## CMDB hierarchy and CI Class Manager

Sets of CIs that share attributes are stored in their own class table. All CMDB tables are connected by relationships and inherit attributes from each other to form a web of tables referred to as the CMDB hierarchy.

Use the [CI Class Manager](../reference/ci-class-manager-landing-page.md) to manage CMDB classes within the CMDB hierarchy, CMDB Health, and other class-related definitions. For example, in the CI Class Manager you can view class attributes, class identification rules, and the list of CIs for a specific class. To view the list of CIs in the CMDB, you can also enter `cmdb_ci_list.do` in the filter navigator.

## Architecture

![Components and data flow of the CMDB](../image/CMDBArchitecture_NewBrand.png)

## Related tables

There are tables that are not part of the CMDB hierarchy but which still qualify as CMDB data. Related tables, such as the Serial Number \[cmdb\_serial\_number\] table, don't inherent from the Configuration Item \[cmdb\_ci\] table, but have at least one column that references a CMDB CI. Related tables are specified in the Related Entries \[cmdb\_related\_entry\] table.

Some scenarios that involve related tables, can result in orphan or otherwise stale records in related tables. A CI in a related table can, for example, become orphan if the referenced CI in the CMDB is deleted. You can use the [CMDB Data Manager](cmdb-data-management.md) to create a policy of the 'Delete CMDB Related Entry' policy type, that will cascade-delete that un-needed related items data. For more information about creating that CMDB Data Manager policy, see [Create a CMDB Data Manager policy](../task/data-manager-create-policy-wrkspc.md).

## Localization

Using the Translated Text field type \(instead of string\) for attributes in CMDB tables, can reduce overall performance, including performance of features such as CMDB Health. This is because values in CMDB tables are dynamic and are likely to change often, and the data itself is likely to continuously grow. Using the Translated Text field also requires manual update of related text. The Translated Text field type is typically effective with static data that doesn't change and doesn't grow. For more information about field types, see Field types reference.

## Roles required

Reading CMDB tables directly requires the cmdb\_read role, however accessing the **Configuration** module requires the sn\_cmdb\_editor, sn\_cmdb\_admin, asset, itil, or itil\_admin roles. For viewing CMDB-related records in the user interface, the sn\_cmdb\_editor or itil roles are usually sufficient. For updating records and for other manipulation of records, roles with higher credentials are usually required, as noted in each procedure throughout the documentation set.

For details about CMDB and other roles, see Base system roles, or see a feature components topic such as [Components installed with CMDB Workspace](../reference/installed-with-cmdb-workspace.md).

**Related topics**  


[CMDB schema model](c_ConfigurationManagementDatabase.md)

