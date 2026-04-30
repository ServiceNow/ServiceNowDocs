---
title: Get field recommendations
description: Get incident field recommendations in Service Operations Workspace while creating or updating incidents.
locale: en-US
release: xanadu
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Recommended Actions for ITSM in Service Operations Workspace, Use, Service Operations Workspace for ITSM, IT Service Management]
---

# Get field recommendations

Get incident field recommendations in Service Operations Workspace while creating or updating incidents.

## Before you begin

Role required: admin

## About this task

-   Field recommendations are only available in the Advanced Recommended actions for ITSM application, which requires the ITSM Pro package subscription.
-   The recommendations associated with field recommendations must be active.
-   The field recommendations must be configured in the Recommended Actions. For more information, see [Create a field recommendation in Recommended Actions](https://www.servicenow.com/docs/access?context=ra-csm-field-recs-create&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US).

## Procedure

1.  Navigate to **All** &gt; **Workspace Experience** &gt; **Workspaces** &gt; **Service Operations Workspace**.

2.  Perform one of the following actions to start creating an incident.

<table id="choicetable_vrd_rrt_tsb"><thead><tr><th align="left" id="d427928e103">

Option

</th><th align="left" id="d427928e106">

Description

</th></tr></thead><tbody><tr><td id="d427928e112">

**From the List menu**

</td><td>

1.  From the primary navigation, select the list icon \(![List icon](../../itsm-manager-workspace/image/lists_icon.png)\).
2.  Select the add icon \(![add icon](../image/add-icon.png)\) next to the **List** tab.
3.  Select **New Incident**.


</td></tr><tr><td id="d427928e151">

**From an incident list**

</td><td>

1.  Navigate to a list of incidents.

**Note:** The following lists are available for incidents:

    -   Assigned to me
    -   Unassigned
    -   Open
    -   Resolved
    -   All
2.  Select **New**.


</td></tr><tr><td id="d427928e191">

**From an interaction**

</td><td>

1.  Open an interaction.
2.  From the record page, select **Create incident**.


</td></tr></tbody>
</table>3.  In the **Description** field and the **Short description** field, enter a description and a short description for the incident.

4.  Perform one of the following actions to get the field recommendations:

    -   If you're on a version prior to 4.2, then press the tab key to get the field recommendations.

        The fields are auto-filled or recommended based on the output defined in the recommendation.

        ![UI of the field recommendations on a new incident form when using a version prior to 4.2.](../image/ra-field-recommendation.png)

    -   If you're using a version after 4.2, select the required fields to see the field recommendations in the drop-down list.

        ![UI of the field recommendations on a new incident form when using a version after 4.2.](../image/ra_get_field_recommendations_drop-down.png)


**Parent Topic:**[Recommended Actions for ITSM in Service Operations Workspace](../concept/recommended-actions-for-itsm-in-service-operations-workspace.md)

