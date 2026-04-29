---
title: Specify the refresh duration for user presence in Service Operations Workspace
description: Define the duration after which the user presence should be refreshed for all collaboration channels in Service Operations Workspace.
locale: en-US
release: australia
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring Service Operations Workspace for ITSM to improve your experience, Configuring Service Operations Workspace for ITSM, Service Operations Workspace for ITSM, IT Service Management]
---

# Specify the refresh duration for user presence in Service Operations Workspace

Define the duration after which the user presence should be refreshed for all collaboration channels in Service Operations Workspace.

## Before you begin

Role required: admin

## About this task

The **sn\_sow\_collab.user\_presence\_refresh\_duration** property specifies the refresh duration of user presence for all collaboration channels in Service Operations Workspace. However, if the user presence refresh duration is also defined for an individual collaboration channel, then the maximum of these two values is considered for that channel.

For example, consider the following scenario where the user presence refresh duration is defined individually for Microsoft Teams and also for all collaboration channels in Service Operations Workspace.

-   The **sn\_tcm\_collab\_hook.teams.presence\_status\_cache\_invalidate\_duration** property value is set to 240 secs. For information about defining the user presence refresh duration for Microsoft Teams, see [Configure cache duration for the user presence status](https://www.servicenow.com/docs/access?context=configure-cache-duration&version=australia&pubname=australia-employee-service-management&ft:locale=en-US).
-   The **sn\_sow\_collab.user\_presence\_refresh\_duration** property value is set to 180 secs.

In this case, the value specified for the **sn\_tcm\_collab\_hook.teams.presence\_status\_cache\_invalidate\_duration** property is considered to refresh the user presence in Microsoft Teams.

## Procedure

1.  From the **All** menu, navigate to **sys\_properties.list**.

2.  Select the **sn\_sow\_collab.user\_presence\_refresh\_duration** property.

3.  In the **Value** field, specify the duration after which you want the user presence to refresh.

4.  Click **Update**.


**Parent Topic:**[Configuring Service Operations Workspace for ITSM to improve your experience](../concept/configuring-sow-to-improve-experience.md)

