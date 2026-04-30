---
title: APIs for IT to OT and OT to IT conversion
description: There are 2 APIs used for handling refresh workflow scenarios for converting IT to Operational Technology \(OT\) and vice versa with the OT Asset Management application.
locale: en-US
release: xanadu
product: Operational Technology Manager
classification: operational-technology-manager
topic_type: reference
last_updated: "2024-12-31"
reading_time_minutes: 1
breadcrumb: [Reference, Operational Technology Manager, Operational Technology]
---

# APIs for IT to OT and OT to IT conversion

There are 2 APIs used for handling refresh workflow scenarios for converting IT to Operational Technology \(OT\) and vice versa with the OT Asset Management application.

## APIs used in OT Asset Management

With OT Asset Management, you need to maintain synchronization between asset and configuration item \(CI\) for OT assets. The following APIs are used for IT to OT conversion and OT to IT conversion in the OT Asset Management application.

**Note:** The IT CI class isn't changed. Instead an OT entity record is added, which provides the OT device context.

-   Convert IT to OT Asset API
-   Convert OT to IT Asset API

**Convert IT to OT Asset API**

The Convert IT to OT Asset API is used in refresh workflows where an OT configuration item \(CI\) is replaced with a new CI. This API creates a replica of the previous OT entity record, and maps them to the new CI. No changes occur in the previous CI and its related OT entity record. Both the new CI and the previous CI references are used with this API.

**Convert OT to IT Asset API**

The Convert OT to IT Asset API is used if an asset needs to be replaced. The API deletes the OT entity record of the passed CI.

For more information about OT Asset Management, see [OT Asset Management](https://www.servicenow.com/docs/access?context=ot-asset-management&version=xanadu&pubname=xanadu-it-asset-management&ft:locale=en-US).

**Parent Topic:**[Operational Technology Manager reference](operational-technology-manager-reference.md)

