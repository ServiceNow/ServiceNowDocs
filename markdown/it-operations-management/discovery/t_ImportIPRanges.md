---
title: Import IP ranges into Discovery schedules with import sets
description: One method of entering large numbers of IP networks into Discovery schedules is by using import sets.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/discovery/t\_ImportIPRanges.html
release: australia
product: Discovery
classification: discovery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Discovery IP address configuration, Configuring Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# Import IP ranges into Discovery schedules with import sets

One method of entering large numbers of IP networks into Discovery schedules is by using import sets.

## Before you begin

Role required: discovery\_admin

## About this task

Common groups of IP addresses, known as [ranges](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/discovery-ip-address-configuration.md) can be used in Advanced Discovery schedules.

**Note:** You can also use IPAM integration for entering large numbers of IP networks into Discovery schedules. See [IPAM Integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/cloud-configuration-governance/IPAM-integration.md) for more information.

Use a data source that can be mapped. Include these fields:

-   Start IP: the first IP address in the range \(inclusive\).
-   End IP: the last IP address in the range \(inclusive\).

## Procedure

1.  Navigate to **All** &gt; **System Import Sets** &gt; **Load Data**.

2.  Identify the file or data source that contains the desired information.

3.  Create a table name, such as `ipnetworks`.

4.  Select **Upload an Excel file** and browse to the source file.

5.  Click **Go** to import the file.

    \[Omitted image "DataSource.png"\] Alt text: Data Sources

6.  Navigate to **System Import Sets** &gt; **Create Transform Map** and map the items in the Excel spreadsheet to the fields of the CMDB in the target table IP Range `[ip_address_range]` table.

7.  Give the Transform Map a unique and descriptive name.

8.  Submit the form, and then click **New** in the **Field Maps** Related List.

9.  Map the fields from the Excel spreadsheet to the fields in the IP Range `[ip_address_range]` table.

    The fields you need values for are the **Start IP** and **End IP** addresses.

10. Click the **Mapping Assist** Related Link and use the lists that appear to resolve the fields between the table and the data source \(the Excel spreadsheet in this example\).

11. Click **Save**.

    The view returns to the Table Transform Map form.

12. Click **Transform** in the Related Links to move the data into the proper fields in the IP Range `[ip_address_range]` table.

    The imported IP ranges are available now for use in any advanced Discovery schedule.


