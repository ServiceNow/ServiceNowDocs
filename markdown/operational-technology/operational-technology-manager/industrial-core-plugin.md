---
title: Industrial Core plugin
description: The Industrial Core plugin contains the class mappings needed for the Operational Technology \(OT\) certified Service Graph Connectors.
locale: en-US
release: zurich
product: Operational Technology Manager
classification: operational-technology-manager
topic_type: reference
last_updated: "2026-02-09"
reading_time_minutes: 3
breadcrumb: [Reference, Operational Technology Manager, Operational Technology]
---

# Industrial Core plugin

The Industrial Core plugin contains the class mappings needed for the Operational Technology \(OT\) certified Service Graph Connectors.

## Industrial Core plugin overview

The Industrial Core plugin \[sn\_ot\_core\] introduces foundational capabilities to support OT-specific data models and the site based licensing requirements for OT. The plugin is required as a dependency by all products in the Operational Technology Management solution. The dependency can be a direct dependency or a dependency through a base product. For example, the Operational Technology Manager application is a dependency. For the Operational Technology Vulnerability Response application, the Industrial Core plugin isn't added as a dependency because Operational Technology Manager is a direct dependency for Operational Technology Vulnerability Response.

**Note:** All partner applications integrating with the OT functionality must declare a dependency on the Industrial Core plugin. This ensures consistent handling of licensing and future model enhancements.

## Industrial Core plugin features

The following table summarizes the features for the Industrial Core plugin.

<table id="table_iwd_2jv_zfc"><thead><tr><th>

Feature

</th><th>

Description

</th></tr></thead><tbody><tr><td>

OT Class Mapping Template \[ot\_class\_mapping\_template\]

</td><td>

The Industrial Core plugin introduces a configuration template to manage class mappings through a user-accessible table part of the OT Service Graph Connectors. This configuration template replaces the prior script-based approach.While the OT Class Mapping Template is currently optional, adopting this method is recommended as it allows you to view, manage, and override class mappings directly in the UI and provides a greater transparency and flexibility.

**Note:** Partners can extend the OT Class Mapping Template table in the scope of their application to capture the class mappings specific to the integration.

With the OT Class Mapping template, you can also define an OT device naming strategy per class by using the **Allow Custom Device Naming** and **Device Naming Strategy** fields. For more information about how to implement the device naming strategy, see [Create and use an OT device naming strategy](../task/create-use-ot-device-naming-strategy.md).

For more information about the OT Class Mapping Template and its available fields, see the **OT Class Mapping Template** section in [Operational Technology \(OT\) extension classes](https://www.servicenow.com/docs/access?context=cmdb-ci-class-models-operation-technology&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).For more information about reviewing class mappings for the Service Graph Connector for Microsoft Excel, see [Review class mappings](../task/review-class-mappings-sgc-excel.md).

</td></tr><tr><td>

OT Device Network Connection \[sn\_ot\_device\_network\_connection\]

</td><td>

The OT Device Network Connection \[sn\_ot\_device\_network\_connection\] table references the CI relationships \[cmdb\_rel\_ci\] table, and identifies device-to-device connections in CI relationships for OT devices.**Note:** This data is populated with the available OT integrations and cannot be manually created.

For more information about the OT Device Network Connection data model, see [Operational Technology \(OT\) extension classes](https://www.servicenow.com/docs/access?context=cmdb-ci-class-models-operation-technology&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td>

OT Site Map \[sn\_ot\_site\_map\]

</td><td>

The OT Site Map \[sn\_ot\_site\_map\] table is used to assign metadata information to OT devices and contains the following fields.-   Approval group
-   Assigned to
-   Change group
-   Company
-   ISA assignment site
-   Location
-   Managed by
-   Managed by group
-   Owned by
-   Site description
-   Site name
-   Network type
-   Support group
-   Active
-   Supported by

</td></tr><tr><td>

OT Discovered Subnet \[sn\_ot\_discovered\_subnet\]

</td><td>

The OT Discovered Subnet \[sn\_ot\_discovered\_subnet\] table contains the discovered subnets used for OT subnet mapping and contains the following fields.-   CIDR
-   Discovered managed network
-   Site

</td></tr><tr><td>

OT Activity \[sn\_ot\_activity\]

</td><td>

The OT Activity \[sn\_ot\_activity\] table captures the following activities that occur on the OT device:-   Addition, update, or retiring of a configuration item
-   Addition of an IP address

</td></tr><tr><td>

OT Backup Job Execution History \[ot\_backup\_history\_and\_comparison\_log\]

</td><td>

The Backup Job Execution History \[ot\_backup\_history\_and\_comparison\_log\] class creates a history of records for all backup executions. It compares the history of records for all backup executions.

</td></tr><tr><td>

OT Automation Repo \[ot\_automation\_repo\]

</td><td>

The OT Automation Repo \[ot\_automation\_repo\] class acts as a repository to store all configuration changes you want to perform on an OT entity.

</td></tr><tr><td>

OT Automation Repo Device M2M \[ot\_automation\_repo\_device\_m2m\]

</td><td>

The OT Automation Repo Device M2M \[ot\_automation\_repo\_device\_m2m\] class acts a reference to the OT Automation Repo and the OT Entity table.

</td></tr><tr><td>

OT AutomationCommit \[ot\_automation\_commit\]

</td><td>

OT AutomationCommit \[ot\_automation\_commit\] class acts as a reference to the changes you have committed to a project.

</td></tr></tbody>
</table>-   **[Create and use an OT device naming strategy](../task/create-use-ot-device-naming-strategy.md)**  
Create and use the Operational Technology \(OT\) device naming strategy to create unique names for your OT devices.

**Parent Topic:**[Operational Technology Manager reference](operational-technology-manager-reference.md)

