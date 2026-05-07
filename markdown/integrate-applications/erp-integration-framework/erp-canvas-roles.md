---
title: Zero Copy Connector for ERP roles
description: Administrators assign roles to give team members permission to configure or use Zero Copy Connector for ERP \(Enterprise Resource Planning\).
locale: en-US
release: australia
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [erp, canvas, erp canvas, integration, data hub, zero, copy, connector, sap, role]
breadcrumb: [Configure, Zero Copy Connector for ERP, Workflow Data Fabric]
---

# Zero Copy Connector for ERP roles

Administrators assign roles to give team members permission to configure or use Zero Copy Connector for ERP \(Enterprise Resource Planning\).

**Important:** When you assign Zero Copy Connector for ERP \(Enterprise Resource Planning\) roles to a user, you must include the scope. For example, assign the `sn_erp_integration.erp_admin` role, not just `erp_admin`.

For more on assigning roles, see [Assign a role to a user](https://www.servicenow.com/docs/access?context=t_AssignARoleToAUser&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

To learn more about product-specific \(granular\) admin roles, see [Platform security granular admin roles](https://www.servicenow.com/docs/access?context=platsec-granular-roles&version=australia&pubname=australia-platform-security&ft:locale=en-US).

## Zero Copy Connector for ERP roles

**Note:** All required roles are the same across development and production instances. However, only sn\_erp\_integration.erp\_user is required to read data in a production instance.

<table id="table_jj3_ykv_cwb"><thead><tr><th>

Role

</th><th>

Description

</th><th>

Additional access

</th></tr></thead><tbody><tr><td>

sn\_erp\_integration.erp\_admin

</td><td>

Grants the user access to updating the application setup.

</td><td>

Granular admin role for Zero Copy Connector for ERP that contains the sn\_erp\_integration.erp\_user role.

 For more information on working with granular roles, see [Platform security granular admin roles](https://www.servicenow.com/docs/access?context=platsec-granular-roles&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

sn\_erp\_integration.erp\_ai\_user

</td><td>

Grants the user access to ERP-related generative AI capabilities including skills, agentic workflows, and agents.

</td><td>

None

</td></tr><tr><td>

sn\_erp\_integration.erp\_data\_pill

</td><td>

Grants the user read access to all the tables needed for making Financial Services Remote Tables requests.This role can be combined with any single Financial Services Remote Tables role. For example, combining sn\_erp\_integration.erp\_data\_pill and sn\_erp\_integration.sap\_company\_code\_user enables the list of SAP Company Codes.

</td><td>

None

</td></tr><tr><td>

sn\_erp\_integration.erp\_mid\_server

</td><td>

Grants the user access to use the API to enable the MID Server to send attachments back to the ServiceNow instance.

</td><td>

-   connection\_admin
-   import\_admin
-   import\_scheduler
-   import\_set\_loader
-   import\_transformer
-   snc\_platform\_rest\_api\_access
-   sn\_erp\_integration.erp\_admin

</td></tr><tr><td>

sn\_erp\_integration.erp\_user

</td><td>

Grants the user read access for all remote tables.

</td><td>

Contains sn\_erp\_integration.erp\_data\_pill and all the data model-specific roles listed in the next section.

</td></tr><tr><td>

sn\_erp\_integration.etl\_user

</td><td>

Grants the user the ability to trigger the ETL process.

</td><td>

Contains sn\_erp\_integration.erp\_data\_pill and import\_admin.

</td></tr></tbody>
</table>## Additional ERP data model roles

If users need access to work with specific ERP data models, such as purchasing or invoices, assign them the following roles for Zero Copy Connector for ERP.

|Persona|Role|
|-------|----|
|Company code user|sn\_erp\_integration.sap\_company\_code\_user|
|Country user|sn\_erp\_integration.sap\_country\_user|
|Currency user|sn\_erp\_integration.sap\_currency\_user|
|Customer invoice user|sn\_erp\_integration.sap\_customer\_invoice\_user|
|Distribution channel user|sn\_erp\_integration.sap\_distribution\_channel\_user|
|Division user|sn\_erp\_integration.sap\_division\_user|
|Language user|sn\_erp\_integration.sap\_language\_user|
|Material stock user|sn\_erp\_integration.sap\_material\_stock\_user|
|Purchase document user|sn\_erp\_integration.sap\_purchase\_document\_user|
|Purchasing organization user|sn\_erp\_integration.sap\_purchasing\_organization\_user|
|Sales customer user|sn\_erp\_integration.sap\_sales\_customer\_user|
|Sales delivery user|sn\_erp\_integration.sap\_sales\_delivery\_user|
|Sales document user|sn\_erp\_integration.sap\_sales\_document\_user|
|Sales organization user|sn\_erp\_integration.sap\_sales\_organization\_user|
|Sales revenue recognition user|sn\_erp\_integration.sap\_sales\_revenue\_recognition\_user|
|Table metadata user|sn\_erp\_integration.sap\_table\_metadata\_user|
|Transport user|sn\_erp\_integration.sap\_transport\_user|
|Vendor invoice user|sn\_erp\_integration.sap\_vendor\_invoice\_user|
|Vendor user|sn\_erp\_integration.sap\_vendor\_user|

**Parent Topic:**[Configuring Zero Copy Connector for ERP](../concept/erp-integration-configuration-overview.md)

