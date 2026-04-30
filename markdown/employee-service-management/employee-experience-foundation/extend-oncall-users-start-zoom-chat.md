---
title: Extend On-call users for Start Zoom Team Chat
description: Shows the list of On-call users in Start Zoom Team Chat for a change, request, or a request item.
locale: en-US
release: zurich
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure Chat group to include On-call Scheduling users for Start Zoom Team Chat, Chat-specific configuration for Collaboration services for Zoom, Enhance employee experience by integrating ServiceNow with Zoom, Integrate, ServiceNow for Zoom, Unified Employee Experience, Employee Service Management]
---

# Extend On-call users for Start Zoom Team Chat

Shows the list of On-call users in Start Zoom Team Chat for a change, request, or a request item.

## Before you begin

Role required: admin

## Procedure

1.  In the navigation filter, enter `sys_properties.list`.

    The entire list of properties in the System Properties \[sys\_properties\] table appears.

2.  Enter `sn_tcm_collab_hook.zoom_on_call_tables_for_start_chat_action` in the **Name** search field.

3.  Select **sn\_tcm\_collab\_hook.zoom\_on\_call\_tables\_for\_start\_chat\_action** system property.

4.  Enter the table names in the **Value** field to which you need to extend the functionality.

    For example: change, request.

5.  Select **Update**.


**Parent Topic:**[Configure Chat group to include On-call Scheduling users for Start Zoom Team Chat](../concept/oncall-users-start-zoom-chat.md)

