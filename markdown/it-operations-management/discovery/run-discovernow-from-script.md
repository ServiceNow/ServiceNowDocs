---
title: Run DiscoverNow from a script
description: You can run DiscoverNow from a script, such as a background job, a business rule, or web services.
locale: en-US
release: yokohama
product: Discovery
classification: discovery
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Schedule a horizontal discovery, Running discoveries in your network, Discovery, ITOM Visibility, IT Operations Management]
---

# Run DiscoverNow from a script

You can run DiscoverNow from a script, such as a background job, a business rule, or web services.

## Before you begin

Role required: admin

## Procedure

1.  Create the following script:

    ```
    var d = new Discovery();
    var statusID = d.discoveryFromIP(TARGET_IP, TARGET_MIDSERVER);
    ```

    The **discoveryFromIP** method takes two arguments: *IP* and *MID Server*. The *IP* argument is mandatory, but the *MID Server* argument is optional.

2.  To choose the MID Server, supply either the *sys\_id* or name of the MID Server as the argument.

    If you do not name a MID Server, the system attempts to find a valid one automatically. A valid MID Server has a status of **Up** and can discover the given IP address. If the system finds a valid MID Server and runs a Discovery, the **discoveryFromIP** method returns the *sys\_id* of the Discovery status record. If no MID Server can discover this IP address, the method returns the value **undefined**.

    If you manually specify the TARGET\_MIDSERVER, the system validates the given value and ensures that the MID Server table contains the specified MID Server record. If the validation passes, the discoveryFromIP method returns the sys\_id of the discovery status record. If the validation fails, the method return the value **undefined**.


