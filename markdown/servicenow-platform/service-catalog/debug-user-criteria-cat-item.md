---
title: Debug user criteria of a catalog item
description: Debug whether a user can access a catalog item based on the matched user criteria and fix any issues.
locale: en-US
release: yokohama
product: Service Catalog
classification: service-catalog
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Debugging Service Catalog, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Debug user criteria of a catalog item

Debug whether a user can access a catalog item based on the matched user criteria and fix any issues.

## Before you begin

Role required: catalog\_manager, catalog\_admin, or admin

## About this task

You can only debug access issues based on user criteria, but not based on access control list rules \(ACLs\). For information about user criteria, see [Set security for items and categories](../concept/c_ServiceCatalogAccessControls.md).

For any scripted user criteria that uses a session api such as gs.getUserID\(\), the session of the logged-in user is used. Edit the behavior of the scripted user criteria using the pre-defined *user\_id* variable in the **Script** field of a user criteria. For information about the Script field, see [Create a user criteria record in Service Catalog](t_CreateAUserCriteriaRecord.md#).

## Procedure

1.  Navigate to **All** &gt; **Service Catalog** &gt; **Catalog Administration** &gt; **User Criteria Diagnostics**.

    The User Criteria Diagnostics form is displayed.

2.  In the **Select user** field, select the user whose access you want to debug.

3.  In the **Select catalog item** field, select the required catalog item.

4.  Click **Diagnose**.

    ![Screenshot for user criteria diagnostics](../image/UserCriteriaDiag.png)

    -   The item hierarchy is displayed along with an indication of the user's access to each node \(catalog, category, or catalog item\) based on the user criteria associated with the node.

        **Note:**

        -   If the item is available in multiple catalogs or nested categories, the corresponding catalogs and categories are displayed as nodes in a tree format.
        -   If the user matches multiple user criteria associated with the node, then the user can access the node only if the following conditions are met:
            -   The user matches at least one of the user criteria in the **Available For** list.
            -   The user does not match any user criteria in the **Not Available For** list.
    -   All user criteria defined for the item is displayed. For each user criteria, the following information is available:
        -   **User Match**

            ![user match icon](../image/userMatch.png) is displayed if the selected user matches the user criteria.

        -   **Association**

            Association of the node with the user criteria, that is, **Available for** or **Not Available for**.

        -   **User Criteria**

            Name of the user criteria.

5.  To verify if the user can view a node of the hierarchy, click the node.

    User criteria defined at the node is displayed. For example, when you click a node representing a category, the user criteria defined for the category is displayed.

6.  To edit the configuration of a user criteria, click its name under the **User Criteria** column.


**Parent Topic:**[Debugging Service Catalog](../concept/debugging-service-catalog.md)

