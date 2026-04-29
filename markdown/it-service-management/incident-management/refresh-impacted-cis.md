---
title: Refresh impacted services and CIs for incident
description: The impacted services and CIs related list refreshes its records and also the records listed in the Service Offerings and Business Applications related lists based on the affected CIs. You can identify the impacted services and CIs and take necessary action.
locale: en-US
release: australia
product: Incident Management
classification: incident-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Managing incidents, Incident Management, IT Service Management]
---

# Refresh impacted services and CIs for incident

The impacted services and CIs related list refreshes its records and also the records listed in the Service Offerings and Business Applications related lists based on the affected CIs. You can identify the impacted services and CIs and take necessary action.

## Before you begin

Role required: itil, incident\_manager, sn\_incident\_write, or admin

Ensure that you have configured the Business Applications related list.

## About this task

When you refresh impacted services, the Impacted Services/CIs, Business Applications, and the Service Offerings related lists get updated based on the affected CIs. The records in each of the related list are unique even though the impact can be from a single affected CI. The following properties are responsible for this functionality:

-   **Populate Impacted Services based on Affected CIs. Note: This requires any Business Service identified to have previously been converted to an Application Service.** \(**com.snc.incident.refresh\_impacted.include\_affected\_cis**\)
-   **Impacted CIs/Services related list is generated via events. When enabled the refresh will be executed in the background and the user will be notified on completion.** \(**com.snc.incident.refresh\_impacted.event**\)
-   **Populate the Business Application related list for incidents** \(**com.snc.incident.populate\_business\_application**\)
-   **Populate the Service Offering related list for incidents** \(**com.snc.incident.populate\_service\_offering**\)
-   **Populate the Refresh impacted services has been initiated message that is displayed on the UI when the Refresh impacted services UI action is clicked.** \(**com.snc.incident.refresh\_impacted\_services.message.show**\)

    **Note:** By default, the property is set to true.

-   **Control and refresh the creation of live feed messages** \(**com.snc.incident.refresh\_impacted\_notify\_user**\)

    **Note:** By default, the property is marked true.


## Procedure

1.  Navigate to **All** &gt; **Incident** &gt; **Open**.

    **Note:** If the UI16 module link redirection feature is enabled in Service Operations Workspace \(SOW\) and the UI16 module supports the redirect configuration, navigating through UI16 paths automatically redirects you to the equivalent list or record pages in SOW instead of displaying the UI16 forms or lists. For more information, see [Redirect UI16 module links to Service Operations Workspace](../../service-operations-workspace/task/redirect-ui16-module-links-sow.md).

2.  Open the incident record for which you want to refresh the related lists those values are based on affected CIs.

3.  Click the Additional actions icon ![The Additional actions icon](../image/context-menu.png) and then select **Refresh Impacted Services**.

    The records in the Impacted Services/CIs, Business Applications, and Service Offerings related lists are updated.


