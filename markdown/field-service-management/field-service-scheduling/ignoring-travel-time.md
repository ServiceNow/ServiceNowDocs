---
title: Ignoring travel time of field service agents
description: You can choose to assign work order tasks to the highest ranked agents without taking into account travel time.
locale: en-US
release: australia
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Assigning tasks using Dynamic Scheduling, Scheduling and dispatching, Use, Field Service Management]
---

# Ignoring travel time of field service agents

You can choose to assign work order tasks to the highest ranked agents without taking into account travel time.

## Enabling ignore travel

The Ignore travel option in the work order task enables dynamic scheduling to assign work order tasks automatically to the highest ranked agents. If the highest ranked agent is not available due to time off, the task is assigned to the next highest ranked agent.

Enabling the **com.snc.dynamic.scheduling.ignoreAgentTravelTimeDuringScheduling** property displays the Ignore Travel option in work order tasks. For more information about enabling a dynamic scheduling property, see [Properties installed with Field Service Management](../../planning-and-policy/reference/r_PropInstallWFieldServMgmnt.md).

The Ignore Travel option does not appear in the work order task form by default so you have to add it manually. For more information, see [Configuring the form layout](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/configure-form-layout.md).

Note the following parameters related to dynamic scheduling when Ignore travel is enabled:

-   Double booking must be enabled for the system to assign tasks to the agent automatically.
-   If access hours are defined in a work order task, the system ignores the defined access hours limit when auto-assigning that task to agents.

