---
title: Find the cause of a "Probe not found" error
description: Verify the correct sys\_id of the probe associated with the probe parameter in the payload of the ECC Queue input record.
locale: en-US
release: yokohama
product: Discovery
classification: discovery
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Discovery error messages, Discovery monitoring and issue resolution, Discovery, ITOM Visibility, IT Operations Management]
---

# Find the cause of a "Probe not found" error

Verify the correct sys\_id of the probe associated with the **probe** parameter in the payload of the ECC Queue input record.

## Before you begin

Role required: discovery\_admin or admin

## Procedure

1.  Record the sys\_id of the probe as it appears in the ECC Queue payload.

    ![ECC Queue payload sample](../image/DiscoveryProbeNotFoundError.png "ECC Queue payload sample")

2.  Navigate to **Discovery Definition** &gt; **Probes** and open the record for the probe you want to inspect.

3.  Right-click in the record's header bar.

4.  Select **Copy sys\_id** from the context menu.

    Follow browser instructions to copy the sys\_id if browser security measures restrict this function.

5.  Compare this value with the sys\_id of the probe from the payload.

    If the sys\_id of the probe record does not match the value in the payload, try to determine the cause of the incorrect value.


**Parent Topic:**[Discovery error messages](../concept/c_DiscoveryErrorMessages.md)

**Related topics**  


[Find the cause of a sensor error message](t_FindTheCauseOfASensorErrorMessage.md)

[Find the cause of a "No Sensor Defined" error message](t_IdentifyCauseNoSenDefEM.md)

[Fix the cause of a sensor error message](t_FixTheCauseOfASensorErrorMessage.md)

