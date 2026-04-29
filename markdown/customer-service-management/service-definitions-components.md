---
title: Components installed with case types
description: Several types of components are installed with the Customer Service Case Types plugin \(com.snc.csm\_case\_types\), including components that support the service definitions feature.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Customer service case types, Case management, Organize agent workspaces, Configure, Customer Service Management]
---

# Components installed with case types

Several types of components are installed with the Customer Service Case Types plugin \(com.snc.csm\_case\_types\), including components that support the service definitions feature.

## Tables installed with case types

The following tables are installed with the Customer Service Case Types \(com.snc.csm\_case\_types\) plugin.

<table id="table_qdp_bbj_fwb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Case Type\[sn\_case\_type\]

</td><td>

This table stores the defined case types.For more information, see [Customer Service case types](../concept/customer-service-case-types.md).

</td></tr><tr><td>

Service Definition\[sn\_case\_type\_selection\]

</td><td>

This table stores the defined service definitions.The service definition feature adds the following fields to the Service Definition table:

-   Domain Path
-   Playbook Record Generator
-   Active
-   Number

For more information, see [Service definitions](../concept/csm-service-definitions.md).

</td></tr><tr><td>

Service Definition Category\[sn\_csm\_case\_types\_service\_category\]

</td><td>

This table stores the categories that are created for service definitions.

</td></tr><tr><td>

Service Definition Category Relationships\[sn\_csm\_case\_types\_service\_category\_rel\]

</td><td>

This table stores the service definitions that are associated with a service definition category.

</td></tr><tr><td>

Product Service Relationship\[sn\_csm\_case\_types\_product\_service\_rel\]

</td><td>

This table stores the products that are linked to a service definition.For more information about these relationships, see [Associate a product with a service definition](../task/service-def-associate-products.md).

</td></tr><tr><td>

Service to Service Relationship\[sn\_csm\_case\_types\_service\_to\_service\_rel\]

</td><td>

This table stores relationships that have been configured between services. For example, related services that have been added to a service definition.

</td></tr><tr><td>

Catalog Service Relationship\[sn\_csm\_case\_types\_catalog\_service\_rel\]

</td><td>

This table stores the catalog items that are linked to a service definition.For more information, see [Configure catalog items for a service definition](../task/service-def-config-catalog-items.md).

</td></tr><tr><td>

Service Definition User Criteria\[sn\_csm\_case\_types\_service\_user\_criteria\]

</td><td>

This table stores the user criteria that has been configured for a service definition record. The system uses this criteria to filter the services that are available to users in the service selector when creating a case. For more information, see [Configure user criteria for a service definition](../task/configure-user-criteria-for-a-service-definition.md).

</td></tr><tr><td>

Service Definition Customer Criteria\[sn\_csm\_case\_types\_service\_customer\_criteria\]

</td><td>

This table stores the customer criteria that has been configured for a service definition record. The system uses this criteria to filter the services that are available to customers. For more information, see [Configure customer criteria for a service definition](../task/configure-customer-criteria-for-a-service-definition.md).

</td></tr></tbody>
</table>## Roles installed with case types

The following service definition roles are installed with the Customer Service Case Types \(com.snc.csm\_case\_types\) plugin.

<table id="table_kkn_mbb_4vb"><thead><tr><th>

Role

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Service definition admin\[sn\_csm\_case\_types.service\_definition\_admin\]

</td><td>

Administrator role for the [Customer Service case types](../concept/customer-service-case-types.md) tables. Users with this role can view, create, update, and delete service definitions, service definition categories, and service definition category relationships.

</td><td>

-   sn\_csm\_case\_types.service\_definition\_manager
-   sn\_service\_org.service\_criteria\_delete

</td></tr><tr><td>

Service definition manager\[sn\_csm\_case\_types.service\_definition\_manager\]

</td><td>

Manager role for the [Customer Service case types](../concept/customer-service-case-types.md) tables. Users with this role can view, create, and update service definitions, service definition categories, and service definition category relationships.

</td><td>

-   sn\_csm\_case\_types.service\_definition\_report\_view
-   sn\_csm\_case\_types.service\_definition\_all\_table\_viewerr
-   sn\_service\_org.service\_criteria\_write
-   sn\_service\_org.service\_criteria\_create
-   sn\_service\_org.service\_criteria\_read

</td></tr><tr><td>

Service definition viewer\[sn\_csm\_case\_types.service\_definition\_viewer\]

</td><td>

Users with this role can view service definitions, service definition categories, and service definition category relationships.

</td><td>

sn\_service\_org.service\_criteria\_read

</td></tr><tr><td>

Service definition report viewer\[sn\_csm\_case\_types.service\_definition\_report\_view\]

</td><td>

Provides report view access to service definition related tables.

</td><td>

None

</td></tr><tr><td>

Service definition all table viewer\[sn\_csm\_case\_types.service\_definition\_all\_table\_viewer\]

</td><td>

Provides view access to the service definition tables. Users with this role can view service definitions, service definition categories, and service definition category relationships.

</td><td>

None

</td></tr></tbody>
</table>## Properties installed with case types

The following properties are added with the Customer Service Case Types plugin. These properties control the version of the case type selector screen that is displayed to agents. For more information, see [Case type selector screen](../concept/csm-case-type-select-modals.md).

<table id="table_dht_2j2_dwb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_csm\_case\_types.case\_type\_single\_field\_select

</td><td>

Set this property to true to enable the case type single select feature in CSM Configurable Workspace. When enabled, an agent can use this feature to create a case of a specific type with a single selection in the case type selector screen.-   **Type:** true \| false
-   **Default value:** false
-   **Location:** System Property \[sys\_properties\] table

</td></tr><tr><td>

sn\_csm\_case\_types.service\_definition\_select

</td><td>

Set this property to true to enable the Product Service Select version of the case type selector screen. When enabled, an agent can use this screen to create a record based on the selected product or service.-   **Type:** true \| false
-   **Default value:** true
-   **Location:** System Property \[sys\_properties\] table

 This property overrides the **sn\_csm\_case\_types.case\_type\_single\_field\_select** property.

-   When set to true, the system displays the Product Service Select screen.
-   When set to false, the system uses the value of the **sn\_csm\_case\_types.case\_type\_single\_field\_select** property.
-   If both properties are set to true, the **sn\_csm\_case\_types.service\_definition\_select** property takes precedence.
-   If both properties are set to false, the system displays the multi-select screen.

</td></tr><tr><td>

sn\_csm\_case\_types.service\_definition\_select\_count

</td><td>

Determines the number of the products and services displayed in the Product Service Select screen.-   **Type:** integer
-   **Default value:** 25
-   **Location:** System Property \[sys\_properties\] table

</td></tr><tr><td>

sn\_csm\_case\_types.get\_case\_types\_roles

</td><td>

Stores the admin and agent roles that can access the Case Type Selector and getCaseTypes API. Roles are listed in the **Value** field in a comma-separated list. To add a role, append the role at the end of the list.-   **Type:** string
-   **Default value:**

itil,admin,sn\_customerservice\_agent,sn\_customerservice.consumer\_agent

-   **Location:** System Property \[sys\_properties\] table

</td></tr></tbody>
</table>## Extension points installed with case types

Extension points enable you to extend the functionality of an application and integrate customizations without altering the application code. Extension points are stored in the Extension Point \[sys\_extension\_point\] table.

The CSMServiceDefinitionIntegrations extension point returns a list of products that is available to agents in the **Product** field on Product Service Select version of the [case type selector screen](../concept/csm-case-type-select-modals.md). Out of box, this list is based on customer context and displays the sold products and install base items owned by the customer.

To access this extension point, navigate to **All** &gt; **System Extension Points** &gt; **Scripted Extension Points** and select **CSMServiceDefinitionIntegrations**.

To modify this extension point:

1.  Select the **Create implementation** related link on the extension point record.
2.  Modify the **Script** field and add an API to return product information.
3.  Select **Update**.

    The system adds the implementation to the Implementations related list on the extension point record.

    **Note:** The implementation with the lowest **Order** number is used to return the list of products.


