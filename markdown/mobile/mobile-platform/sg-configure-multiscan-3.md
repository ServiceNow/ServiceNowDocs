---
title: Configure your action item to use your grouped input UI parameters
description: Configure the action item on your button so that you can use the values that your users scan in.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/mobile/mobile-platform/sg-configure-multiscan-3.html
release: zurich
product: Mobile Platform
classification: mobile-platform
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure grouped input, Barcode scanning, Considerations before implementation, Configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Configure your action item to use your grouped input UI parameters

Configure the action item on your button so that you can use the values that your users scan in.

## Before you begin

Role required: admin

## Procedure

1.  From your grouped input record, click the reference icon \(\[Omitted image "gac-info-icon.png"\] Alt text: Reference icon\) next to the **Button** field, and then click **Open record** to open your function record.

2.  From your function record, click the reference icon \(\[Omitted image "gac-info-icon.png"\] Alt text: Reference icon\) next to the **Action item** field, and then click **Open record** to open your action item record.

3.  Modify the **Execution Script** field to use your grouped input UI parameters.

    These parameters are contained within the **input** object. You can access the parameters by using this format: ``input.grouped_input_name`[`input index`]["`UI Parameter Name`"]`. For example, if you have a grouped input called `add_asset` that has a UI parameter named `Serial number`, you would use `input.add_asset[0]["Serial number"]` to access the first serial number asset.

    In this example, the script checks the length of **input.add\_asset** to see how many items were scanned. It then adds an asset for each scanned item using the scanned-in serial number and asset tag.

    \[Omitted image "grouped-input-script-example.png"\] Alt text: Grouped input used in an execution script example.

    **Note:**

    -   The action item type must be set to **Script** to display this **Execution Script** field.
    -   In the above script example, the addAssetToStockroom\(\) function is a custom function that has been created by the user. For more information, see [Configure an action function](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/mobile/mobile-platform/sg-studio-config-action-function.md).

## What to do next

Your button is configured for multi-scan, and your users can begin creating records. For information on using the mobile scanning interface, see [Multi-scan for mobile applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/mobile/mobile-platform/sg-multi-scan.md).

**Parent Topic:**[Configure a grouped input for multiple scans](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/mobile/mobile-platform/sg-configure-multiscan.md)

