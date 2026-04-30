---
title: Configure property to set default map location for Health and Safety incidents and observations
description: Configure the property that enables users to add default coordinates when the map location isn’t enabled on their device.
locale: en-US
release: yokohama
product: Health and Safety Incident Management
classification: health-and-safety-incident-management
topic_type: task
last_updated: "2025-11-24"
reading_time_minutes: 1
breadcrumb: [Configure settings, Health and Safety Incident Management, Health and Safety, Employee Service Management]
---

# Configure property to set default map location for Health and Safety incidents and observations

Configure the property that enables users to add default coordinates when the map location isn’t enabled on their device.

## Before you begin

Role required: sn\_ohs\_im.admin

## About this task

This property is required to set a default coordinate for the map when using the map location feature to report an incident or an observation.

The Geo map component \[sn\_geo\_map\] must be installed to use this feature. For more information, see [Activate a plugin](https://www.servicenow.com/docs/access?context=t_ActivateAPlugin&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

## Procedure

1.  Navigate to **All** &gt; **Health and Safety** &gt; **Health and Safety administration** &gt; **Properties**.

2.  In the **Default map location fields**, enter the latitude and longitude.

3.  Select **Save**.


## Result

The latitude and longitude are saved as the default coordinates that loads while completing the Health and Safety incidents or observation form.

**Parent Topic:**[Setting up Health and Safety Incident Management](../concept/setting-up-hs-incident-mgmt.md)

