---
title: Digital Portfolio Management homepage default solution cards
description: Digital Portfolio Management uses certain fields to auto-generate a set of default solution cards to display on your DPM homepage. After you add or remove solutions from your homepage, DPM remembers your updates by displaying your personalized solutions cards instead of the auto-generated set.
locale: en-US
release: zurich
product: Digital Portfolio Management
classification: digital-portfolio-management
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Reference, Digital Portfolio Management, IT Service Management]
---

# Digital Portfolio Management homepage default solution cards

Digital Portfolio Management uses certain fields to auto-generate a set of default solution cards to display on your DPM homepage. After you add or remove solutions from your homepage, DPM remembers your updates by displaying your personalized solutions cards instead of the auto-generated set.

## DPM homepage overview

Each time that you log in to the DPM Workspace, the system uses certain fields to display a set of default solution cards. You can use the personalize option to add or remove solutions to your homepage. For more information, see [Personalize the Digital Portfolio Management Workspace home page](../task/dpm-personalize-homepage.md).

After you add or remove solutions, the DPM system remembers your updates in the **dpm\_home\_page\_item** table so that next time you log in to the DPM Workspace, your personalized homepage displays. The system no longer generates a set of default solution cards for you.

**Note:** Each time you access the DPM homepage, the solution card data refreshes, whether you have the auto-generated default solution set or a personalized solution card set.

## System properties for number of solution cards

Two system properties determine the number of solutions cards on your DPM homepage.

<table id="table_ccr_qqy_mzb"><thead><tr><th>

System property

</th><th>

Description

</th><th>

Solution type

</th><th>

Default limit

</th></tr></thead><tbody><tr><td>

dpm.homepage.cmdb\_ci\_service\_limit

</td><td>

The query limit when auto-generating services, service offerings, and service instances for your DPM homepage.

</td><td>

cmdb\_ci\_service

</td><td>

750

</td></tr><tr><td>

dpm.homepage.cmdb\_ci\_business\_app\_limit

</td><td>

The query limit when auto-generating business applications for your DPM homepage.

</td><td>

cmdb\_ci\_business\_app

</td><td>

250

</td></tr></tbody>
</table>These two system properties derive the overall limit on the DPM homepage of 1000. Even after you personalize your DPM homepage, the total number of solutions on your homepage can't exceed 1000.

You can personalize your DPM homepage to adjust the solution card count. For example, you can have 1000 services and zero business applications but the total number of solutions on the DPM homepage can't exceed 1000.

**Important:** An administrator with the sn\_dpm.dpm\_admin role can change the system property limits to more than 1000 solutions on the DPM homepage. However, raising the limit may negatively impact system performance.

 

## Default solution card fields

The DPM application uses certain fields to auto-generate a set of default solution cards to display when you first login to DPM \(before you personalize\).

**Note:** Starting with the Zurich release, the \[cmdb\_ci\_service\_technical\] table is labeled Technology Management Service in the user interface \(formerly labeled Technology management service\). Additionally, the \[service\_offering\] table is labeled Technology Management Offering in the user interface \(formerly labeled Technology management service offering\).

<table id="table_cft_ksw_2zb"><thead><tr><th>

Solution

</th><th>

Solution record name

</th><th>

Fields used for default solution cards

</th></tr></thead><tbody><tr><td>

Service

</td><td>

-   cmdb\_ci\_service
-   cmdb\_ci\_service\_business
-   cmdb\_ci\_service\_technical

</td><td>

-   Owned by
-   Delivery manager
-   Delegate
-   Business relationship manager
-   Business contact
-   Managed by 

</td></tr><tr><td>

Service offering

</td><td>

service\_offering

</td><td>

-   Owned by
-   Delivery manager
-   Delegate
-   Business contact
-   Managed by 

</td></tr><tr><td>

Business application

</td><td>

cmdb\_ci\_business\_app

</td><td>

-   IT application owner
-   Business owner
-   Portfolio manager

</td></tr><tr><td>

Service instance

</td><td>

cmdb\_ci\_service\_auto including dynamic configuration item \(CI\) groups

</td><td>

-   Owned by
-   Managed by 

</td></tr></tbody>
</table>**Parent Topic:**[Digital Portfolio Management reference](dpm-reference-cfw.md)

