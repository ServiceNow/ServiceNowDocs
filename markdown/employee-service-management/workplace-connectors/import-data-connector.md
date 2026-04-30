---
title: Configure data Sources and schedule imports
description: Set up the data source for the integration framework \(for example, badging spoke data\) and schedule the import job to retrieve data from the data source periodically.
locale: en-US
release: xanadu
product: Workplace Connectors
classification: workplace-connectors
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configure Workplace Connectors, Workplace Connectors, Workplace Service Delivery, Employee Service Management]
---

# Configure data Sources and schedule imports

Set up the data source for the integration framework \(for example, badging spoke data\) and schedule the import job to retrieve data from the data source periodically.

## Before you begin

Role required: sn\_wsd\_wc.admin

## Procedure

1.  Navigate to **All** &gt; **System Import Sets** &gt; **Data Sources**.

2.  Open the data source form by selecting **Create New**.

3.  Import the badging data record of employees to Workplace Connectors by selecting the imported file \(for example, the CSV badging file\).

4.  On the form, fill in the fields.

<table id="table_dzx_f5h_5xb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name for the data source.

</td></tr><tr><td>

Import set table label

</td><td>

Label for the import set table. For example, Badging Data.

</td></tr><tr><td>

Import set table name

</td><td>

Name of the import set table. For example, badging\_data.

</td></tr><tr><td>

Type

</td><td>

Option to select the connection type from the source to the Badging Data table. For example, select File.

</td></tr><tr><td>

File retrieval method

</td><td>

Option to select the appropriate method from the drop-down list to import the file.For example, SFTP, FTP, and so on.

</td></tr><tr><td>

Format

</td><td>

Option to indicate the data format type. For example, CSV.

</td></tr></tbody>
</table>5.  Select **Save**.

6.  Navigate to **All** &gt; **Scheduled Import Sets** &gt; **Scheduled Imports**.

7.  Select **Create New**.

8.  Configure the scheduled job according to your requirements, including the frequency of execution, and mapping to the data source.

9.  On the form, fill in the fields.

<table id="table_wpk_4xh_5xb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the installed workplace hardware,sensor data provider, or spoke. For example, occupancy sensor, badging spoke data, and so on.

</td></tr><tr><td>

Data Source

</td><td>

The source data table \(Badging Data table\) and the target table \(Employee Attendance Data table\).

</td></tr><tr><td>

Run as

</td><td>

User that executes the scheduled job. For example: **System Administrator**.

</td></tr><tr><td>

Run

</td><td>

Desired import frequency for the scheduled job. For example, **Daily**.

</td></tr><tr><td>

Daily

</td><td>

The time at which the scheduled job should be imported. For example: 10:30:00

</td></tr></tbody>
</table>10. Select **Execute Now**.


**Parent Topic:**[Configure Workplace Connectors](../concept/configure-workplace-connectors.md)

**Previous topic:**[Configure sensor data providers](providers-occupancy.md)

**Next topic:**[Configure badging data choices](configure-badging-data-choices.md)

