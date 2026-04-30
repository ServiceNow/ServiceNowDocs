---
title: Components installed with Order Operations Case Management
description: Several types of components are installed with the Order Operations Case Management application, including tables, roles, and service definitions.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 7
breadcrumb: [Order Operations Case Management, Case management, Organize agent workspaces, Configuring Customer Service Management, Customer Service Management]
---

# Components installed with Order Operations Case Management

Several types of components are installed with the Order Operations Case Management application, including tables, roles, and service definitions.

## Tables

The Order Operations Case Management application adds the following tables.

<table id="table_v3g_jhj_jcc"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

[Order Case](../reference/order-case-form.md)\[sn\_order\_case\]

</td><td>

Stores order case records. This table extends the Case \[sn\_customerservice\_case\] table.Records in the Order Case table use the prefix **ORDCS**.

</td></tr><tr><td>

[Order Case Line](../reference/order-case-line-form.md)\[sn\_order\_case\_line\]

</td><td>

Stores the case line items created for order cases. This table extends the Case Line \[sn\_case\_line\] table.Requesters and fulfillers can use this table to capture the orders and order lines as line items on an order case for which they want to request order changes, resolve disputes, or make inquiries.

Records in the Order Case Line table use the prefix **ORDCSL**.

</td></tr></tbody>
</table>The Order Operations Case Management application also uses the following tables from the [Case lines and workflows](csm-case-mgmt-case-lines.md) application.

<table id="table_jcd_55l_fdc"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Case Line\[sn\_case\_line\]

</td><td>

The Case Line table stores case line item records. This table extends the Task table.The prefix for case line records is **CSL**.

</td></tr><tr><td>

Case Line Characteristic\[sn\_case\_line\_characteristic\]

</td><td>

The Case Line Characteristic form displays details about a case line item on a case record.The prefix for case line characteristic records is **CSLC**.

</td></tr><tr><td>

Case Line Task\[sn\_case\_line\_task\]

</td><td>

The Case Line Task table stores the tasks related to case line items. This table extends the Case Task table.The prefix for case line task records is **CSLTASK**.

</td></tr></tbody>
</table>## Roles

The Order Operations Case Management application includes roles that provide access to order cases and order case line items. It also updates some existing roles to provide this same access.

<table id="table_nfd_kkj_jcc"><thead><tr><th>

Role

</th><th>

Description

</th><th>

Includes roles

</th></tr></thead><tbody><tr><td>

Order case agent\[sn\_order\_case.agent\]

</td><td>

Provides create, read, and update access to:-   Order cases
-   Order case line items
-   Case line characteristics
-   Order case tasks
-   Order case line tasks

Provides read access to:

-   Orders
-   Order line items
-   Order line characteristics

</td><td>

-   sn\_customerservice\_agent
-   sn\_order\_case.creator
-   sn\_order\_case.writer
-   sn\_order.navigation\_menu
-   sn\_order\_case.delete

</td></tr><tr><td>

Order case agent manager\[sn\_order\_case.agent\_manager\]

</td><td>

Provides create, read, and update access to:-   Order cases
-   Order case line items
-   Case line characteristics
-   Order case tasks
-   Order case line tasks

This role can also override agent actions.

</td><td>

-   sn\_customerservice\_manager
-   sn\_order\_case.agent
-   sn\_order\_case.report\_viewer

</td></tr><tr><td>

Order case viewer\[sn\_order\_case.viewer\]

</td><td>

Provides read access to the following records:-   Order cases
-   Order case line item s
-   Case line characteristics

</td><td>

sn\_case\_line.characteristic\_viewer

</td></tr><tr><td>

Order case creator\[sn\_order\_case.creator\]

</td><td>

Provides create access to the following records:-   Order cases
-   Order case line items
-   Case line characteristics

</td><td>

-   sn\_order\_case.viewer
-   sn\_case\_line.characteristic\_creator

</td></tr><tr><td>

Order case writer\[sn\_order\_case.writer\]

</td><td>

Provides write access to the following records:-   Order cases
-   Order case line items
-   Case line characteristics

</td><td>

-   sn\_order\_case.viewer
-   sn\_case\_line.characteristic\_writer

</td></tr><tr><td>

sn\_order\_case.delete

</td><td>

Provides delete access to order cases and case line items.**Note:** Once a case has been submitted, only users with the admin role can delete an order case or case line items.

</td><td>

-   sn\_order\_case.viewer
-   sn\_case\_line.characteristic\_delete

</td></tr><tr><td>

Order case report viewer\[sn\_order\_case.report\_viewer\]

</td><td>

Report viewer role for the Order Case and Order Case Line tables. This role can view reports for order cases.

</td><td>

 

</td></tr><tr><td>

sn\_order\_case.navigation\_menu

</td><td>

Provides access to Order case navigation menus.

</td><td>

 

</td></tr><tr><td>

sn\_caseline\_characteristic.viewer

</td><td>

Provides read access to case line characteristic records if the user has access to the case line items.

</td><td>

 

</td></tr><tr><td>

sn\_caseline\_characteristic.creator

</td><td>

Provides create access to case line characteristic records if the user has access to the case line items.

</td><td>

sn\_caseline\_characteristic.viewer

</td></tr><tr><td>

sn\_caseline\_characteristic.writer

</td><td>

Provides update access to case line characteristic records if the user has access to the case line items.

</td><td>

sn\_caseline\_characteristic.viewer

</td></tr><tr><td>

sn\_caseline\_characteristic.delete

</td><td>

Provides delete access to case line characteristic records if the user has access to the case line items.

</td><td>

sn\_caseline\_characteristic.viewer

</td></tr><tr><td>

sn\_caseline\_characteristic.report\_viewer

</td><td>

Report viewer role for the Case Line Characteristic table.

</td><td>

 

</td></tr><tr><td>

Case task agent\[sn\_customerservice.case\_task\_agent\]

</td><td>

This role provides access to case tasks and related case information.For the Order Operations Case Management application, when a case line task is assigned to a case task agent, that agent has read access to the following records:

-   Order case
-   Order case line item
-   Case line characteristic

When a case line task is assigned to a case task agent, the agent's name and assignment group are added to the **Contributor Users** and **Contributor Groups** fields on the Order case record. If the **Assigned to** field on the case line task record changes, these fields are updated.

</td><td>

-   sn\_customerservice.customer\_data\_viewer
-   sn\_customerservice.csm\_workspace\_user
-   sn\_customerservice.case\_contributor\_editor

</td></tr></tbody>
</table>## Service definitions and service definition categories

The Order Operations Case Management application provides the following order case service definitions. These service definitions belong to the Orders service definition category, which stores services for order-related issues. When creating a case, agents can select the desired service definition in the [case type selector](csm-case-type-select-modals.md).

**Note:** The system administrator needs to activate these service definitions. Navigate to **All** &gt; **Customer Service** &gt; **Administration** &gt; **Service Definitions** and filter the list to show service definitions from the Order Case \[sn\_order\_case\] table.

For more information about service definitions and categories, see the following topics:

-   [Service definitions](csm-service-definitions.md)
-   [Service definition categories](csm-service-definitions.md#section_e5p_mzw_jzb)

<table id="table_xwk_wkw_tcc"><thead><tr><th>

Service definition

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Sales Order Change Request

</td><td>

Request a change to sales order lines on a single order or multiple sales orders.-   Type: Post Sales
-   Table: Order Case \[sn\_order\_case\]
-   Products: All
-   Service definition category: Orders

</td></tr><tr><td>

Sales Order Dispute

</td><td>

Dispute an entire order or specific order lines on an order.-   Type: Post Sales
-   Table: Order Case \[sn\_order\_case\]
-   Products: All
-   Service Definition Category: Orders

</td></tr></tbody>
</table>## Special handling notes configuration

The Order Operations Case Management application includes a configuration for special handling notes on the Order Case table \[sn\_order\_case\]. To view this record, navigate to **Special Handling Notes** &gt; **Configuration**.

The configuration for the Order Case table includes the following related fields:

-   Account
-   Contact
-   Product Model
-   Sold Product
-   Install Base
-   Assigned to

This configuration includes a condition that creates special handling notes for order cases that have a priority of P1 - Critical. It also includes the following information:

-   **Short description**: Urgent issue reported.
-   **Message**: This case is set as critical. Follow up immediately.

For more information, see [Special handling notes](c_OnScreenAlerts.md).

## Order case archive rules

The Order Operations Case Management application includes archive rules that archive older order cases.

<table id="table_bmp_vgp_2dc"><thead><tr><th>

Archive rule

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Archive Order Case

</td><td>

This rule archives order case records that have been closed for more than 2 years. Archiving these order case records also archives the following records:-   Order case tasks
-   Order case lines
-   Case line characteristics
-   Order case line tasks

</td></tr><tr><td>

Archive Order Case Line

</td><td>

This rule archives order case line records that have been closed for more than 2 years. Archiving these order case records also archives the following records:-   Case line characteristics
-   Order case line tasks

</td></tr></tbody>
</table>Order case records that have been archived for more than 5 years are deleted. Deleting these records also deletes the following records:

-   Order case tasks
-   Order case line items
-   Case line characteristics
-   Order case line tasks

## Order case workflows

The Order Operations Case Management application includes subflows that provide the mapping between a customer order and an order case. These subflows are used when an agent creates an order case from a customer order.

These subflows create the data mapping between two different entities: 1\) the customer order and 2\) the order case. For example, when mapping a customer order to order case line items, the entities share some fields such as **Account**, **Contact**, and **Contract**. The data mapping copies these field values from the customer order to the order case line items on the order case.

-   If an order case is created by selecting **Create case** from a customer order:
    -   The **Scope of request** is set to **Multiple orders**.
    -   The mapping copies the data from the selected order headers to create order case line items.
-   If an order case is created by selecting **Create case** from the Order Line Items list on a customer order.
    -   The **Scope of request** is set to **Specific line items, Single order**.
    -   The mapping copies the data from selected order lines to create case line items as well as copies the order line characteristics to case line item characteristics.

Subflows:

-   **Primitives - Order to order case for multiple request**
    -   Inputs: Order IDs, Order Case ID
    -   Action: Create Case Line Item - Multiple Request

        Creates an order case line item on the order case based on the customer order.

-   **Primitives - Order to order case for single request**
    -   Inputs: Order ID, Order Case ID, Selected IDs
    -   Action: Create Case Line Item - Single Request

        Creates order case line items based on the selected order line items from the customer order.


To view these subflows, navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio** and select **Subflows** on the Workflow Studio homepage.

