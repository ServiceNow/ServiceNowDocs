---
title: Zero Copy Connector for ERP roles
description: Administrators assign roles to give team members permission to configure or use Zero Copy Connector for ERP.
locale: en-US
release: yokohama
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring Zero Copy Connector for ERP, Zero Copy Connector for ERP, Building low-code applications, Developing your application, Building applications]
---

# Zero Copy Connector for ERP roles

Administrators assign roles to give team members permission to configure or use Zero Copy Connector for ERP.

**Important:** When you assign Zero Copy Connector for ERP \(Enterprise Resource Planning\) roles to a user, you must include the scope. For example, assign the `sn_erp_mining.erp_admin` role, not just `erp_admin`.

For more on assigning roles, see [Assign a role to a user](https://www.servicenow.com/docs/access?context=t_AssignARoleToAUser&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

To learn more about managing per-user subscriptions, see [Managing per-user subscriptions in Subscription Management](https://www.servicenow.com/docs/access?context=managing-user-subscriptions-v2&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US) and contact your account representative.

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

Contains sn\_erp\_integration.erp\_user.

</td></tr><tr><td>

sn\_erp\_integration.erp\_data\_pill

</td><td>

Grants the user read access to all the tables needed for making Financial Services Remote Tables requests.This role can be combined with any single Financial Services Remote Tables role. For example, combining sn\_erp\_integration.erp\_data\_pill and sn\_erp\_integration.sap\_company\_code\_user enables the list of SAP Company Codes.

</td><td>

--

</td></tr><tr><td>

sn\_erp\_integration.erp\_mid\_server

</td><td>

Grants the user access to use the API to enable the MID Server to send attachments back to the ServiceNow instance.

</td><td>

--

</td></tr><tr><td>

sn\_erp\_integration.erp\_user

</td><td>

Grants the user read access for all remote tables.

</td><td>

Contains sn\_erp\_integration.erp\_data\_pill and all Financial Services Remote Tables roles.-   sn\_erp\_integration.sap\_company\_code\_user
-   sn\_erp\_integration.sap\_country\_user
-   sn\_erp\_integration.sap\_currency\_user
-   sn\_erp\_integration.sap\_customer\_invoice\_user
-   sn\_erp\_integration.sap\_distribution\_channel\_user
-   sn\_erp\_integration.sap\_division\_user
-   sn\_erp\_integration.sap\_language\_user
-   sn\_erp\_integration.sap\_material\_stock\_user
-   sn\_erp\_integration.sap\_purchase\_document\_user
-   sn\_erp\_integration.sap\_purchasing\_organization\_user
-   sn\_erp\_integration.sap\_sales\_customer\_user
-   sn\_erp\_integration.sap\_sales\_delivery\_user
-   sn\_erp\_integration.sap\_sales\_document\_user
-   sn\_erp\_integration.sap\_sales\_organization\_user
-   sn\_erp\_integration.sap\_sales\_revenue\_recognition\_user
-   sn\_erp\_integration.sap\_vendor\_invoice\_user
-   sn\_erp\_integration.sap\_vendor\_user

</td></tr></tbody>
</table>## Additional ERP data model roles

If users need access to work with specific ERP data models, such as purchasing or invoices, assign them the following roles and access for Zero Copy Connector for ERP.

<table id="table_qh1_fwr_bwb"><thead><tr><th>

Persona

</th><th>

Role

</th><th>

Access

</th></tr></thead><tbody><tr><td>

ERP MID Server user

</td><td>

erp\_mid\_server

</td><td>

-   sys\_attachments
-   sn\_erp\_integration\_queue

</td></tr><tr><td>

Customer invoice user

</td><td>

sap\_customer\_invoice\_user

</td><td>

sn\_erp\_integration\_st\_sap\_customer\_invoice

</td></tr><tr><td>

Material stock user

</td><td>

sap\_material\_stock\_user

</td><td>

sn\_erp\_integration\_st\_sap\_material\_stock

</td></tr><tr><td>

Purchase document user

</td><td>

sap\_purchase\_document\_user

</td><td>

sn\_erp\_integration\_st\_sap\_purchase\_document

</td></tr><tr><td>

Purchasing organization user

</td><td>

sap\_purchasing\_organization\_user

</td><td>

sn\_erp\_integration\_st\_sap\_purchasing\_organization

</td></tr><tr><td>

Sales customer user

</td><td>

sap\_sales\_customer\_user

</td><td>

sn\_erp\_integration\_st\_sap\_sales\_customer

</td></tr><tr><td>

Sales delivery user

</td><td>

sap\_sales\_delivery\_user

</td><td>

sn\_erp\_integration\_st\_sap\_sales\_delivery

</td></tr><tr><td>

Sales document user

</td><td>

sap\_sales\_document\_user

</td><td>

sn\_erp\_integration\_st\_sap\_sales\_document

</td></tr><tr><td>

Sales organization user

</td><td>

sap\_sales\_organization\_user

</td><td>

sn\_erp\_integration\_st\_sap\_sales\_organization

</td></tr><tr><td>

Sales revenue recognition user

</td><td>

sap\_sales\_revenue\_recognition\_user

</td><td>

sn\_erp\_integration\_st\_sap\_sales\_revenue\_recognition

</td></tr><tr><td>

Vendor invoice user

</td><td>

sap\_vendor\_invoice\_user

</td><td>

sn\_erp\_integration\_st\_sap\_vendor\_invoice

</td></tr><tr><td>

Vendor user

</td><td>

sap\_vendor\_user

</td><td>

sn\_erp\_integration\_st\_sap\_vendor

</td></tr></tbody>
</table>**Parent Topic:**[Configuring Zero Copy Connector for ERP](../concept/erp-integration-configuration-overview.md)

