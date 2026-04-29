---
title: Establish an SAP connection using OAuth 2.0
description: Create a connection profile to establish a connection between your SAP system and your ServiceNow instance using OAuth 2.0 authentication.
locale: en-US
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Software Asset Management publisher pack for SAP, Supported software publisher licenses, Software Asset Management, IT Asset Management]
---

# Establish an SAP connection using OAuth 2.0

Create a connection profile to establish a connection between your SAP system and your ServiceNow instance using OAuth 2.0 authentication.

## Before you begin

Before establishing a connection between SAP and your ServiceNow instance, make sure that the following conditions are met:

-   Verify if your SAP system network is accessible to external applications like ServiceNow.
-   If external connections are blocked, install a MID Server. A MID Server enables communication and data movement between a ServiceNow instance and external applications or data sources. For instructions, see [Installing the MID Server](https://www.servicenow.com/docs/access?context=mid-server-installation&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

If you already have a MID Server installed in the network and connected to your ServiceNow instance, this SAP connection automatically uses it.

Role required: sam\_admin

## Procedure

1.  Navigate to **All** &gt; **SAP Compliance and Optimization** &gt; **Connection Setup** and select **New**.

2.  On the form, fill in the fields.

<table id="table_llt_dlc_hfb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of connection profile.

</td></tr><tr><td>

Default price list

</td><td>

Default price list that should be considered for reconciliation.

</td></tr><tr><td>

Connection type

</td><td>

Values include:-   Basic Auth
-   OAuth 2.0


</td></tr><tr><td>

Connection URL

</td><td>

The base URL to connect to the SAP instance.

</td></tr><tr><td>

OAuth Client ID

</td><td>

Client ID for your SAP connection.

</td></tr><tr><td>

OAuth Client Secret

</td><td>

Client secret for your SAP connection.

</td></tr></tbody>
</table>    **Note:** You can get the OAuth Client ID and Client Secret at the time of registering your SAP application.

3.  Select **Submit**.

    The initial connection is established.

4.  Select the SAP connection and review the fields on the record.

<table id="table_vzk_fwb_qfb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the connection profile. The value is generated in the SAP Connection Setup form.

</td></tr><tr><td>

Default price list

</td><td>

Default price list that should be considered for reconciliation. The value is generated in the SAP Connection Setup form.

</td></tr><tr><td>

Use USMM Role Optimization

</td><td>

The option to specify USMM role-based optimization that must be applied during reconciliation.

</td></tr><tr><td>

Last run

</td><td>

Date and time when the data was last pulled for the SAP connection.

</td></tr><tr><td>

REST message

</td><td>

REST message that contains the SAP API information.

</td></tr><tr><td>

OAuth entity profile

</td><td>

The OAuth entity profile that contains the credentials for the connection.

</td></tr><tr><td>

Active

</td><td>

Option that indicates that the SAP connection is active.

</td></tr><tr><td>

Connection type

</td><td>

This field is automatically populated based on your connection type.

</td></tr><tr><td class="sub-head" colspan="2">

User Mapping

</td></tr><tr><td>

SAP user field

</td><td>

SAP users across different clients that are mapped to a corresponding ServiceNow user.

</td></tr><tr><td>

User field

</td><td>

ServiceNow user field.**Important:** Changing the values in the User Mapping fields after data is pulled results in the loss of the mapping between discovered users and system users. The mapping between discovered users and the **Rights used by** and **Rights needed by** fields is also lost.

</td></tr><tr><td colspan="2">

Configuration

</td></tr><tr><td>

Fetch roles

</td><td>

Controls the data pull from SAP for roles data.

</td></tr><tr><td>

Fetch engine usage

</td><td>

Controls the data pull from SAP for engine usage data.

</td></tr><tr><td>

Fetch digital access usage

</td><td>

Controls the data pull from SAP for digital access usage data.

</td></tr><tr><td>

Fetch activity

</td><td>

Controls the data pull from SAP for user activity and web activity data.

</td></tr><tr><td>

Fetch user transactions

</td><td>

Controls the data pull from SAP for user transaction activity data.

</td></tr></tbody>
</table>5.  Generate an access token by selecting the **Get OAuth Token** related link.

    **Note:** You must be in the local network of SAP to generate the access token.

    1.  Log in using your SAP credentials.

    2.  In the Access Permission Request dialog box, select **Allow** for the scopes that you had added during the application registry.

        A message is displayed on the SAP Connection form indicating that the OAuth refresh token is available.

6.  If you're running the latest version of the ABAP program, test your SAP connection by selecting the **Test SAP Connection and Version** related link.

    **Note:** If you upgrade your ServiceNow instance, you must download and deploy the new version of the ABAP program and reconfigure a service provider with the SOA Manager.

7.  Send a request to the custom ABAP program to collect the SAP data into the custom tables again by selecting the **Refresh data in SAP** related link.

8.  If the SAP data you pulled is corrupted, view current data by selecting the **Pull all SAP Data to ServiceNow** related link.

    SAP data is scheduled to be pulled regularly.

9.  Update connection information by selecting the **Update connection** related link.

10. Select **Submit**.

11. View SAP clients in the **SAP Clients** related list.

    The SAP clients are generated when SAP data is pulled during the scheduled job.

12. Select **Update**.


## Result

The SAP connection is established.

## What to do next

You can start creating software models and entitlements.

**Parent Topic:**[Software Asset Management publisher pack for SAP](../concept/sap-publisher-pack.md)

**Related topics**  


[Tables installed with the SAP publisher pack](../concept/component-installed-sap-plugin.md)

[Deploy the ABAP program for SAP](import-abap-program-sap.md)

[Establish an SAP connection using basic authentication](add-sap-connection.md)

[Create entitlements for SAP](create-entitlement-sap.md)

[Create software models for SAP](add-software-model-sap.md)

[Create a custom SAP named user type](create-named-user.md)

[Map a role to a named user type](create-named-user-type-role-mapping.md)

[Create custom SAP price lists](create-sap-pricelist.md)

[Import custom SAP named user types](import-custom-sap-named-user-type.md)

[Import custom SAP price lists](import-custom-sap-price-list.md)

[SAP USMM-based optimization](../concept/usmm-optimization.md)

[User transaction activity for named user types](../concept/sap-named-user-transaction-activity.md)

[Self-declaring SAP engine license usage](../concept/self-declaring-sap-engine-usage.md)

[Software Publisher Analytics dashboard for SAP in Software Asset Management classic](../reference/dashboard-sap.md)

[Publisher overview for SAP in the Software Asset Workspace](../reference/publisher-overview-sap.md)

