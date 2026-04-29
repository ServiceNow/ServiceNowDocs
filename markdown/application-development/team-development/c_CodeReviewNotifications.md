---
title: Code review notifications
description: You must enable email notifications on the instance requiring code review for that instance to send code review notifications.
locale: en-US
release: australia
product: Team Development
classification: team-development
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Code reviews, Administer, Team Development, Planning your application, Building applications]
---

# Code review notifications

You must enable email notifications on the instance requiring code review for that instance to send code review notifications.

The Team Development Code Review workflow sends notifications to members of the Team Development Code Reviewers group when:

-   A push requires code review.
-   A user cancels a push.

If the user who pushed the changes has a user record with an email address on the instance where code review was required, the user receives a notification when the approval stage is set to Complete \(approved\) or Code Changes Rejected.

The code review notifications contain the following information:

<table id="table_qzf_1jv_1q"><thead><tr><th>

Notification name

</th><th>

Table

</th><th>

Contents

</th></tr></thead><tbody><tr><td>

Code review update for developer

</td><td>

Push or Pull \[sys\_sync\_history\]

</td><td>

-   The push name
-   The approval stage of the push \(approved or rejected\)
-   A link to the instance where the code review request was made

</td></tr><tr><td>

Notify code reviewer of canceled review

</td><td>

Push or Pull \[sys\_sync\_history\]

</td><td>

-   The user who canceled review
-   The push that was canceled

</td></tr></tbody>
</table>