---
title: Discovery sensors
description: Every probe in Discovery must have a corresponding sensor to process the data returned.By default, this rule cancels the sensor transaction if it takes more than 20 minutes to complete.
locale: en-US
release: yokohama
product: Discovery
classification: discovery
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Discovery probes and sensors, Discovery, ITOM Visibility, IT Operations Management]
---

# Discovery sensors

Every probe in Discovery must have a corresponding sensor to process the data returned.

For example, if incoming data is the result of a WMI probe, then the WMI sensor is triggered to process the payload.

**Note:** If you create a multiprobe, you must create a multisensor to process the data returned from this probe.For details, see [Multiprobes and Multisensors](r_MultiprobesIncludedWithDiscovery.md#).

Navigate to **Discovery** &gt; **Discovery Definition** &gt; **Sensors** and edit or create a sensor.

<table id="table_llf_4lv_tp"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Enter a unique probe name.

</td></tr><tr><td>

Reacts to probe

</td><td>

Select the probe whose payload this sensor must process.

</td></tr><tr><td>

Sensor Class \[sys\_class\_name\]

</td><td>

Select the type of sensor to create:-   Import Export Map: This option is not currently used.
-   MultiSensor: Multisensors process the data returned from multiprobes. Select this type to create a multisensor that responds to the simple probes used in a multiprobe.
-   Sensor: Select this type if this sensor is a simple sensor that responds to a simple probe.

</td></tr><tr><td>

Description

</td><td>

Enter an optional description of the sensors function.

</td></tr><tr><td>

Sensor type \[sensor\_type\]

</td><td>

Specify how the results from the probe are processed.-   Classifier: This field is not currently used.
-   Java: This field is not currently used.
-   Javascript: Returned data from the probe is processed in the sensor itself, outside the application, and is visible to the user. This is the most common sensor type.
-   Multiline Text: This field is not currently used.
-   XML: The XML data from the probe is broken into pieces. Some pieces can be used to launch other probes that the original sensor needs to complete all the necessary information about a device.

</td></tr><tr><td>

Active

</td><td>

Select this option to enable or disable the sensor.

</td></tr><tr><td>

Script

</td><td>

Enter a script to run when processing the probe. You can use the g\_probe\_parameters hashmap in a sensor script to set probe parameters for any configured, triggered probes. For example, this code sets a '**node\_port**' parameter to 16001 for all triggered probes.```
g_probe_parameters['node_port']=16001;
```

</td></tr><tr><td>

Responds to probes

</td><td>

Use this related list to specify the simple probe within a multiprobe whose payload this multisensor must process. This list is available for multisensors only.

</td></tr><tr><td>

Triggers probes

</td><td>

Use this related list to specify which probes this sensor can start for additional exploration.

</td></tr><tr><td colspan="2">

These fields can be added by configuring the form

</td></tr><tr><td>

Field

</td><td>

Description

</td></tr><tr><td>

Agent

</td><td>

Enter the ECC queue type to match this sensor with.

</td></tr><tr><td>

Apply Defaults

</td><td>

Select this option to apply default sensor values.

</td></tr><tr><td>

Classification type

</td><td>

Select the classification type associated with this sensor.

</td></tr><tr><td>

Coalesce

</td><td>

Enter the field to match against when determining whether to coalesce.

</td></tr><tr><td>

Condition script

</td><td>

Create a predetermined requirement for this sensor to run.

</td></tr><tr><td>

Data option

</td><td>

Select how to treat imported sensor data. Options include:-   Insert and Update
-   Insert Only
-   Update Only

</td></tr><tr><td>

External names

</td><td>

Enter a name to tag the sensor data.

</td></tr></tbody>
</table>**Parent Topic:**[Discovery probes and sensors](../concept/c_DiscoveryProbesAndSensors.md)

## Cancel sensor transaction by duration

By default, this rule cancels the sensor transaction if it takes more than 20 minutes to complete.

### Before you begin

Role required: admin

### About this task

If the Discovery sensor transaction takes more than 20 minutes to complete, the following actions occur:

-   The associated ECC Queue input record is set to the error state.
-   The *Discovery Status Completed Count* is updated.
-   An error message is logged, for example:

    ```
    Sensor error when processing Linux - Storage: Transaction cancelled: maximum execution time exceeded
    ```

-   The remainder of the discovery continues to run.

    This behavior is provided by the Discovery Sensors Transaction Quota Rule. This rule is active by default.

    You can disable the rule and you can modify the amount of time that has elapsed before the rule takes effect. Accessing this record requires the admin role.


### Procedure

1.  To disable the rule, navigate to **System Definition** &gt; **Quota Rules**.

    The **Transaction Quotas** plugin must be active.

2.  Search on the name `*Discovery` to filter the list of rules.

3.  In the name column, click **Discovery Sensors**.

4.  To modify the amount of time, edit the **Maximum Duration** field of the rule.

    The value is in seconds.


