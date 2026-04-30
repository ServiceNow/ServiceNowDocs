---
title: Configure Google Maps to integrate with linear assets
description: Configure the integration between Google Maps and geomaps, a ServiceNow component, that provides Google Maps functionality while working on linear assets.
locale: en-US
release: zurich
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure, Enterprise Asset Management, IT Asset Management]
---

# Configure Google Maps to integrate with linear assets

Configure the integration between Google Maps and geomaps, a ServiceNow component, that provides Google Maps functionality while working on linear assets.

## Before you begin

Role required: sys\_admin

## About this task

sn-geo-map is the UI component used to support the map visualization in linear assets. For more details on geomaps, see the section titled Geo Maps for linear assets in [Linear assets in Enterprise Asset Management](../concept/using-linear-assets.md).

## Procedure

1.  Obtain a Google Maps API key.

    A Google Maps API Key is an alphanumeric key. For information, refer to Google documentation.

2.  In your ServiceNow instance, navigate to **System Properties** &gt; **All Properties**.

3.  Search for the system property `google.maps.key` and open it.

4.  Enter the Google Maps API key in the **Value** field.

5.  Select **Save**.

    Google Maps and geomaps are integrated, enabling you to work on linear assets.


