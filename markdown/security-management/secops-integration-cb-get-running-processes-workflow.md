---
title: Security Operations Carbon Black Integration - Get Running Processes Flow
description: The Security Operations Carbon Black Integration - Get Running Processes is the implementation for the Carbon Black integration launched by the Security Operations Integration - Get Running Process flow.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Security Operations Integration- Get Running Processes capability, Integration capabilities, Security Operations Integration Reference, Security Operations common functionality, Security Operations]
---

# Security Operations Carbon Black Integration - Get Running Processes Flow

The Security Operations Carbon Black Integration - Get Running Processes is the implementation for the Carbon Black integration launched by the Security Operations Integration - Get Running Process flow.

Role required: sn\_si.analyst

![Flow Design for Security Operations Carbon Black Integration - Get Running Processes 1](../image/carbon-black-get-running-proccess-1.png "Carbon Black Get Running Processes") ![Flow Design for Security Operations Carbon Black Integration - Get Running Processes 2](../image/carbon-black-get-running-proccess-2.png "Carbon Black Get Running Processes") ![Flow Design for Security Operations Carbon Black Integration - Get Running Processes 3](../image/carbon-black-get-running-proccess-3.png "Carbon Black Get Running Processes") ![Flow Design for Security Operations Carbon Black Integration - Get Running Processes 4](../image/carbon-black-get-running-proccess-4.png "Carbon Black Get Running Processes") ![Flow Design for Security Operations Carbon Black Integration - Get Running Processes 5](../image/carbon-black-get-running-proccess-5.png "Carbon Black Get Running Processes")

Actions specific to this flow are described here. For more information on other actions, see [Common Security Operations integration flows and orchestration activities](../../security-operations-common/concept/common-wf-activities.md).

-   **[Collect Carbon Black Configurations Flow Action](../reference/collect-cb-config-activity.md)**  
The Collect Carbon Black Configurations flow action gathers configuration information to use in the flow.
-   **[Check MID Server Status](../reference/check-mid-server-status.md)**  
Determines whether the MID Server identified in the **MID Server Host** field of the integration's configuration is up and running. If the field is set to **Any**, the flow action verifies that any MID Server is up and running.
-   **[Get Sensor ID Flow Action](../reference/get-sensor-id-activity.md)**  
The Get Sensor ID flow action gathers sensor identifiers to use in the flow.
-   **[Create Session Flow Action](../reference/create-session-activity.md)**  
The Create Session flow action establishes a Carbon Black session to use in the flow.
-   **[Check Session Status Flow Action](../reference/check-session-status-activity.md)**  
Determines the status of a Carbon Black session within the flow.
-   **[Create Command Process Flow Action](../reference/create-command-process-activity.md)**  
The Create Command Process flow action create a Carbon Black command process to use in the flow .
-   **[Check Command Status and Get Process Flow Action](../reference/check-command-status-get-process-activity.md)**  
Checks the Carbon Black command status and retrieves processes to use in the flow.
-   **[Map Processes Data Flow Action](../reference/map-processes-data-activity.md)**  
The Map Processes Data flow action maps Carbon Black process data within the flow.
-   **[Capability Execution Tracking - Complete Flow Action](../../security-operations-common/concept/capability-execution-tracking-complete.md)**  
The Capability Execution Tracking - Complete flow action updates the audit record when the flow is complete.
-   **[Close Session Flow Action](../reference/close-session-activity.md)**  
Closes a Carbon Black session within the flow.

**Parent Topic:**[Security Operations Integration- Get Running Processes capability](../../security-operations-common/concept/get-running-processes-capability.md)

