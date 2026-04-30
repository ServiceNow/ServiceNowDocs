---
title: Validate the NIDS
description: Validate the NIDS to import the devices from the ETL that were detected by the sensor. The sensors can only pass the validation if they aren't in learning mode as such sensors aren't eligible for device import.
locale: en-US
release: zurich
product: Operational Technology Manager
classification: operational-technology-manager
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Managing Network Intrusion Detection System appliances, Use, Operational Technology Manager, Operational Technology]
---

# Validate the NIDS

Validate the NIDS to import the devices from the ETL that were detected by the sensor. The sensors can only pass the validation if they aren't in learning mode as such sensors aren't eligible for device import.

## Before you begin

It's recommended that you have the Common Service Data Model plugin installed. The Service Graph Connector aligns with the life cycle data models as per the Configuration Management Database \(CMDB\) standards. For more information, see [Implementing the CSDM framework in stages](https://www.servicenow.com/docs/access?context=csdm-implementation-stages&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).

Role required: cmdb\_nids\_admin

## About this task

The **Life Cycle Stage** and **Life Cycle Stage Status** fields are used to capture the learning mode of a sensor. If the Life Cycle Stage field is set to **Operational** and Life Cycle Stage Status is set to **Learning Mode**, then validation is unsuccessful. If the Life Cycle Stage Status field is set to **In Use**, the validation is successful.

## Procedure

1.  Navigate to **All** &gt; **Network IDS Appliance \(NIDS\)** &gt; **Sensors**.

2.  If there are any management consoles or central managers in the list, do the following actions:

    1.  Click **edit the record**.

    2.  In the **NIDS Admin Configuration** tab, select **Is NIDS manager** to set the **Validated** column true.

3.  In the NIDS Admin Configuration section, make sure that the **Life Cycle Stage Status** value is not Learning Mode.

    Otherwise, the validation fails.

4.  Select the **NIDS network type**.

    The Network type must be selected based on the location of the sensor.

    **Note:** The network type OT creates the OT device record. The network type IT does not create the OT device records.

5.  In the **NIDS Assigned Meta Data** tab, check that all the devices discovered by the NIDS are entered.

6.  Click **Validate**.

    **Note:**

    The zone value is populated by the ETL. If a zone value is manually entered on the NIDS record, it is overridden what is populated by the ETL.

    If the NIDS record is not validated, the devices are not imported from the ETL that were detected by the sensor.


## What to do next

Alternatively, you can validate more than one NIDS sensor through a bulk validation. For more information, see [Validate multiple NIDS sensors at once](bulk-validation-nids.md).

**Parent Topic:**[Managing Network Intrusion Detection System appliances](managing_network_intrusion_detection_system_nids_appliances.md)

