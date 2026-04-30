---
title: Install Workplace PPE Inventory Management
description: You can install Workplace PPE Inventory Management if you have the admin role.Several types of components are installed with Workplace PPE Inventory Management, including tables and user roles.
locale: en-US
release: yokohama
product: Safe Workplace
classification: safe-workplace
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Workplace PPE Inventory Management, Safe Workplace, Health and Safety, Employee Service Management]
---

# Install Workplace PPE Inventory Management

You can install Workplace PPE Inventory Management if you have the admin role.

## Before you begin

Workplace PPE Inventory Management requires the Asset Management plugin \(com.snc.asset\_management\). Asset Management is active by default.

Role required: admin

<table id="table_kxr_yz3_blb"><thead><tr><th>

Type

</th><th>

Instructions

</th></tr></thead><tbody><tr><td>

Commercial on-premise

</td><td>

Visit the ServiceNow® Store to download and install the application.

</td></tr><tr><td>

Federal hosted

</td><td>

See the [Federal downloads for the Emergency Response Management and Safe Workplace suite apps \[KB0030260\]](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030260) article in the Store Help Center for more information.

</td></tr><tr><td>

Federal on-premise

</td><td>

If you are a federal on-premise customer and you would like to install this application, reach out to your sales representative or open a Now Support or HIWAVE ticket. In the ticket, request to be routed to the SHOT team.

 See the [Federal downloads for the Emergency Response Management and Safe Workplace suite apps \[KB0030260\]](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030260) article in the Store Help Center for more information.

</td></tr><tr><td>

On-premise

</td><td>

See the [Commercial downloads for the Emergency Response Management and Safe Workplace suite apps \[KB0030258\]](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030258) article in the Store Help Center for more information.

</td></tr></tbody>
</table>If you've subscribed to the Safe Workplace suite and you already have some of the apps installed, refer to the following order of installation for the remaining apps.

-   Emergency Outreach \(sn\_imt\_checkin\)
-   Employee Health Screening \(sn\_imt\_monitoring\)
-   Workplace PPE Inventory Management \(sn\_imt\_ppe\)
-   Employee Readiness Surveys \(sn\_imt\_readiness\)
-   COVID-19 Global Health Data Set \(sn\_imt\_c19datafeed\)
-   Contact Tracing \(sn\_imt\_tracing\)
-   Emergency Self Report \(sn\_imt\_quarantine\)
-   Workplace Core \(sn\_wsd\_core\)
-   Safe Workplace Dashboard \(sn\_imt\_dashboard\)
-   Emergency Response Management for Now Mobile \(sn\_imt\_mobile\)
-   Employee Travel Safety \(sn\_imt\_travel\)
-   Health and Safety Testing \(sn\_imt\_health\_test\)
-   Vaccination Status \(sn\_imt\_vaccine\)

## Procedure

1.  Navigate to **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Search for `PPE Inventory Management`.

3.  Click **Install**.

    The Application installation dialog box opens.

4.  Load the demo data by selecting the **Load demo data** check box.

    For information about how to install or reinstall demo data after the initial installation, see the [Work around to install demo data if application is already installed \[KB0722909\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0722909) article in the Now Support Knowledge Base.

5.  Click **Install**.

6.  When the installation is complete, click **Close**.


**Parent Topic:**[Workplace PPE Inventory Management](../concept/ppe-inventory-management.md)

## Components installed with Workplace PPE Inventory Management

Several types of components are installed with Workplace PPE Inventory Management, including tables and user roles.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see [Find components installed with an application](https://www.servicenow.com/docs/access?context=find-components&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

Demo data is available for this feature.

### Roles installed

<table id="table_u1t_gb1_wdb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

PPE Inventory Management admin\[sn\_imt\_ppe.ppe\_admin\]

</td><td>

Can create PPE models, manage PPE inventory, and assign PPE to employees.

</td><td>

-   asset
-   inventory\_admin

</td></tr></tbody>
</table>### Tables installed

<table id="table_fbz_45z_vdb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

PPE Model\[sn\_imt\_ppe\_ppe\_model\]

</td><td>

Contains all PPE models.

</td></tr><tr><td>

PPE Stock Log\[sn\_imt\_ppe\_ppe\_stock\_log\]

</td><td>

Contains a log of PPE stock additions over time.

</td></tr><tr><td>

PPE Request\[sn\_imt\_ppe\_ppe\_request\]

</td><td>

Contains all employee requests for PPE.

</td></tr><tr><td>

PPE Assignment Log\[sn\_imt\_ppe\_ppe\_assignment\_log\]

</td><td>

Contains a log of PPE assignments over time.

</td></tr></tbody>
</table>