---
title: Extend On-Call Scheduling users to initiate Microsoft Teams Chat
description: View the list of On-Call Scheduling users in Start Microsoft Teams chat for a change, request, or a request item.
locale: en-US
release: zurich
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Include On-call scheduling users, HR Service Delivery integration, Microsoft Teams Integration for Employee Experience, Configure, ServiceNow for Microsoft Teams and Microsoft 365, Unified Employee Experience, Employee Service Management]
---

# Extend On-Call Scheduling users to initiate Microsoft Teams Chat

View the list of On-Call Scheduling users in Start Microsoft Teams chat for a change, request, or a request item.

## Before you begin

Role required: admin

## Procedure

1.  In the navigation filter, enter `sys_properties.list`.

    The list of properties in the System Properties \[sys\_properties\] table appears.

    ![System properties list.](../images/sys-properties.png)

2.  In the Name search field, enter `sn_tcm_collab_hook.on_call_tables_for_start_chat_action`.

3.  Select **sn\_tcm\_collab\_hook.on\_call\_tables\_for\_start\_chat\_action** system property.

    ![TCM system property details.](../images/sn-tcm-collab-system-property.png)

4.  In the Value field, provide the tables to which you must extend the functionality.

    Example: change, request.

5.  Select **Update**.


**Parent Topic:**[Include On-call scheduling users to initiate Microsoft Teams chat](../concept/on-call-users-start-chat.md)

