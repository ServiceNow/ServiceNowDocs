---
title: Configure dynamic related records
description: System administrators can configure the dynamic related records feature to display related records in the contextual side panel in CSM Configurable Workspace. These records dynamically change based on the context of the current record or playbook activity.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [Agent tools, Organize agent workspaces, Configuring Customer Service Management, Customer Service Management]
---

# Configure dynamic related records

System administrators can configure the dynamic related records feature to display related records in the contextual side panel in CSM Configurable Workspace. These records dynamically change based on the context of the current record or playbook activity.

Configuring the dynamic related records feature involves several types of records. See the following table for details about these record types.

-   Related record contexts
-   Related record definitions
-   Context related record definitions

<table id="table_s4x_hbc_gqb"><thead><tr><th>

Record type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Related record context

</td><td>

Defines the context in which related records appear in the Related Records tab. You can create a related record context for the following types of records:

-   A source record, such as a customer service case
-   A playbook activity, such as adding additional members to an onboarding case

 A context record identifies the following information:

-   The table that contains the type of record for which related records are being configured.
-   Additional conditions that apply to the selected table. These conditions determine if the related record definitions for the selected table are executed at runtime.
-   The types of related records to display, such as SLAs or emails.

</td></tr><tr><td>

Related record definition

</td><td>

Identifies one specific type of data to be retrieved, such as SLAs or active contracts.

 You can create a related record definition for each type of data to include in the Related Records tab and then associate one or more definitions with a context record.

</td></tr><tr><td>

Context related record definition

</td><td>

Defines the relationship between a context record and its associated definition records.

 When you open a context record, you can see the associated definition records in the Context Related Record Definitions related list.

</td></tr></tbody>
</table>For more information about these tables, including field descriptions, see [Dynamic related record tables](../reference/dynamic-related-record-tables.md).

## How the context and definition records work

The context record defines the context in which related records appear in the Related Records tab. This includes conditions to apply to the selected record type. For example, to create a context record for an onboarding playbook activity:

1.  Select the table that stores the activity: **Activity Execution \[sys\_pd\_activity\_context\]**.
2.  Define additional conditions that apply to the selected table:

    -   **\[Activity.Process definition\] \[is\] \[Onboarding playbook\]**
    -   **\[Activity\] \[is\] \[Add additional members\]**
    These conditions determine if the related record definitions for the selected table are executed at runtime. If the conditions evaluate to true, the definitions are executed. If false, the definitions are ignored. If a context has no conditions, this evaluates to true.

3.  Select the related record definitions to execute: **Additional Members**

At runtime, the system checks to see if there are related record contexts that match the current record or playbook activity.

-   When it finds a match, the system evaluates the conditions defined in the context.
-   If the conditions evaluate to true, the system executes the related record definitions for the context.

To continue with the example above, an agent using the Case Playbook for Onboarding is currently working on the activity to add additional members. The system performs the following actions to display the correct related records:

-   Checks the active contexts and finds **Onboarding Additional Members**.
-   Evaluates the conditions in the context and determines that they evaluate to true.
-   Executes the **Additional Members** related record definition.
-   Retrieves and displays the correct set of records from the table identified in the **Additional Members** related record definition. In this case, the Related Party \[sn\_customerservice\_related\_party\] table.

The definition record uses a script to define which related records are retrieved based on the context. This record also includes the table where the related record data is stored. At runtime, the script evaluates the context of the current record or playbook activity, along with any conditions, and dynamically displays the related record data.

## Dynamic related record configuration tasks

Configuring the dynamic related records feature includes the following tasks:

-   Configure the related record contexts and definitions to identify which related records to display in the Related Records tab.
-   Configure the card layout for the records displayed in the Related Records tab.
-   Configure the maximum number of related records to display.

## Related Records list card layout

Records appear in the Related Records tab in a card format. This format is created with [Entity View Action Mapper](https://www.servicenow.com/docs/access?context=entity-view-action-mapper&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US) \(EVAM\), a ServiceNow AI Platform application that standardizes how different data sources display in cards and lists.

EVAM uses view configurations and view templates to determine how information for each type of related record is displayed.

-   EVAM view configuration: Combines conditions, the table and table fields, and declarative actions with an associated view template.
-   EVAM view template: Contains the JSON used to give the necessary information for the card display and use.

EVAM view configurations can be grouped together to create configuration bundles. The Dynamic Related Records for Configurable Workspace plugin includes a configuration bundle, **dynamic\_related\_records\_bundle**, which contains view configurations and view templates for the dynamic related records feature.

The system administrator can modify the view configurations in the **dynamic\_related\_records\_bundle** or create new view configurations. This includes selecting the fields that are displayed on the card for each type of record. For more information, see:

-   [Define an EVAM view configuration](https://www.servicenow.com/docs/access?context=configuring-entity-view-action-mapper&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US)
-   [Define an EVAM view template](https://www.servicenow.com/docs/access?context=define-evam-template&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US)

## Related record definitions included with the plugin

The Dynamic Related Records for Configurable Workspace plugin includes several related record definitions for case records. To view a list of definitions, navigate to **Dynamic Related Record** &gt; **Related Record Definitions**.

The system administrator can make any of these definitions available to agents by adding them to the related records shared page in UI Builder.

<table id="table_kbr_yjl_lpb"><thead><tr><th>

Related record definition

</th><th>

Description

</th></tr></thead><tbody><tr><td>

SLAs

</td><td>

Displays SLAs for a case, including information from the following fields: -   Stage
-   SLA definition
-   Start time
-   Business time left

</td></tr><tr><td>

Emails

</td><td>

Displays emails for a case, including information from the following fields:-   Notification type
-   Subject
-   Recipient
-   Date created

</td></tr><tr><td>

Escalations

</td><td>

Displays escalations for a case or for the account and contact or consumer, including information from the following fields:-   State
-   Number
-   Escalation severity
-   Source record

</td></tr><tr><td>

Blocked By

</td><td>

Displays blocking tasks for a case, including information from the following fields:-   Blocking task
-   Blocking reason

</td></tr><tr><td>

Child Cases

</td><td>

Displays child cases related to a case, including information from the following fields:-   Number
-   Short description
-   Account and contact
-   Consumer

</td></tr></tbody>
</table>