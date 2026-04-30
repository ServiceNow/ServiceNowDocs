---
title: Service Definition form
description: In the Customer Service Management \(CSM\) application, the Service Definition form displays information about a service definition configuration. This information record stores the details about a service that is provided to customers.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Customer Service forms, Customer Service Management reference, Customer Service Management]
---

# Service Definition form

In the Customer Service Management \(CSM\) application, the Service Definition form displays information about a service definition configuration. This information record stores the details about a service that is provided to customers.

<table id="table_czw_ftc_nr"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number \(deprecated\)

</td><td>

The unique number of the service definition record.**Note:** Starting with the Washington DC release, this field has been replaced with the **ID** field.

</td></tr><tr><td>

Name

</td><td>

The name of the service definition.

</td></tr><tr><td>

ID

</td><td>

The ID of the service definition.The system auto-populates the **ID** field with the name of the service definition and replaces the spaces with underscores. The ID can contain alphanumeric characters and underscores and can be up to 40 characters in length.

**Note:** The value in this field must be unique.

</td></tr><tr><td>

Table

</td><td>

The table that the service definition is available for, either the Case table or a table that extends the case table.For example, if the service is available for the onboarding case type, select the Onboarding Case \[sn\_onboarding\_case\] table.

</td></tr><tr><td>

Customer service type

</td><td>

The type of service:-   Pre-sale
-   Post-sale
-   General

A service type enables the system to display services based on the context.

</td></tr><tr><td>

Playbook record generator

</td><td>

The playbook record generator associated with the service definition.If a service definition has an associated playbook, the agent can use the playbook in a tab on the case record. For more information, see [Associate a playbook with a service definition](../task/service-def-associate-playbook.md).

</td></tr><tr><td>

Image

</td><td>

The image associated with the service definition.Service definitions appear in the [case type selector](../concept/csm-case-type-select-modals.md) or [case task type selector](../concept/csm-case-task-type-select-modal.md) in a card view. The image appears in the card for a service definition along with the name and description.

</td></tr><tr><td>

Order

</td><td>

This value determines the order in which the services are displayed in the case type selector or other workflows. Service definitions with the lowest order value are displayed first. The default value is 100.-   Service definitions with no order value appear above the ordered service definitions.
-   If one or more service definitions have the same order value, the system displays the service definitions in alphabetical order.

</td></tr><tr><td>

Active

</td><td>

Enables the service definition.

</td></tr><tr><td>

Description

</td><td>

The description of the service definition.Service definitions appear in the case type selector in a card view. The card includes the name, description, and image for a service definition. Customer service agents can search for services by entering keywords found in the service definition name and description.

</td></tr><tr><td>

Default table field values

</td><td>

One or more fields and default values from the target table \(the table that you selected in the **Table** field\). When a record is created for the target table for service definitions, the system uses these values to automatically fill in the record fields.

</td></tr></tbody>
</table>After creating and saving a service definition, the following related lists are available on the Service Definition form:

-   Product Service Relationships
-   Catalog Service Relationships
-   Service to Service Relationships
-   Service Definition Category Relationships
-   Reports

