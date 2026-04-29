---
title: Archive and Purge space occupancy data
description: Archive and purge the Space Occupancy data \(sn\_wsd\_wc\_space\_occupancy\) table after every five days.
locale: en-US
release: australia
product: Workplace Connectors
classification: workplace-connectors
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Setup Workplace Connectors for occupancy data, Configure Workplace Connectors, Workplace Connectors, Workplace Service Delivery, Employee Service Management]
---

# Archive and Purge space occupancy data

Archive and purge the Space Occupancy data \(sn\_wsd\_wc\_space\_occupancy\) table after every five days.

## Before you begin

The Archive rule **Archive Space Occupancy table at the end of everyday** runs every day to archive data from the Space Occupancy data \(sn\_wsd\_wc\_space\_occupancy\) table and archives it in the **Archived Space Occupancy** Table \(ar\_sn\_wsd\_wc\_space\_occupancy\). The Archive Destroy Rule **Destroy Space Occupancy archived table after every 5 days** purges data from Archived Space Occupancy Table \(ar\_sn\_wsd\_wc\_space\_occupancy\) after every five days.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Archiving** &gt; **Archive Rules**.

2.  Select and open the **Archive Space Occupancy table at the end of everyday** rule.

3.  Select the **Active** check box.

4.  In the **Conditions** field, change the archive filter conditions as required.

5.  From the **Related Links** section, select **Run Archive Now**.

    The archived data is stored in the Archived Space Occupancy \(ar\_sn\_wsd\_wc\_space\_occupancy\) table.

6.  Navigate to **All** &gt; **System Definition** &gt; **Tables**.

7.  Select **Archive space occupancy record**.

    All the deleted space occupancy data are stored in **Show List** under the Related Links section.

8.  Navigate to **All** &gt; **System Archiving** &gt; **Archive Destroy Rules**.

9.  Select **Destroy Space Occupancy archived table after every 5 days**.

10. In the **Conditions** field, set the archive duration condition as required.

11. From the Related Links section, select **Run Archive Destroy Now** to run the job.

    The Space occupancy data table records are deleted permanently.


**Parent Topic:**[Setup Workplace Connectors for occupancy data](../concept/setup-occupancy-connectors.md)

**Previous topic:**[Retrieving Space Occupancy Data](space-occupancy-data.md)

**Next topic:**[Setup Workplace Connectors for environmental data](../concept/setup-environmental-data-connectors.md)

