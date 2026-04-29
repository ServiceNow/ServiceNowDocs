---
title: General guidelines for activity stream
description: Consider these general guidelines when configuring your activity stream.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure an activity stream screen, Record screen, Mobile screen types, Mobile screens, Mobile app components, Building mobile apps, Mobile Platform]
---

# General guidelines for activity stream

Consider these general guidelines when configuring your activity stream.

**Note:** For design considerations and user experience general guidelines when configuring your activity stream, refer to the [Activity stream screen section](https://horizon.servicenow.com/native-mobile/screens/activity-stream-screen) in the [Horizon design system](https://horizon.servicenow.com/native-mobile/overview) website.

-   **Add activity stream as a stream segment**

    Depending on your requirements, you can add an activity stream as a screen segment in a record screen or have it as a standalone screen.

-   **Include in incidents and requests**

    Incidents and requests that have pending activity should include an activity stream screen segment.

-   **Use of update history**

    Use an activity stream screen segment for records where history updates are important. However, if you're looking at a user profile record, activity stream segments may not be needed.

-   **Rename for user familiarity**

    The term Activity stream as a tab name may not be understood by some users. Consider renaming this tab to a term your users are familiar with, such as Updates, History, or Notes.

-   **@mention feature**
    -   Users can @mention someone in the activity stream, and the mentioned user will receive an email and push notifications based on admin and user preferences. For more information, see [Mobile push notifications](../concept/sg-mobile-push-notifications.md).
    -   Supporting @mention mobile push notifications requires configuration and isn’t supported by default for all tables. In this case, consider adding support for tables which require collaboration between users to increase communication efficiency.
-   **User role user or user criteria permissions**

    You can restrict access to the activity stream segment within the Record screen for specific users by assigning user roles or user criteria permissions. For more information, see [User roles and user criteria permissions for mobile apps](../concept/roles-user-criteria.md).


