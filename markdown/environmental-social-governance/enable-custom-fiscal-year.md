---
title: Create fiscal calendars
description: Collect, aggregate, and report data based on your fiscal calendars, which may differ from the standard Gregorian calendar. Global organizations often operate in countries with unique fiscal calendars. By creating fiscal calendars in the Operational Sustainability Management application, you enable local entities to collect data according to their own schedules.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring GRC: Metrics, GRC: Metrics, Operational Sustainability Management \(formerly Environmental, Social, and Governance\)]
---

# Create fiscal calendars

Collect, aggregate, and report data based on your fiscal calendars, which may differ from the standard Gregorian calendar. Global organizations often operate in countries with unique fiscal calendars. By creating fiscal calendars in the Operational Sustainability Management application, you enable local entities to collect data according to their own schedules.

## Before you begin

Role required: sn\_grc\_metric.admin

## Procedure

1.  Navigate to **All** &gt; **Operational Sustainability Management** &gt; **Metric Calendar Configurations**.

2.  Select **New**.

3.  On the form, fill in the fields.

<table id="table_rtg_j3k_zbc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Calendar name. For example, `Australia calendar`.

</td></tr><tr><td>

Description

</td><td>

Brief description of the calendar.

</td></tr><tr><td>

Start month

</td><td>

Month the fiscal year begins.

</td></tr><tr><td>

End month

</td><td>

Month the fiscal year ends. This field is automatically set based on the start month. This field cannot be modified.

</td></tr><tr><td>

Year representation

</td><td>

Specify how you want to represent the fiscal year. In some countries, such as India, the fiscal year starts in one calendar year and ends in the next. For instance, the fiscal year in India starts on April 1, 2024, and ends on March 31, 2025. In this field, the choices are as follows:

-   **Start year**: Represents the fiscal year by its starting year. For example, 2024 for the fiscal year starting April 1, 2024.
-   **End Year**: Represents the fiscal year by its ending year. For example, 2025 for the fiscal year ending March 31, 2025.


</td></tr></tbody>
</table>4.  Select **Submit**.


## What to do next

Map the source and target calendars. For more information, see [Map target and source calendars](map-target-and-source-calendars.md).

-   **[Map target and source calendars](map-target-and-source-calendars.md)**  
Map target calendars with source calendars to establish the data roll up hierarchy. You can create multiple calendar mappings depending on your requirements.
-   **[Add entities for fiscal calendars](add-entities-for-a-fiscal-calendar.md)**  
Identify the entities that will follow the fiscal calendars you have created. This ensures that data collection is consistent, as each entity follows the designated calendar.

**Parent Topic:**[Configuring GRC: Metrics](../concept/configuring-grc-metrics.md)

