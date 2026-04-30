---
title: Create a Script Include to transform Scratchpad updates from the provider
description: To transform Scratchpad updates sent by your provider into a format required for the Zero Touch request flow, you must have a Script Include with the method transformScratchPadToHAMZTRFormat.
locale: en-US
release: xanadu
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Manage hardware asset requests using the Zero Touch request flow, Using Hardware Asset Management, Hardware Asset Management, IT Asset Management]
---

# Create a Script Include to transform Scratchpad updates from the provider

To transform Scratchpad updates sent by your provider into a format required for the Zero Touch request flow, you must have a Script Include with the method **transformScratchPadToHAMZTRFormat**.

In the confirmation and shipment stages of the Zero Touch request flow, your provider should ideally send Scratchpad updates to your ServiceNow instance in a particular format. For details, see [Use the Scratchpad to complete your request fulfillment tasks](using-scratchpad-for-provider-updates.md). However, if your provider's Scratchpad update isn't in the required format, you can transform it by using a Script Include with the method **transformScratchPadToHAMZTRFormat**.

Consider the following points when you create the Script Include:

-   The Script Include is accessible from the Asset Management Common application scope by adjusting the following settings on the application resource record:
    -   Set the **Accessible from** field to **All application scopes**.
    -   Set the **Caller Access** field to **None** to make sure the caller access isn't restricted.
-   Define the method **transformScratchPadToHAMZTRFormat** in the following format:

    ```
    /*** Input to the following method is scratchpad value of type JSON ***/
    transformScratchPadToHAMZTRFormat: function (input) {
    // Logic to transform the input to the expected format
    // This method should return a value of type JSON with expected format
    }
    ```


