---
title: Widgets for Listening Posts
description: Pre-configured widgets help to display a pulse survey that is raised from Listening Posts onto Employee Center.
locale: en-US
release: xanadu
product: Listening Posts
classification: listening-posts
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring Listening Posts, Listening Posts, HR Service Delivery, Employee Service Management]
---

# Widgets for Listening Posts

Pre-configured widgets help to display a pulse survey that is raised from Listening Posts onto Employee Center.

|Name|Description|
|----|-----------|
|Listening Posts My Survey|Displays a pulse survey as a widget on Employee Center.|
|Listening Posts Take Survey|Displays the pulse survey page with pulse questions on Employee Center.|
|Listening Posts Survey List|Displays all pulse surveys assigned to a user in a list view on Employee Center.|
|Listening Posts Feedback Bucket|Contains the fly out notifications that are received after a task completion on Employee Center.|
|Listening Posts Feedback Collection|Displays the pulse survey fly out notifications after a task completion on Employee Center. This fly out notification remains for 10 seconds on the screen.|
|Listening Posts Popup Survey|Displays the survey to the user in a modal after a user clicks the **Give feedback** button on the fly out notification on Employee Center.|
|Listening Posts Voluntary Feedback Popup|Displays the **Give feedback** button on Employee Center to enable a user take a voluntary survey.|
|Listening Posts Voluntary Feedback|Displays a questionnaire when a user clicks the **Give feedback** button on Employee Center.|

For more information on these widgets, navigate to **Service Portal** &gt; **Widgets**.

## Additional configuration to display pulse survey widgets on Employee Center

-   Update the Employee Center plugin to 22.0.\* version.
-   Allow Restricted Caller Access to be created under the Listening Posts application.
-   Deactivate the record Use Standard Ticket \(sys\_id: ed1cbb15738200105788e1e54cf6a760\) in Page Route Maps to get the notifications on the My Requests page.

    **Note:**

    -   Only the HR ticket page \[hrm\_ticket\_page\] is supported and not the Standard ticket page \[standard\_ticket page\].
    -   The Listening Posts Feedback Bucket, Listening Posts Feedback Collection, and Popup Listening Posts Survey widgets are embedded only in the To-dos page \[hrm\_todos\_page\], HR ticket page \[hrm\_ticket\_page\], and HRM To-dos page \[hrm\_todo\].

