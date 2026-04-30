---
title: Configuring the data table for a request type example
description: Review the data table associated with a request, such as the EMR Request Data \[sn\_ind\_rmt\_help\_incident\_data\] table, and make sure that the table has columns to store each system variable that you're planning to fetch from an EMR system.
locale: en-US
release: xanadu
product: EMR Help
classification: emr-help
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring EMR Help, EMR Help, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Configuring the data table for a request type example

Review the data table associated with a request, such as the EMR Request Data \[sn\_ind\_rmt\_help\_incident\_data\] table, and make sure that the table has columns to store each system variable that you're planning to fetch from an EMR system.

Say, as an administrator, you want to include a system variable `encounter` from an EMR system in the EMR incident request type.

You would confirm that the `encounter` system variable appears on the incident request type by using the following workflow:

1.  You review the EMR Request Data \[sn\_ind\_rmt\_help\_incident\_data\] table by navigating to **All** &gt; **System Definition** &gt; **Tables** and selecting the table.
2.  You check whether a column corresponding to the encounter system variable exists in the table.

    You observe that the column doesn't exist.

3.  You add a new column corresponding to the `encounter` system variable by clicking **New** in the Columns related list and filling in the column details associated with the `encounter` system variable on the Dictionary entry form and clicking **Submit**.

    For more information, see Dictionary entry form.


