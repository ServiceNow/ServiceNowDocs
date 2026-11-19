---
title: Modify the Glide durations format
description: To convert fields that are displayed in milliseconds \(such as 'Resolution Time' on the Incident table\) to a duration format \(Months/Days/Hours/Seconds\), populate the attribute field on the dictionary with: format=glide\_duration.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/platform-administration/table-administration-and-data-management/c\_ModifyTheGlideDurationsFormat.html
release: yokohama
product: Table Administration and Data Management
classification: table-administration-and-data-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Dictionary attributes, Manage tables and indexes, Table administration, Tables and data, Configure core features, Administer the ServiceNow AI Platform]
---

# Modify the Glide durations format

To convert fields that are displayed in milliseconds \(such as 'Resolution Time' on the Incident table\) to a duration format \(Months/Days/Hours/Seconds\), populate the attribute field on the dictionary with: `format=glide_duration`.

Now the value is displayed as a duration in lists and can be utilized in the Configure Calculations functions. This may be useful to illustrate ITIL KPIs such as Mean Time To Repair.

\[Omitted image "DurationDict.png"\] Alt text:

Results in list:

\[Omitted image "DurationResult.png"\] Alt text:

**Parent Topic:**[Altering tables and fields using dictionary attributes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/platform-administration/table-administration-and-data-management/c_DictionaryAttributes.md)

