---
title: Displaying the role hierarchy of a user
description: The role hierarchy node map displays the relationship between the license contributing roles for role-based users and provides insights into the licensing treatment of a user.
locale: en-US
release: zurich
product: GRC Common Functions
classification: grc-common-functions
topic_type: concept
last_updated: "2026-05-01"
reading_time_minutes: 1
breadcrumb: [Licensing summary dashboard, Common GRC features, Governance, Risk, and Compliance]
---

# Displaying the role hierarchy of a user

The role hierarchy node map displays the relationship between the license contributing roles for role-based users and provides insights into the licensing treatment of a user.

If a user is assigned a direct role that has child roles, then the user inherits all the permissions of the child roles. In such a case, the license treatment of the user depends on the combination of the roles.

GRC users can have usage-based or role-based use of licenses. If the license usage is usage-based, there’s no role hierarchy for the selected user.

To see the role hierarchy of a user, use either of the following methods:

-   On the GRC licensing summary dashboard, under the License consumption tab, select the user count, then a user and select **Show role hierarchy**.
-   On the GRC licensing summary dashboard, under the Estimated next month usage tab, select the user count, then a user and select **Show role hierarchy**. Or select a user under User role allocation and then select **Show role hierarchy**.

The role hierarchy node map displays the child relationships of a user. If a user has multiple roles assigned, the role hierarchy node map displays the entire hierarchy.

**Note:** Your license consumption is calculated based on the licensable roles that are available at the time of calculation. Same roles might not be available at the time you view the role hierarchy node map.

The following illustration shows a sample node map for user Cary Mccamey. Cary has the roles sn\_compliance\_ws.corporate\_compliance\_analyst, and sn\_compliance.manager. The sn\_compliance\_ws.corporate\_compliance\_analyst role contains the sn\_compliance.user and sn\_audit.user roles. Selecting the count on each node expands it further.

![Role hierarchy of a sample user, Cary Maccamey](../image/role-hierarchy-nodemap.png)

**Parent Topic:**[GRC licensing summary dashboard](grc-licensing-summary-dashboard.md)

