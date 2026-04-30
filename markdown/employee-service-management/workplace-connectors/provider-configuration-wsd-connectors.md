---
title: Configure badging table data
description: Register details for a new provider, configure a badging table and import data from the source table to the target table to integrate with the badging system.
locale: en-US
release: xanadu
product: Workplace Connectors
classification: workplace-connectors
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Provider connector configuration, Setup Workplace Connectors for badging data, Configure Workplace Connectors, Workplace Connectors, Workplace Service Delivery, Employee Service Management]
---

# Configure badging table data

Register details for a new provider, configure a badging table and import data from the source table to the target table to integrate with the badging system.

## Before you begin

The Badging data table is the source table and the Employee Attendance Data table is the target table. The badging data from the source table is imported from a badging provider \(for example, the attendance data from badge readers\).

Role required: sn\_wsd\_wc.admin

## Procedure

1.  Navigate to **All** &gt; **Workplace Connectors** &gt; **Provider Connector Configurations**.

2.  From the menu, select the application scope icon \(![Application Scope icon.](../images/wsd-appl-global-scope-icon.png)\).

3.  Select **Create New**.

    On the form, fill in the fields.

<table id="table_vct_344_vyb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Provider

</td><td>

Name of badging data provider.

</td></tr><tr><td>

Source Type

</td><td>

Source from where the badging data is collected and loaded into the target Employee attendance table. From the drop-down list, select **Table**.

**Note:** If you’re an existing user and have selected the **Import from table** option in an earlier release to retrieve badging data in your Workplace Connectors instance, the **Source Type** field is defaulted to **Table**. If the **Import from table** option wasn’t selected in your Workplace Connectors instance, then the **Source Type** field is defaulted to **External**. The **Import from table** option isn’t supported in the November ServiceNow Store release.

</td></tr><tr><td>

Run frequency

</td><td>

Day and time frequency to import data from the workplace system. For example: 5 minutes.The process provider data record picks the records from the badging data table and populates the Employee Attendance table based on the run frequency.

</td></tr><tr><td>

Active

</td><td>

Option to indicate that the provider configuration is active.

</td></tr><tr><td>

Connector Configuration

</td><td>

Select the lookup list icon \(![Lookup list icon.](../../workplace-lease-administration/images/look-up-icon.png)\) and select **Badging**. For more information, see [Configure connector configuration for badging data](workplace-connector-configuration.md).

</td></tr></tbody>
</table>4.  Select **Submit**.

5.  In the Provider Executions table section, filter by **Last query time**.

    The Provider Execution table \[sn\_wsd\_wc\_provider\_execution\] stores all the scheduled job execution timestamps. Every time that the scheduled job **Process Provider data** record runs, this table shows an entry in the Last query time column. The time to import data from the source table \(Badging data\) to the target table \(Employee attendance data\) table is updated in the Last query time column.

6.  Select **Save**.

7.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled jobs**.

8.  In the **Scheduled Jobs Name** field, filter data by **Process provider data records** and select it.

    Process provider data records read data from vendor badging data \(source table\). After processing the badging data, it loads it into the Employee Attendance Data table \(target table\).

9.  Select and open the Schedule Script Execution for Provider process data records in the edit mode.

10. Review the Process provider data records form.

    If necessary, change or update the **Repeat interval** timings for the scheduled job.

11. Select **Execute Now**.

    The scheduled job takes the source data from the Badging data table to transform the data in the required format, and place it in the target Employee Attendance Data table.


**Parent Topic:**[Provider connector configuration](../concept/provider-configuration-ovw.md)

**Previous topic:**[Provider connector configuration](../concept/provider-configuration-ovw.md)

**Next topic:**[Configure a webhook event](configure-webhook-restapi.md)

