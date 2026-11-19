---
title: Edit trigger words for OT CMDB search
description: Edit the trigger words used in the Operational Technology \(OT\) Configuration Management Database \(CMDB\) search feature to optimize OT search results.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/operational-technology/operational-technology-manager/edit-trigger-words-for-ot-cmdb-search.html
release: zurich
product: Operational Technology Manager
classification: operational-technology-manager
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring the OT Manager Foundation, Configure, Operational Technology Manager, Operational Technology]
---

# Edit trigger words for OT CMDB search

Edit the trigger words used in the Operational Technology \(OT\) Configuration Management Database \(CMDB\) search feature to optimize OT search results.

## Before you begin

Role required: admin

## About this task

Optionally, update the `sn_mfg_common.ot_cmdb_search_trigger_words` system property to include additional search keywords.

## Procedure

1.  Navigate to **All** &gt; **Industrial Workspace Admin** &gt; **Workspace System Properties**.

2.  Under the **OT CMDB Search** section, update the Additional OT CMDB Search trigger words in a comma-separated format \(**sn\_mfg\_common.ot\_cmdb\_search\_trigger\_words**\) system property with additional keywords as needed.

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
    -   Industrial 3D printer
    -   Industrial actuator
    -   Industrial drive
    -   Industrial sensor
    -   Industrial robot
    -   Industrial printer
    -   supervisory system
    -   SCADA client
    -   SCADA server
3.  Select **Save**.


**Parent Topic:**[Configuring the OT Manager Foundation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/operational-technology/operational-technology-manager/configuring-na-otm.md)

