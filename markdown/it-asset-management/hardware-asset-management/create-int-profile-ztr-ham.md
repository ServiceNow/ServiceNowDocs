---
title: Create a provider integration profile
description: Create a provider integration profile to convert any format of Scratchpad update sent by your provider to a format required for the Zero Touch request flow.
locale: en-US
release: xanadu
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Manage hardware asset requests using the Zero Touch request flow, Using Hardware Asset Management, Hardware Asset Management, IT Asset Management]
---

# Create a provider integration profile

Create a provider integration profile to convert any format of Scratchpad update sent by your provider to a format required for the Zero Touch request flow.

## Before you begin

You must have the Script Include with the method **transformScratchPadToHAMZTRFormat**. For details, see [Create a Script Include to transform Scratchpad updates from the provider](../concept/creating-script-include-for-provide-ztr.md).

Role required: admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Hardware Asset Workspace** &gt; **Asset operations**.

2.  From the **Zero touch** list, select **Provider integration profiles**.

3.  Select **New**.

4.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Provider|Name of the external provider.|
    |API|Name of the Script Include that includes the business logic for transforming the Scratchpad update sent by the provider to the required format.|
    |Active|Option for indicating the status of the provider integration profile.|

5.  Select **Save**.


## Result

The provider integration profile is created and added to the Provider integration profiles list.

