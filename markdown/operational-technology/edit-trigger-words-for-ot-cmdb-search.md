---
title: Edit trigger words for OT CMDB search
description: Edit the trigger words used in the Operational Technology \(OT\) Configuration Management Database \(CMDB\) search feature to optimize search results specific to OT.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-11-07"
reading_time_minutes: 1
breadcrumb: [Configure, Now Assist for Operational Technology Manager \(OTM\), Operational Technology]
---

# Edit trigger words for OT CMDB search

Edit the trigger words used in the Operational Technology \(OT\) Configuration Management Database \(CMDB\) search feature to optimize search results specific to OT.

## Before you begin

Role required: admin

## About this task

Optionally, you can update the `sn_mfg_common.ot_cmdb_search_trigger_words` system property as needed to include additional search keywords.

## Procedure

1.  Navigate to **All** &gt; **Indsutrial Workspace Admin** &gt; **Workspace System Properties**.

2.  Under the **OT CMDB Search** section, update the Additional OT CMDB Search trigger words in a comma-separated format \(`sn_mfg_common.ot_cmdb_search_trigger_words`\) system property with additional keywords as needed.

    The following keywords are included for the OT CMDB search feature.

    -   OT
    -   Operational Technology
    -   CNC
    -   Control system
    -   Control module
    -   DCS
    -   DPU
    -   EWS
    -   Field device
    -   Historian
    -   HMI
    -   IED
    -   OPC client
    -   OPC server
    -   PLC
    -   RTU
    -   QICS
    -   Industrial 3d printer
    -   Industrial actuator
    -   Industrial drive
    -   Industrial sensor
    -   Industrial robot
    -   Industrial printer
    -   supervisory system
    -   SCADA client
    -   SCADA server
3.  Select **Save**.


**Parent Topic:**[Configuring Now Assist for Operational Technology Manager \(OTM\)](../concept/configuring-na-otm.md)

