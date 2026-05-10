---
title: Establish an SAP connection using basic authentication
description: After you have deployed the Advanced Business Application Programming \(ABAP\) program in your SAP system, create a connection profile to establish a connection between your SAP system and your ServiceNow instance using basic authentication.
locale: en-US
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Software Asset Management publisher pack for SAP, Supported software publisher licenses, Software Asset Management, IT Asset Management]
---

# Establish an SAP connection using basic authentication

After you have deployed the Advanced Business Application Programming \(ABAP\) program in your SAP system, create a connection profile to establish a connection between your SAP system and your ServiceNow instance using basic authentication.

## Before you begin

Before establishing a connection between SAP and your ServiceNow instance, check if your SAP system network is accessible to external applications like ServiceNow. If external connections are blocked, you can install a MID Server. A MID Server enables communication and data movement between a ServiceNow instance and external applications or data sources. For instructions, see [Installing the MID Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/mid-server-installation.md).

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
**Important:** The Basic Auth authentication method is planned for deprecation by SAP. You should use the OAuth 2.0 authentication for a secure and compliant integration. For more information, see [Establish an SAP connection using OAuth 2.0](add-sap-connection-oauth.md).

</td></tr><tr><td>

WSDL

</td><td>

Web Service Description Language \(WSDL\) URL from the SOA manager that includes an IP address that is used to connect to the SAP system.**Note:** Don’t change the SAP WSDL name. The WSDL service definition name must be /NOW/SAMP and the service binding name must be NOW\_SAMP. The only WSDL name that can be changed is the WSDL generation name.

</td></tr><tr><td>

User name

</td><td>

User name used to connect to the SAP system.

</td></tr><tr><td>

Password

</td><td>

Password used to connect to the SAP system.

</td></tr></tbody>
</table>3.  Select **Submit**.

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

SOAP message

</td><td>

SOAP message that has the SAP WSDL information.

</td></tr><tr><td>

Credential alias

</td><td>

Connection alias that contains the credentials for the connection. The connection alias resolves your connection and credentials at runtime.

</td></tr><tr><td>

Active

</td><td>

Option that indicates that the SAP connection is active.

</td></tr><tr><td>

Connection type

</td><td>

This field is automatically populated based on your connection type.

</td></tr><tr><td colspan="2">

User Mapping

</td></tr><tr><td>

SAP user field

</td><td>

SAP users across different clients that are mapped to a corresponding ServiceNow user.

</td></tr><tr><td>

User field

</td><td>

ServiceNow user field.**Note:** Changing the values in the User Mapping fields after data is pulled results in the loss of the mapping between discovered users and system users. The mapping between discovered users and the **Rights used by** and **Rights needed by** fields is also lost.

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
</table>5.  View the credentials that you used to create the connection in the SAP Credentials related list.

    **Note:** Only one credential record should be active for a given SAP connection. To determine the roles associated with your credentials, contact your SAP Basis administrator. Your administrator assigns respective roles to your SAP user ID credentials.

6.  If you're running the latest version of the ABAP program, test your SAP connection by selecting the **Test SAP Connection and Version** related link.

    **Note:** If you upgrade your ServiceNow instance, you must download and deploy the new version of the ABAP program and reconfigure a service provider with the SOA Manager.

7.  Send a request to the custom ABAP program to collect the SAP data into the custom tables again by selecting the **Refresh data in SAP** related link.

8.  If the SAP data you pulled is corrupted, you can view current data by selecting the **Pull all SAP Data to ServiceNow** related link.

    SAP data is scheduled to be pulled regularly.

9.  Update connection information or switch to a different authentication method by selecting the **Update connection** related link.

    1.  In the Update Connection dialog box, select the authentication method.

    2.  Enter the connection details based on the authentication method that you select.

    3.  Select **Submit**.

10. View SAP clients in the **SAP Clients** related list.

    The SAP clients are generated when SAP data is pulled during the scheduled job.

11. Select **Update**.


## Result

You can start creating software models and entitlements.

**Parent Topic:**[Software Asset Management publisher pack for SAP](../concept/sap-publisher-pack.md)

**Related topics**  


[Tables installed with the SAP publisher pack](../concept/component-installed-sap-plugin.md)

[Deploy the ABAP program for SAP](import-abap-program-sap.md)

[Establish an SAP connection using OAuth 2.0](add-sap-connection-oauth.md)

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

