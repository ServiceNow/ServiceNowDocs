---
title: Access observer
description: Use Access Observer to understand people and processes access data on your instance.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
---

# Access observer

Use Access Observer to understand people and processes access data on your instance.

With Access Observer security administrators can:

-   Understand which entities like users, roles, scoped apps, and scripts that access your data.
-   Use this foreknowledge to know how best to apply security to limit unnecessary access to your data, while confirming those requiring access and still operate normally.
-   Avoid broken automation by seeing a clear view of how your data is accessed before making security changes.
-   Address the need to provide information regarding how encryption is applied on your instance.

Configure Access Observer by creating Access Observer configuration records. Within these records, you define a specific table and column to be observed and the time in which the column is observed.

![Access Observer configuration record](../images/data-obs-1.png)

Find the results of your observations on the Access Observer log record table. On this table you can see a record detailing each time the specified column is accessed.

![Access Observer log records showing details of an observation](../images/data-obs-2.png)

-   **[Configure access observation](../task/config-access-observation.md)**  
Create an access observation record to review access to a data column during a specified time window.
-   **[Review Access Observer logs](../reference/review-access-obs-logs.md)**  
Use information in the Access Observer log records for insights on how your data is accessed.

