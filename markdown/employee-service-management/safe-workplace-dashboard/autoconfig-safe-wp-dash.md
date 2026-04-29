---
title: Auto-map a location and create a campus
description: Create multiple campuses automatically by mapping them from locations so that they appear on the Safe Workplace Dashboard.
locale: en-US
release: australia
product: Safe Workplace Dashboard
classification: safe-workplace-dashboard
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Create a campus to appear on the Safe Workplace Dashboard, Safe Workplace Dashboard, Safe Workplace, Health and Safety, Employee Service Management]
---

# Auto-map a location and create a campus

Create multiple campuses automatically by mapping them from locations so that they appear on the Safe Workplace Dashboard.

## Before you begin

Role required: sn\_imt\_dashboard.admin

## Procedure

1.  Navigate to **All** &gt; **Safe Workplace Dashboard** &gt; **Campus Locations**.

2.  Click **Generate Campuses**.

    The Add Locations pop-up appears.

3.  Select all the locations that you want to be a campus.

    The **Populate OpenStreetMap data** scheduled job runs every five \(5\) minutes and queries the Campus Locations \[sn\_imt\_dashboard\_locations\] table. If the latitude and longitude are missing, an open street API is called to fetch the coordinates and update the Campus \[sn\_wsd\_core\_campus\] table by passing the zip code and country name.

4.  Click **Add Locations to Dashboard**.


## Result

A site is created based on the parent name. The parent name is based on the location name. If a region does not exist, a region is created.

**Parent Topic:**[Create a campus to appear on the Safe Workplace Dashboard](../concept/configrng-safe-workplce-dshbrd.md)

