---
title: Global events
description: Your instance has a global function called global\_events\(\) that triggers from a business rule when certain conditions occur.
locale: en-US
release: xanadu
product: System Events
classification: system-events
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [System events reference, System Events, Build workflows]
---

# Global events

Your instance has a global function called global\_events\(\) that triggers from a business rule when certain conditions occur.

This function triggers when your instance is:

-   Inserting new records
-   Updating existing records
-   Adding comments to an existing record
-   Assigning a record to a user
-   Exceeding a record's inactive timer

For example, if you add the script global.events\(current\) to a business rule on the `change_request` table, the instance automatically configures the following events:

-   change\_request.inserted
-   change\_request.updated
-   change\_request.commented
-   change\_ request.assigned
-   change\_ request.inactive

**Parent Topic:**[System events reference](system-events-reference.md)

