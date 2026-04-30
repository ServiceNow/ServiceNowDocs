---
title: User Presence Indicator
description: User presence indicator helps the agents to know the status of the users in Microsoft Teams before the agent can initiate a chat using Microsoft Teams.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Integration for Employee Experience, Setup for integrating pre-published apps, Setup the Servicenow instance, Microsoft Teams and Microsoft 365, Integrate, ServiceNow for Microsoft Teams and Microsoft 365, Employee Service Management]
---

# User Presence Indicator

User presence indicator helps the agents to know the status of the users in Microsoft Teams before the agent can initiate a chat using Microsoft Teams.

By default, the agents can view the status of the users when they launch the Start chat modal in the ServiceNow instance.

When you are upgrading the application, you must reauthorize the **Request Based Chat** from **Install Azure Apps** page. For more information on installing the Azure apps, refer [Grant permissions to required Microsoft Azure apps](../task/authorize-multi-tenant-apps-mt.md).

![Install Azure apps](../images/install-azure-apps-0011.png)

The system takes 60 minutes to display the user presence status in the start chat modal for the first use when you upgrade to IT Service Management integration with Microsoft Teams v2.5.0 or Collaboration Services v3.5 applications.

The status of the user from Microsoft Teams is mapped into the ServiceNow instance as depicted in the table.

|User status in Microsoft Teams|Status shown in Start Chat modal|
|------------------------------|--------------------------------|
|'Available', 'AvailableIdle'|available|
|'Busy', 'BusyIdle', 'DoNotDisturb'|busy|
|'Offline', 'PresenceUnknown'|offline|
|'Away', 'BeRightBack'|away|

The user presence status is cached for 180 seconds, this implies if a user is “online” in Microsoft Teams, the Start Chat modal displays the user status as “online” until 180 seconds. If the user status is modified, the system fetches the user status after the interval of 180 seconds and updates the status in the Start Chat modal.

The time interval to cache the user status is configurable by a system property `sn_tcm_collab_hook.teams.presence_status_cache_invalidate_duration`. You can modify the time interval to retain the user presence status. For more information, refer [Configure cache duration for the user presence status](../task/configure-cache-duration.md).

-   **[Configure cache duration for the user presence status](../task/configure-cache-duration-mt.md)**  
You can modify the system property to configure the cache duration to retain the user presence status of the Microsoft Teams user.

**Parent Topic:**[Setup for integrating pre-published apps with Microsoft Teams for Employee Experience](c_employee_ex_tnt.md)

