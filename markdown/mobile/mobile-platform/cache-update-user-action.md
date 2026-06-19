---
title: Cache updates triggered by user actions
description: Use action-triggered cache updates to define specific user actions that automatically refresh the offline cache in the background. This process reduces reliance on manual cache updates and helps to verify that users have current data when its needed.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile/mobile-platform/cache-update-user-action.html
release: australia
product: Mobile Platform
classification: mobile-platform
topic_type: concept
last_updated: "2026-06-01"
reading_time_minutes: 1
breadcrumb: [Configure offline cache to devices, Offline mode setup options, Offline mode, Before implementation, Configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Cache updates triggered by user actions

Use action-triggered cache updates to define specific user actions that automatically refresh the offline cache in the background. This process reduces reliance on manual cache updates and helps to verify that users have current data when its needed.

When a user performs a defined action, such as tapping a button, the app automatically initiates a cache download or update upon successful completion of the assigned write-back action. This behavior is controlled by an optional button attribute \(sys\_sg\_button\_attribute\_name\), which can be configured to trigger an offline cache refresh after the write-back action completes successfully, with no additional user input required.

-   **[Configure offline caching upon writeback actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/mobile-platform/trigger-offline-cache-download.md)**  
**Trigger offline cache download** is an optional button attribute \(**sys\_sg\_button\_atribute\_name**\) that will generate an offline cache after a successful completion of the assigned writeback action.

**Parent Topic:**[Configure offline cache downloads to user devices](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/mobile-platform/offline-cache.md)

