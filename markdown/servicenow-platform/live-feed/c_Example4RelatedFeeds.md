---
title: Related feeds table notification
description: This example demonstrates table notifications to be sent out to related feeds.
locale: en-US
release: xanadu
product: Live Feed
classification: live-feed
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Live Feed table notification examples, Live Feed table notifications, Administering Live Feed, Live Feed Core UI, Manage people and work capabilities, Extend ServiceNow AI Platform capabilities]
---

# Related feeds table notification

This example demonstrates table notifications to be sent out to related feeds.

For this example, whenever the status of a story changes to **Complete**, a table notification message is sent to the related sprint, release, or epic. Messages are posted only if the related feed already exists; this notification does not create a new feed.

-   **Table**: Story \[rm\_story\]
-   **Active**: Select the check box.
-   **Update**: Select the check box.
-   **Post to Live Feed**: Select the check box.
-   **Record feeds**: Move **Sprint**, **Release**, and **Epic** to the **Selected** column.
-   **Conditions**: \[State\] \[changes to\] \[Complete\]
-   **Description**: `Story is done; message to Epic, Release, and Sprint`
-   **Message**:

    ```
    ${URI} status changed to ${state}
    ```


**Parent Topic:**[Live Feed table notification examples](c_LFTableNotifiExamples.md)

