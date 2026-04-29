---
title: Create and use an OT device naming strategy
description: Create and use the Operational Technology \(OT\) device naming strategy to create unique names for your OT devices.
locale: en-US
release: australia
product: Operational Technology Manager
classification: operational-technology-manager
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Industrial Core plugin, Reference, Operational Technology Manager, Operational Technology]
---

# Create and use an OT device naming strategy

Create and use the Operational Technology \(OT\) device naming strategy to create unique names for your OT devices.

## Before you begin

Role required: cmdb\_ot\_admin and script\_include\_admin

## About this task

The Industrial Core plugin comes with the **DeviceNamingStrategyHelper** script include, which identifies whether or not to use the device naming strategy. If yes, then the script identifies which naming strategy to use for a given source class. This helps reduce the number of changes that are required for the Service Graph Connector.

## Procedure

1.  Create an OT device naming strategy.

    1.  Switch the **Application scope** from **Global** to the application that you want to create a device naming strategy for.

    2.  Navigate to **All** &gt; **System Extension Points** &gt; **Scripted Extension Points**.

    3.  Search for and open the **OTDeviceNamingStrategyExtPoint** extension point.

    4.  Select the **Create Implementation** related link.

        A script include is created in the application scope you're in.

    5.  Update the **Name** field to a unique name that indicates what type of naming strategy the created script defines.

        **Note:** Ensure you keep the name unique across all Service Graph Connectors as the name is visible in the Class Mapping table form view when you select an existing script from the list of available strategies.

    6.  In the **Script** field, implement the **calculateDeviceName** function.

        Make sure the function returns a string value. You have access to the jsonObj parameter, which is an object with information provided by the caller.

    7.  Select **Update**.

2.  Use an OT device naming strategy.

    1.  Switch the **Application scope** from **Global** to the application that you want to make changes for.

    2.  Identify the logic where the device name is being calculated.

    3.  Initialize the helper script include with your SGC-specific class mapping table name.

        The **OTDeviceNamingStrategyHelpercontains** helper script include contains functions that can identify the correct implementation for the given source class and can calculate the device name.

    4.  Prepare the data that's required for the device name to be calculated based on the naming strategy that you defined.

        The calculateDeviceName function expects following parameters.

        |Parameter|Description|
        |---------|-----------|
        |sourceClassName|Source class name. Ensure the name is in the same format as defined in the Class Mapping table.|
        |jsonObj|Any attributes that you want to pass to the implementation. You can use this in the implementation script include.|

    5.  Call the **calculateDeviceName** function of the helper script include.

    6.  Ensure you have a fallback mechanism for calculating the device name.

        In cases where there was an error in calculating the device name using the naming strategy, the helper script returns device name as an empty string. Additionally, in a case where no device naming strategy is defined, a default device naming logic is required.

    7.  Run the device import for your Service Graph Connector to verify whether the changes are working as expected.


**Parent Topic:**[Industrial Core plugin](../reference/industrial-core-plugin.md)

