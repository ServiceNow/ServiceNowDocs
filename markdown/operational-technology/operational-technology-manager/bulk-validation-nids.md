---
title: Validate multiple NIDS sensors at once
description: Validate multiple NIDS sensors at once through a bulk validation so that you can edit your records more quickly and efficiently.
locale: en-US
release: yokohama
product: Operational Technology Manager
classification: operational-technology-manager
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Managing Network Intrusion Detection System appliances, Use, Operational Technology Manager, Operational Technology]
---

# Validate multiple NIDS sensors at once

Validate multiple NIDS sensors at once through a bulk validation so that you can edit your records more quickly and efficiently.

## Before you begin

Role required: cmdb\_nids\_admin

## About this task

You can use bulk validation to validate multiple NIDS sensors at once instead of individually validating each NIDS sensor.

**Note:** Carefully review the NIDS sensors by discovery source and proceed with caution while bulk validating.

## Procedure

1.  Navigate to **All** &gt; **Network IDS Appliance \(NIDS\)** &gt; **Sensors**.

2.  Select the check boxes the sensor records that you want to validate.

3.  Select the **Validate Sensors** button.


## Result

If the sensors you validated have a **Life Cycle Stage Status** of In Use, a successful validation message appears.

If the selected sensors have a **Life Cycle Stage Status** of Learning Mode or the **Validated** column is set to true, an error message appears alerting you that one or more sensors in learning mode haven’t been validated or already validated. You should consider changing the **Life Cycle Stage Status** column to In Use to proceed with the bulk validation.

**Parent Topic:**[Managing Network Intrusion Detection System appliances](managing_network_intrusion_detection_system_nids_appliances.md)

