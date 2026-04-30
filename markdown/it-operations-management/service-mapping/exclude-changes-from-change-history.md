---
title: Fine-tune tracking changes for the change history
description: Define CI fields for which the system reflects changes in the change history for application services. The change history view shows changes to CIs making up application services as well as changes to application services themselves.
locale: en-US
release: xanadu
product: Service Mapping
classification: service-mapping
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Advanced Service Mapping configuration, Configuring Service Mapping, Service Mapping, ITOM Visibility, IT Operations Management]
---

# Fine-tune tracking changes for the change history

Define CI fields for which the system reflects changes in the change history for application services. The change history view shows changes to CIs making up application services as well as changes to application services themselves.

## Before you begin

Role required: admin

## About this task

Details about changes to a service instance and to its CIs are stored in the CMDB. Typically, these changes reflect adding or removing CIs from a service instance, upgrading or updating CIs, or modifying CI configuration files. The system gathers this data by querying CMDB tables and then creating the change history view. In deployments where Service Mapping is activated, the type of change information Service Mapping queries depends on discovery patterns that Service Mapping uses to discover CIs.

Changes to configuration files are associated with CIs to which these files belong. Maps show configuration file changes as changes to related CIs.

## Procedure

1.  Navigate to **All** &gt; **Configuration** &gt; **Exclusion List**.

    The Exclusion Lists list opens displaying records that the system uses to exclude changes from the change history view.

2.  To make the system ignore changes to an extra field:

    1.  Click **New**.

    2.  Enter the CI class name in the **Table Name** field.

        For example, enter `cmdb_ci` for the Configuration Item \[cmdb\_ci\] class.

        **Note:** The Service Mapping user interface refers to CI classes as CI types.

    3.  Enter the name of the field you want to exclude in the **Field Name** field.

        For example, enter `work_notes` to exclude changes to the item work notes from the change history view.

    4.  Select **Submit**.

3.  To make the system include previously ignored changes in the change history:

    1.  Select the check boxes next to the relevant records.

    2.  Select **Delete** from the **Actions on selected rows** list.


**Related topics**  


[View the change history of application services in legacy Agent Workspace](workspace-view-history-app-service.md)

[View the change history of application services in classic Service Mapping](t_ViewCIChanges.md)

