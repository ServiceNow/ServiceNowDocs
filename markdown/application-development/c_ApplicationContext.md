---
title: Application context
description: When application developers create new records, the system automatically assigns the records to the currently selected application in the application picker.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Contextual development environment, Learning about developing on the ServiceNow AI Platform, Building applications]
---

# Application context

When application developers create new records, the system automatically assigns the records to the currently selected application in the application picker.

When application developers attempt to change existing records, the platform checks whether the currently selected application matches the scope of the application artifact. If they match, the application developer can save changes to the artifact. If they differ, the system makes the following changes to the user interface:

-   Makes all the fields on the current record read-only.
-   Displays a warning message that the application artifact belongs to another scope.

