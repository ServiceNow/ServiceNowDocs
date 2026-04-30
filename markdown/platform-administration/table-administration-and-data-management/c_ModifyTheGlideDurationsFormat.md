---
title: Modify the Glide durations format
description: To convert fields that are displayed in milliseconds \(such as 'Resolution Time' on the Incident table\) to a duration format \(Months/Days/Hours/Seconds\), populate the attribute field on the dictionary with: format=glide\_duration.
locale: en-US
release: xanadu
product: Table Administration and Data Management
classification: table-administration-and-data-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Altering tables and fields using dictionary attributes, Managing tables and indexes, Table administration, Tables and data, Configure core features, Administer the ServiceNow AI Platform]
---

# Modify the Glide durations format

To convert fields that are displayed in milliseconds \(such as 'Resolution Time' on the Incident table\) to a duration format \(Months/Days/Hours/Seconds\), populate the attribute field on the dictionary with: `format=glide_duration`.

Now the value is displayed as a duration in lists and can be utilized in the Configure Calculations functions. This may be useful to illustrate ITIL KPIs such as Mean Time To Repair.

![](../image/DurationDict.png "Field dictionary")

Results in list:

![](../image/DurationResult.png "Results in list")

**Parent Topic:**[Altering tables and fields using dictionary attributes](../../reference-pages/concept/c_DictionaryAttributes.md)

