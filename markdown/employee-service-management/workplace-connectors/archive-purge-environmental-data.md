---
title: Archive and purge Environmental data
description: Use the archive rules and destroy rules to archive and purge the environmental data. Archive and purge the Environmental data \(sn\_wsd\_wc\_space\_envrionment\) table records.
locale: en-US
release: australia
product: Workplace Connectors
classification: workplace-connectors
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Setup Workplace Connectors for environmental data, Configure Workplace Connectors, Workplace Connectors, Workplace Service Delivery, Employee Service Management]
---

# Archive and purge Environmental data

Use the archive rules and destroy rules to archive and purge the environmental data. Archive and purge the Environmental data \(sn\_wsd\_wc\_space\_envrionment\) table records.

## Before you begin

The Archive rule **Archive Environmental Data table** runs every day to archive data from the Environmental data \(sn\_wsd\_wc\_space\_environment\) table and archives Environmental Data table records after 48 hours. The Archive Destroy Rule **Destroy rule for sn\_wsd\_wc\_space\_environment** purges data from Archived Environmental data \(sn\_wsd\_wc\_space\_environment\) permanently.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Archiving** &gt; **Archive Rules**.

2.  Select and open the **Archive Environmental Data table** rule.

3.  Select the **Active** check box.

4.  In the **Conditions** field, change the archive filter conditions as required.

5.  From the **Related Links** section, select **Run Archive Now**.

    The data is archived in the Archived Environmental data \(sn\_wsd\_wc\_space\_environment\) table.

6.  Navigate to **All** &gt; **System Archiving** &gt; **Archive Destroy Rules**.

7.  Select **Destroy rule for sn\_wsd\_wc\_space\_environment**.

8.  In the **Conditions** field, set the archive duration condition as required.

9.  From the Related Links section, select **Run Archive Destroy Now** to run the job.

    Destroys archived records for sn\_wsd\_wc\_space\_environment table. The data table records are deleted permanently.


**Parent Topic:**[Setup Workplace Connectors for environmental data](../concept/setup-environmental-data-connectors.md)

**Previous topic:**[Configure environmental sensor data for a workplace location](config-connectors-env-sensor.md)

**Next topic:**[Workplace Connectors references](../concept/workplace-connectors-references.md)

