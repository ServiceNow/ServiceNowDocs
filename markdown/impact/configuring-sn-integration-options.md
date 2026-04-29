---
title: Configure ServiceNow integration options
description: Perform the following procedure to configure your ServiceNow integration options.The following leading practices are guidelines for creating ServiceNow integration scripts.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Scan Engine integrations, Scan Engine, Platform Health, Using Impact, Impact]
---

# Configure ServiceNow integration options

Perform the following procedure to configure your ServiceNow integration options.

## Before you begin

Role required: Scan Engine Admin \(sn\_se.scan\_engine\_admin\).

## Procedure

1.  Select **ServiceNow instance** as the integration type.

2.  Select the **User story table** for creating tasks in your designated target instance.

    The table must exist in your Source instance as well as the Target instance.

3.  **User story field mapping** contains the script used by the task creation integration for mapping fields from findings to the chosen task table.

    **Note:** This script is executed twice. Once in the Source instance and once in the Target instance.


## ServiceNow integration script leading practices

The following leading practices are guidelines for creating ServiceNow integration scripts.

-   First, check the predefined variable isSourceto ensure that the script executes within the Source environment. Then check the predefined variable isDestination to ensure that the script is being executed in the Destination instance \(usually Production\).
-   The predefined variable payload is an object that can be used to store variables so that they are available in the Destination instance. You should load the payload with data when the script is executing on the Source instance, and extract the payload data when the script is executing on the Destination instance.
-   Use Violation in the script only when it is executing in the Source instance.
-   Use grTaskin the script only when it is executing in the Destination instance.
-   Use isSource in the script only when it is executing in the Source instance.
-   Use isDestination in the script only when it is executing in the Destination instance.
-   The payload object can be used regardless of the environment.

The predefined variables available for ServiceNow integrations are:

<table id="table_vgz_hzx_2hc"><tbody><tr><td>

isSource

</td><td>

True when on the Source instance \(Development\).

</td></tr><tr><td>

isDestination

</td><td>

True when on the Destination instance \(Production\).

</td></tr><tr><td>

payload

</td><td>

The user-defined variable that passes information between the instances.

</td></tr><tr><td>

grFinding

</td><td>

The glide record of the finding that sends the request, on the Defined instance in Source only.

</td></tr><tr><td>

grTask

</td><td>

The glide record being created on the Destination instance.

</td></tr></tbody>
</table>