---
title: Validate NIDS sensors
description: Validate the Network IDS \(NIDS\) sensors once they're imported to prepare for the device import. Sensors only pass the validation if they aren't in learning mode as such sensors are not eligible for device import.
locale: en-US
release: zurich
product: Operational Technology Manager
classification: operational-technology-manager
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Service Graph Connector for Microsoft Defender for IoT \(Azure\), Integrate, Operational Technology Manager, Operational Technology]
---

# Validate NIDS sensors

Validate the Network IDS \(NIDS\) sensors once they're imported to prepare for the device import. Sensors only pass the validation if they aren't in learning mode as such sensors are not eligible for device import.

## Before you begin

It's recommended that you have the CSDM plugin installed. The Service Graph Connector aligns with the life cycle data models as per the CMDB standards. For more information, see [Implementing the CSDM framework in stages](https://www.servicenow.com/docs/access?context=csdm-implementation-stages&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).

Role required: cmdb\_nids\_admin

**Note:** An NIDS appliance in ServiceNow represents a Microsoft Defender for IoT \(Azure\) sensor.

## About this task

The **Life Cycle Stage** and **Life Cycle Stage Status** fields are used to capture the learning mode of a sensor. If the Life Cycle Stage field is set to **Operational** and Life Cycle Stage Status is set to **Learning Mode**, then validation is unsuccessful. If the Life Cycle Stage Status field is set to **In Use**, the validation is successful.

## Procedure

1.  Navigate to **All** &gt; **Network IDS Appliances \(NIDS\)** &gt; **Sensors**.

2.  Select the sensor record that you want to validate.

3.  In the NIDS Assigned Meta Data section, add values for the sensor that you want to be assigned to the detected devices.

4.  From the NIDS Admin Configuration section, make sure that the **Life Cycle Stage Status** field value isn't **Learning Mode**.

    Otherwise, the validation fails.

5.  Make sure that the **NIDS network type** field is set based on the NIDS network location.

    For example, you can select an NIDS network type of **IT** for a data center deployment of the NIDS, or an NIDS network type of **OT** for an industrial deployment on an Industrial/OT network.

    If you select OT, the OT device details are created for all devices.

6.  When the attributes are correctly filled out, select **Validate**.

    **Note:**

    NOTE: The attributes passed from the sensor to the devices are defined in the sn\_cmdb\_ci\_class.nids\_map\_fields system property. The following list is the default list of attributes.

    -   assigned\_to
    -   location
    -   company
    -   owned\_by
    -   managed\_by
    -   supported\_by
    -   change\_control
    -   support\_group
    -   managed\_by\_group
    -   assignment\_group
    -   zone
    -   isa\_entity\_site \(only available if you have the Industrial Process Manager application installed\)

**Parent Topic:**[Service Graph Connector for Microsoft Defender for IoT \(Azure\)](../concept/integration-sgc-microsoft-defender-iot-azure.md)

