---
title: Tables installed with the SAP publisher pack
description: Tables are installed with the Software Asset Management Professional for SAP plugin. The tables store data pulled from the SAP systems.
locale: en-US
release: xanadu
product: Software Asset Management
classification: software-asset-management
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Software Asset Management publisher pack for SAP, Supported software publisher licenses, Software Asset Management, IT Asset Management]
---

# Tables installed with the SAP publisher pack

Tables are installed with the Software Asset Management Professional for SAP plugin. The tables store data pulled from the SAP systems.

**Note:** Use the Application Files table to see all components installed with the SAP publisher pack. For more information, see [Find components installed with an application](https://www.servicenow.com/docs/access?context=find-components&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

Demo data is available for the SAP publisher pack.

## Tables

<table id="table_cvs_4lx_4fb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Named User Type Role \[samp\_named\_user\_type\_has\_role\]

</td><td>

Roles assigned to each named user type.

</td></tr><tr><td>

SAP Client \[samp\_sap\_client\]

</td><td>

Remote Function Call \(RFC\) destination connecting Advanced Business Application Programming \(ABAP\) systems to external systems.To view the table, navigate to **SAP Compliance and Optimization** &gt; **Administration** &gt; **SAP Clients**.

</td></tr><tr><td>

SAP Connection \[samp\_sap\_connection\]

</td><td>

SAP system connections.To view the table, navigate to **SAP Compliance and Optimization** &gt; **Administration** &gt; **SAP Connections**.

</td></tr><tr><td>

SAP Engine Usage \[samp\_sap\_sw\_client\_access\]

</td><td>

Most recent engine usage measurements for SAP clients based on the license metric for each engine.

</td></tr><tr><td>

SAP License Metric \[samp\_sap\_license\_metric\]

</td><td>

This table is populated by the ServiceNow Content Service. It’s a list of all license metrics that are used by SAP engines.To view the table, navigate to **SAP Compliance and Optimization** &gt; **Administration** &gt; **Engines**.

 **Note:** The table is periodically updated with new data from the Content Service. New license metrics may be added, and existing license metrics may be deactivated to reflect current SAP licensing. To view your software models that have deactivated license metrics, navigate to **SAP Compliance and Optimization** &gt; **Administration** &gt; **Software Models with Deactivated SAP License Metrics**.

</td></tr><tr><td>

SAP License Metric Measurement \[samp\_sap\_license\_metric\_measurement\]

</td><td>

Monthly engine usage measurements for SAP clients based on the license metric for each engine.To view the table, navigate to **SAP Compliance and Optimization** &gt; **Licensing** &gt; **All SAP Engines**.

</td></tr><tr><td>

SAP Roles \[samp\_sap\_role\]

</td><td>

SAP roles pulled from the SAP systems.

</td></tr><tr><td>

SAP System User \[samp\_sap\_system\_user\]

</td><td>

Discovered users pulled from the SAP systems.To view the table, navigate to **SAP Compliance and Optimization** &gt; **Licensing** &gt; **All SAP Users**.

 **Note:** The Discovered Users table \[samp\_discovered\_user\] maps the discovered SAP users to system user records in the Users table \[sys\_user\].

</td></tr><tr><td>

SAP User Activity \[samp\_sap\_user\_activity\]

</td><td>

Data related to a user’s activity on an SAP client, such as the amount of time spent on an SAP system or the number of database records created or updated.

</td></tr><tr><td>

SAP User Roles \[samp\_sap\_user\_has\_role\]

</td><td>

SAP users and their assigned roles.

</td></tr><tr><td>

SAP Web Activity \[samp\_sap\_web\_activity\]

</td><td>

Data related to web activity or RFC connections performed in the SAP client, such as the number of calls or amount of data received or sent by each connection.

</td></tr><tr><td>

SAP User Active Transactions \[samp\_named\_user\_type\_has\_transactions\]

</td><td>

Data related to a named user's transaction activity on an SAP client. User transaction activity is based on SAP transaction codes, which are shortcuts for performing transactions or tasks on an SAP client. For example, the ME21N transaction code enables you to create a purchase order in SAP.

</td></tr><tr><td>

SAP USMM Rules \[samp\_sap\_usmm\_rule\]

</td><td>

USMM rules information from all connected SAP applications.

</td></tr></tbody>
</table>**Note:** Staging tables for SAP data are also installed.

Data from SAP is also stored in some additional tables that aren't part of the SAP publisher pack.

-   Price list data is pulled and stored in the Price List table \[samp\_price\_list\].

    To view the table, navigate to **SAP Compliance and Optimization** &gt; **Administration** &gt; **Price Lists**.

-   Named user types are pulled and stored in the Named User Type table \[samp\_named\_user\_type\].

    To view the table, navigate to **SAP Compliance and Optimization** &gt; **Administration** &gt; **Named User Types**.

-   The Digital Access details such as Client, User name, Document type, Document type count, and Measured by are pulled from the SAP systems and stored in the SAP Digital Access \[samp\_sap\_digital\_access\] table.

    To view the data in the table, navigate to **All** &gt; **Software Asset Workspace** &gt; **License operations** &gt; **Discovery** &gt; **SAP Digital Access Data**.


**Parent Topic:**[Software Asset Management publisher pack for SAP](sap-publisher-pack.md)

**Related topics**  


[Deploy the ABAP program for SAP](../task/import-abap-program-sap.md)

[Establish an SAP connection](../task/add-sap-connection.md)

[Create entitlements for SAP](../task/create-entitlement-sap.md)

[Create software models for SAP](../task/add-software-model-sap.md)

[Create a custom SAP named user type](../task/create-named-user.md)

[Map a role to a named user type](../task/create-named-user-type-role-mapping.md)

[Create custom SAP price lists](../task/create-sap-pricelist.md)

[Import custom SAP named user types](../task/import-custom-sap-named-user-type.md)

[Import custom SAP price lists](../task/import-custom-sap-price-list.md)

[SAP USMM-based optimization](usmm-optimization.md)

[User transaction activity for named user types](sap-named-user-transaction-activity.md)

[Self-declaring SAP engine license usage](self-declaring-sap-engine-usage.md)

[Software Publisher Analytics dashboard for SAP in Software Asset Management classic](../reference/dashboard-sap.md)

[Publisher overview for SAP in the Software Asset Workspace](../reference/publisher-overview-sap.md)

