---
title: GRC licensing summary dashboard
description: Use the GRC licensing summary dashboard to track license usage trends and next month's projected usage. You can see the aggregated counts of license consumption across different product families. You can also search for roles to identify their combined GRC license treatment when these roles are assigned to a user.
locale: en-US
release: xanadu
product: GRC Common Functions
classification: grc-common-functions
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Common GRC features, Governance, Risk, and Compliance]
---

# GRC licensing summary dashboard

Use the GRC licensing summary dashboard to track license usage trends and next month's projected usage. You can see the aggregated counts of license consumption across different product families. You can also search for roles to identify their combined GRC license treatment when these roles are assigned to a user.

The GRC licensing summary dashboard displays the monthly aggregated counts of license consumption across different product families including Integrated Risk Management, Business Continuity Management, and Privacy Management.

You must have the product owner role \(sn\_irm\_shared\_cmn.product\_owner\) to access the dashboard. Navigate to **All** &gt; **GRC Licensing Overview** &gt; **Licensing Summary Dashboard**.

## GRC licensing summary dashboard tabs

The GRC licensing summary dashboard has the following three tabs:

-   License consumption- Shows the license utilization, usage trend analysis using a filter for product family, and license utilization month on month.
-   Estimated next month usage- Shows the estimated license usage for the next month based solely on the current roles assigned to users.
-   Role attribution to licensing mapping- Shows the license mapping of default GRC roles, users license treatment, license treatment for users who are part of a user group based on the roles assigned to the user group, and license treatment based on combination of multiple roles.

<table id="table_tzp_xlk_r2b"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

IRM Operator

</td><td>

Count of IRM Operator for the previous month.**Note:** The IRM Operator card is available only when IRM Operator is selected in the **Product family** field.

</td></tr><tr><td>

IRM Lite Operator

</td><td>

Count of IRM Lite Operator for the previous month.**Note:** The IRM Lite Operator card is available only when IRM Operator is selected in the **Product family** field and the GRC: Business User – Lite application is installed.

</td></tr><tr><td>

PRM Operator

</td><td>

Count of PRM Operator for the previous month.**Note:** The PRM Operator card is available only when PRM Operator is selected in the **Product family** field.

</td></tr><tr><td>

PRM Lite Operator

</td><td>

Count of PRM Lite Operator for the previous month.**Note:** The PRM Lite Operator card is available only when PRM Operator is selected in the **Product family** field and the GRC: Privacy Lite User application is installed.

</td></tr><tr><td>

BCM Operator

</td><td>

Count of BCM Operator for the previous month.**Note:** The BCM Operator card is available only when BCM Operator is selected in the **Product family** field.

</td></tr><tr><td>

BCM Lite Operator

</td><td>

Count of BCM Lite Operator for the previous month.**Note:** The BCM Lite Operator card is available only when BCM Operator is selected in the **Product family** field and the GRC: Business Continuity Management User - Lite application is installed.

</td></tr><tr><td>

Usage trend analysis

</td><td>

Displays the usage patterns of various types of licenses over a specified time period. Use this information to track changes and trends in license consumption over time. Additionally, you can filter the usage trend based on predefined or custom date ranges.

</td></tr><tr><td>

License utilization month on month

</td><td>

Shows the last 12 months usage of different license types, including their accrual periods and counts. Select the counts to view detailed information such as the user, licensable application family, licensing type, and license contributing roles.

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|User|Shows the user name.|
|Licensable application family|Shows the licensable family to which the user belongs to.|
|Licensing type|Shows if the licensing type is usage-based or role-based.|
|License contributing roles|Shows all the roles that contribute to the license treatment of the user.|

<table id="table_zy4_sxl_dcc"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

IRM Operator

</td><td>

Estimated count of IRM Operator for the next month.**Note:** The IRM Operator card is available only when IRM Operator is selected in the **Product family** field.

</td></tr><tr><td>

IRM Lite Operator

</td><td>

Estimated count of IRM Lite Operator for the next month.**Note:** The IRM Lite Operator card is available only when IRM Operator is selected in the **Product family** field and the GRC: Business User – Lite application is installed.

</td></tr><tr><td>

PRM Operator

</td><td>

Estimated count of PRM Operator for the next month.**Note:** The PRM Operator card is available only when PRM Operator is selected in the **Product family** field.

</td></tr><tr><td>

PRM Lite Operator

</td><td>

Estimated count of PRM Lite Operator for the next month.**Note:** The PRM Lite Operator card is available only when PRM Operator is selected in the **Product family** field and the GRC: Privacy Lite User application is installed.

</td></tr><tr><td>

BCM Operator

</td><td>

Estimated count of BCM Operator for the next month.**Note:** The BCM Operator card is available only when BCM Operator is selected in the **Product family** field.

</td></tr><tr><td>

BCM Lite Operator

</td><td>

Estimated count of BCM Lite Operator for the next month.**Note:** The BCM Lite Operator card is available only when BCM Operator is selected in the **Product family** field and the GRC: Business Continuity Management User - Lite application is installed.

</td></tr><tr><td>

User role allocation

</td><td>

Provides an overview of the users, the licensable application family they’re associated with, and the roles assigned to them. Use this information to visualize the estimated license usage for the next month based on the current role allocations to each user.

</td></tr></tbody>
</table><table id="table_vkw_kbd_zcc"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

License treatment of default roles

</td><td>

Provides an overview of the default GRC roles and the licensable application family that they’re mapped with. Seeing which license is tied to the default GRC role helps you identify the correct license treatment for each role.

</td></tr><tr><td>

User\(s\)/User group\(s\) license treatment

</td><td>

Shows the license treatment of a specific user. You can search for users to see which licensable application family they belong to based on their assigned roles.

 Helps you understand the license treatment of a user when added to a user group based on the roles that are assigned to the user group.

</td></tr><tr><td>

License treatment based on roles

</td><td>

Shows the license treatment for a specific combination of roles. You can search for roles to identify their combined GRC license treatment when these roles are assigned to a user.**Note:** The combined role license treatment results are based on customer license entitlements and installed applications.

</td></tr></tbody>
</table>The following illustration shows the tabs, sections, and cards that are available on the GRC licensing summary dashboard:

![GRC licensing summary dashboard](../image/grc-licensing-summary-dashboard.gif "GRC licensing summary dashboard")

-   **[Displaying the role hierarchy of a user](role-hierarchy.md)**  
The role hierarchy node map displays the relationship between the license contributing roles for role-based users and provides insights into the licensing treatment of a user.

**Parent Topic:**[Common Governance, Risk, and Compliance features](common-grc-features.md)

