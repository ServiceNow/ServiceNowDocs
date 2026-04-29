---
title: Include On-call scheduling users to initiate Microsoft Teams chat
description: Users who are associated with On-Call Scheduling will be displayed on the Selected column in Start Microsoft Teams Chat modal.
locale: en-US
release: australia
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [IT Service Management integration, Microsoft Teams Integration for Employee Experience, Configure, ServiceNow for Microsoft Teams and Microsoft 365, Unified Employee Experience, Employee Service Management]
---

# Include On-call scheduling users to initiate Microsoft Teams chat

Users who are associated with On-Call Scheduling will be displayed on the Selected column in **Start Microsoft Teams Chat** modal.

When initiating a Microsoft Teams chat, users who are part of On-Call Scheduling groups are automatically included in the Selected column of the Start Microsoft Teams Chat modal.

**sn\_tcm\_collab\_hook.on\_call\_tables\_for\_start\_chat\_action** system property is created to support this functionality. You can extend this functionality to modify the tables and requests that determine which on-call users are included.

For more information on On-Call Scheduling, see [On-Call Scheduling](https://www.servicenow.com/docs/access?context=c_OnCallScheduling&version=australia&pubname=australia-it-service-management&ft:locale=en-US).

-   **[Extend On-Call Scheduling users to initiate Microsoft Teams Chat](../task/extend-on-call-users-start-chat-it.md)**  
View the list of On-Call Scheduling users in Start Microsoft Teams chat for a change, request, or a request item.

**Parent Topic:**[Configure IT Service Management integration with Microsoft Teams](sn-ms-teams-config-it.md)

