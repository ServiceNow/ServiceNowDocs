---
title: Dynamic related record tables
description: The dynamic related records feature uses different tables to store context and definition information.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Dynamic related records, Configure dynamic related records, Agent tools, Organize agent workspaces, Configure, Customer Service Management]
---

# Dynamic related record tables

The dynamic related records feature uses different tables to store context and definition information.

The following tables support the configuration of the dynamic related records feature. These tables extend the sys\_metadata table.

## Related Record Context table

Records in the Related Record Context \[sn\_related\_record\_context\] table define the context in which related records appear in the Related Records tab. This includes the following information:

-   The selected table. You can create context records for source records \(such as customer service cases\) or playbook activities \(such as adding additional members to an onboarding case\).
-   Additional conditions that apply to the selected table. These conditions determine when the related record definitions for the selected table are executed.
-   The related record definitions to execute. These definitions identify the data to be retrieved, such as SLAs or emails.

<table id="table_qdx_zx4_t4b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

The unique name of the context record.

</td></tr><tr><td>

Applies to table

</td><td>

The table that stores the record type for the context record.

 To display related records for a source record, select the table that stores the source record. For example, Case \[sn\_customerservice\_case\].

 To display related records for a playbook activity, select the table that stores the activities: Activity Execution \[sys\_pd\_activity\_context\].

</td></tr><tr><td>

Primary reference field

</td><td>

The primary field from the **Applies to table** that is passed to the Context Related Record Definition for evaluation. The value is used by the scripted query in the definition. The following data types are supported:

-   Sys ID
-   Doc ID
-   Reference

</td></tr><tr><td>

Secondary reference field

</td><td>

The secondary field from the **Applies to table** that is passed to the Context Related Record Definition for evaluation. The value is used by the scripted query in the definition. The following data types are supported:

-   Sys ID
-   Doc ID
-   Reference

</td></tr><tr><td>

Application

</td><td>

The application to which the context record applies. This is a read-only field.

</td></tr><tr><td>

Active

</td><td>

Enables the context record.

</td></tr><tr><td>

Inherited

</td><td>

When enabled, the context record also considers tables that extend from the **Applies to table**.

</td></tr><tr><td>

Conditions

</td><td>

Conditions that are applied to the records in the **Applies to table**.

</td></tr></tbody>
</table>## Related Record Definition table

Records in the Related Record Definition \[sn\_related\_record\_definition\] table identify one type of data to be retrieved, such as active contracts, case tasks, or SLAs. A definition record includes:

-   The display label, which appears in the filter dropdown list in the Related Records tab.
-   The table to be queried from. For example, the Email \[sys\_email\] table.
-   If needed, primary and secondary reference tables.
-   Scripted conditions that further specify which fields to query from.

You can create definition records for each type of data to include in the Related Records tab and then associate the definitions with one or more context records.

<table id="table_icd_n1p_t4b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Display label

</td><td>

The unique name of the related record definition. This label appears in the filter list in the Related Records tab.

</td></tr><tr><td>

Primary reference table

</td><td>

The primary table used in the definition script. At runtime, the script expects to get passed a record of this type. If you entered a data type in the **Primary reference field** in the related record context, enter the table for that data type.

</td></tr><tr><td>

Secondary reference table

</td><td>

The secondary table used in the definition script. At runtime, the script expects to get passed a record of this type. If you entered a data type in the **Secondary reference field** in the related record context, enter the table for that data type.

</td></tr><tr><td>

Application

</td><td>

The application to which the definition record applies. This is a read-only field.

</td></tr><tr><td>

Queries from

</td><td>

The table that stores the related record data to be retrieved.

</td></tr><tr><td>

Active

</td><td>

Enables the definition record. A definition must be active for the related records of that type to be displayed in the Related Records tab.

</td></tr><tr><td>

Script

</td><td>

Create a script that defines which records are retrieved based on the context.

</td></tr></tbody>
</table>## Context Related Record Definition table

The Context Related Record Definition \[sn\_m2m\_context\_related\_record\_defn\] table defines the relationship between a context record and its associated definition records.

When you open a context record, you can see the associated definition records in the Context Related Record Definitions related list.

<table id="table_pbv_m4n_cqb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Related record context

</td><td>

The context record.

</td></tr><tr><td>

Related record definition

</td><td>

The name of the related record definition associated with the context record. The system uses this definition to determine which records to retrieve.

</td></tr><tr><td>

Application

</td><td>

The application to which the context record applies. This is a read-only field.

</td></tr><tr><td>

Order

</td><td>

The order determines where the related record type appears in the filter list in the Related Records tab. The order for this related record definition is compared with the order of the other definitions associated with the **Related record context** to determine the order of appearance in the filter list.

 If more than one context applies to a record, the system evaluates the order for all of the related record types. If there is a duplicate related record type, the system takes the record type with the lowest order value.

</td></tr><tr><td>

Active

</td><td>

Enables the **Related record definition** for this context record.

</td></tr></tbody>
</table>