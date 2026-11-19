---
title: Workaround posted
description: This example demonstrates a table notification that generates an automatic message on Live Feed whenever a workaround is added to an open problem.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/servicenow-platform/live-feed/c\_Example1WorkaroundPosted.html
release: zurich
product: Live Feed
classification: live-feed
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Live Feed table notification examples, Live Feed table notifications, Administering Live Feed, Live Feed Core UI, Manage people and work capabilities, Extend ServiceNow AI Platform capabilities]
---

# Workaround posted

This example demonstrates a table notification that generates an automatic message on Live Feed whenever a workaround is added to an open problem.

-   **Table**: Problem \[problem\]
-   **Active**: Select the check box.
-   **Update**: Select the check box.
-   **Post to Live Feed**: Select the check box.
-   **Conditions**: \[State\] \[is\] \[Open\]
-   **Description**: `Workaround Posted`
-   **Message**:

    ```
    ${sys_updated_by} posted a workaround for ${URI}.
    Short description: ${short_description}
    ```

-   **Before script**:

    ```
    // only post to Live Feed when the Workaround field changes
    answer  = changedFields. contains ( "work_around" ) ;
    ```


**Parent Topic:**[Live Feed table notification examples](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/live-feed/c_LFTableNotifiExamples.md)

**Related topics**  


[Live Feed table notifications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/live-feed/c_SetUpLiveFeedTableNotifications.md)

