---
title: Interaction wrap up timer
description: The interaction wrap up timer displays a countdown of the wrap up duration period in CSM Configurable Workspace.
locale: en-US
release: yokohama
product: Interaction Management
classification: interaction-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Interaction wrap up, Configuring Interaction Management, Interaction Management, Manage people and work capabilities, Extend ServiceNow AI Platform capabilities]
---

# Interaction wrap up timer

The interaction wrap up timer displays a countdown of the wrap up duration period in CSM Configurable Workspace.

The system administrator can configure the display of the wrap up timer by enabling the **Show duration to agent** field on the Interaction Wrap Up Configuration form.

The read-only timer appears in an interaction record's secondary values. Depending on the configuration of the secondary values, these values can be displayed either in the form header or in the contextual side panel.

**Note:** The interaction wrap up timer works in both CSM Configurable Workspace and CSM Agent Workspace but the timer display is only available in CSM Configurable Workspace.

The timer counts down the amount of time specified in the **Duration in seconds** field on the Interaction Wrap Up Configuration form. The background color of the timer changes as it counts down the duration.

|Timer color|Description|
|-----------|-----------|
|Green|Time remaining is between 100% to 50% of duration.|
|Yellow|Time remaining is between 50% and 25% of duration.|
|Orange|Time remaining is between 25% and 0% of duration.|
|Red|When the timer reaches 0.00, the display turns red and then disappears. The system updates the state of the interaction record to Closed Complete.|

**Parent Topic:**[Interaction wrap up](interaction-wrap-up-state.md)

