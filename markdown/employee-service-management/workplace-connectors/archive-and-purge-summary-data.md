---
title: Archive and purge summary data tables
description: Use the archive rules and destroy rules to archive and purge the summary data. Archive and purge the Space Occupancy Daily Summary Data \(sn\_wsd\_wc\_space\_occupancy\_daily\_summary\_data\), Environmental Daily Summary Data \(sn\_wsd\_wc\_environmental\_daily\_summary\_data\), Environmental Hourly Summary Data \(sn\_wsd\_wc\_environmental\_hourly\_summary\_data\), and Wi-Fi Daily Summary Data \(sn\_wsd\_wc\_wifi\_daily\_summary\_data\) table records.
locale: en-US
release: yokohama
product: Workplace Connectors
classification: workplace-connectors
topic_type: task
last_updated: "2025-03-05"
reading_time_minutes: 2
breadcrumb: [Workplace Connectors data summarization, Reference, Workplace Connectors, Workplace Service Delivery, Employee Service Management]
---

# Archive and purge summary data tables

Use the archive rules and destroy rules to archive and purge the summary data. Archive and purge the Space Occupancy Daily Summary Data \(sn\_wsd\_wc\_space\_occupancy\_daily\_summary\_data\), Environmental Daily Summary Data \(sn\_wsd\_wc\_environmental\_daily\_summary\_data\), Environmental Hourly Summary Data \(sn\_wsd\_wc\_environmental\_hourly\_summary\_data\), and Wi-Fi Daily Summary Data \(sn\_wsd\_wc\_wifi\_daily\_summary\_data\) table records.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Archiving** &gt; **Archive Rules**.

2.  Select and open the required archive rule.

    |Type|Archive Rule|Duration|
    |----|------------|--------|
    |Space Occupancy Daily Summary Data|Archive Space Occupancy Daily Summary Data Table|Archive the space occupancy daily summary data table after 365 days.|
    |Environmental Daily Summary Data|Archive Environmental Daily Summary Data \(ar\_sn\_wsd\_wc\_environmental\_daily\_summary\_data\)|Archive the environmental daily summary data table after 365 days.|
    |Environmental Hourly Summary Data|Archive Environmental Hourly Summary Data \(ar\_sn\_wsd\_wc\_environmental\_hourly\_summary\_data\)|Archive the environmental hourly summary data table after every 15 days.|
    |Wifi Daily Summary Data|Archive Wifi Daily Summary Data Table|Archive the Wi-Fi daily summary data table after 365 days.|

3.  Select the **Active** check box.

4.  In the **Conditions** field, change the archive filter conditions as required.

5.  Select the **Run Archive Now** related link.

    The data is archived in the Archived table.

6.  Navigate to **All** &gt; **System Archiving** &gt; **Archive Destroy Rules**.

7.  Select and open the required destroy rule.

    |Type|Destroy Rule|Duration|
    |----|------------|--------|
    |Space Occupancy Daily Summary Data|Destroy rule for sn\_wsd\_wc\_space\_occupancy\_daily\_summary\_data|Purges data from the Archive Space Occupancy Daily Summary Data table \[ar\_sn\_wsd\_wc\_space\_occupancy\_daily\_summary\_data\] after 365 days.|
    |Environmental Daily Summary Data|Destroy rule for sn\_wsd\_wc\_environmental\_daily\_summary\_data|Purges data from the Archive Environmental Daily Summary Data table \[ar\_sn\_wsd\_wc\_environmental\_daily\_summary\_data\] after 365 days.|
    |Environmental Hourly Summary Data|Destroy rule for sn\_wsd\_wc\_environmental\_hourly\_summary\_data|Purges data from the Archive Environmental Hourly Summary Data table \[ar\_sn\_wsd\_wc\_environmental\_hourly\_summary\_data\] after every 15 days.|
    |Wifi Daily Summary Data|Destroy rule for sn\_wsd\_wc\_wifi\_daily\_summary\_data|Purges data from the Archive Wi-fi Daily Summary Data table \[ar\_sn\_wsd\_wc\_wifi\_daily\_summary\_data\] after 365 days.|

8.  In the **Archive Duration** field, set the archive duration before the records are destroyed.

9.  Run the job by selecting the **Run Archive Destroy Now** related link.


**Parent Topic:**[Workplace Connectors data summarization](../concept/data-summarization.md)

**Previous topic:**[Workplace Connectors data summarization](../concept/data-summarization.md)

**Next topic:**[Run the DataSummarization on-demand job](run-the-datasummarization-on-demand-job.md)

