---
title: Managing email notifications in Knowledge Management
description: Reminders enable relevant users to review knowledge articles and complete tasks associated with them.
locale: en-US
release: australia
product: Knowledge Management
classification: knowledge-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Using Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Managing email notifications in Knowledge Management

Reminders enable relevant users to review knowledge articles and complete tasks associated with them.

By default, the Knowledge Management application includes the following types of email notifications:

-   [Email notifications for knowledge article feedback tasks](email-notifications-km.md#section_wn1_kxp_mlb).
-   [Email notifications for knowledge subscriptions](email-notifications-km.md#section_dcs_yfq_mlb).
-   [Email notifications for knowledge article approval publishing workflow](email-notifications-km.md#section_wdn_y3q_mlb).
-   [Email notifications for translation tasks](email-notifications-km.md#section_h1c_f3q_mlb).
-   [Email notifications for expiring knowledge articles](email-notifications-km.md#section_gsy_5jq_mlb).
-   [Email notifications for article quality index \(AQI\) reviews](email-notifications-km.md#section_dk1_rjq_mlb).

You can decide if you must receive any knowledge notifications by setting notification preferences. For more information, see [Set knowledge notification preferences](../task/set-subscription-notifications.md).

## Email notifications for knowledge article feedback tasks

The email notifications for knowledge article feedback tasks are available when your administrator activates the Knowledge Management Core plugin \(com.glideapp.knowledge\).

The following table describes the recipient list of notifications for knowledge article feedback tasks and the associated conditions when a notification is sent.

|Notification|Condition|Recipients|
|------------|---------|----------|
|KM Feedback Task: Commented|A comment was added to a user feedback task.|User who was assigned the feedback task|
|KM Feedback Task: Created|A user feedback task was created.|User who was assigned the feedback task|
|KM Feedback Task: Info from Submitter|More information was requested from the submitter of a user feedback task.|User who submitted the feedback task|
|KM Feedback Task: Reassigned|A user feedback task was reassigned.|User who was reassigned the feedback task|
|KM Feedback Task: Resolution Accepted|A resolution described in a user feedback task was accepted.|User who was assigned the feedback task|
|KM Feedback Task: Resolution Rejected|A resolution described in a user feedback task was rejected.|User who was assigned the feedback task|
|KM Feedback Task: Resolved|A user feedback task was set as resolved.|User who submitted the feedback task|

## Email notifications for knowledge subscriptions

The email notifications for knowledge subscriptions are available when your administrator activates the Knowledge Management Core plugin \(com.glideapp.knowledge\). For notifications associated with ownership groups, your administrator must also activate the Knowledge Management Advanced plugin \(com.snc.knowledge\_advanced\).

The following table describes the recipient list of notifications for knowledge subscriptions and the associated conditions when a notification is sent.

<table id="table_rkp_cgq_mlb"><thead><tr><th>

Notification

</th><th>

Condition

</th><th>

Recipients

</th></tr></thead><tbody><tr><td>

KM Subscription Group: Article checkout

</td><td>

A subscribed knowledge article was checked out

</td><td>

-   Author \(if no Ownership group is associated with the article\)
-   Ownership group manager and members \(if an Ownership group is associated with the article\)
-   Revisers

 **Note:** The user who checked out the article does not receive the notification.

</td></tr><tr><td>

KM Subscription Group: Article commented

</td><td>

A comment was added to a subscribed knowledge article

</td><td>

-   Author \(if no Ownership group is associated with the article\)
-   Ownership group manager and members \(if an Ownership group is associated with the article\)
-   Revisers

</td></tr><tr><td>

KM Subscription: Article published

</td><td>

A knowledge article was created in a subscribed knowledge base

</td><td>

-   knowledge base owner
-   Knowledge base subscribers

</td></tr><tr><td>

KM Subscription: Article revised

</td><td>

A subscribed knowledge article was edited

</td><td>

-   Knowledge base owner
-   Knowledge article subscribers
-   Author
-   Revisers

</td></tr><tr><td>

KM Subscription: Article revised in subscribed KB

</td><td>

A knowledge article in a subscribed knowledge base was edited.

</td><td>

-   Knowledge base owner
-   Knowledge article subscribers
-   Author
-   Revisers
-   Knowledge base subscriber

</td></tr></tbody>
</table>**Note:** An email notification is sent to a reviser of a knowledge article when the article versioning feature is enabled.

## Email notifications for knowledge article approval publishing workflow

The email notifications for knowledge article approval publishing workflow are available when your administrator activates the Knowledge Management Core plugin \(com.glideapp.knowledge\).

The following table describes the recipient list of notifications for the knowledge article approval publishing workflow and the associated conditions when a notification is sent.

|Notification|Condition|Recipients|
|------------|---------|----------|
|KM: Approve article for publishing|A knowledge article was approved for publishing with the ownership group feature disabled.|Knowledge base owner and managers|
|A knowledge article was approved for publishing with the ownership group feature enabled.|Ownership group manager and members|
|KM: Article approved for publish|A knowledge article was approved for publication.|User \(author or reviser\) who submitted the article for approval|
|KM: Article rejected for publish|A knowledge article was rejected for publication.|User \(author or reviser\) who submitted the article for approval|

**Note:** An email notification is sent to a reviser of a knowledge article when the article versioning feature is enabled.

## Email notifications for translation tasks

The email notifications for translation tasks are available when your administrator activates the Knowledge Management Advanced plugin \(com.snc.knowledge\_advanced\) and I18N: Knowledge Management Internationalization Plugin v2 plugin \(com.glideapp.knowledge.i18n2\). The 18N: Internationalization plugin \(com.glide.i18n\) activates the I18N: Knowledge Management Internationalization Plugin v2 plugin.

The following table describes the recipient list of notifications for translation tasks on knowledge articles and the associated conditions when a notification is sent.

<table id="table_umr_f3q_mlb"><thead><tr><th>

Notification

</th><th>

Condition

</th><th>

Recipients

</th></tr></thead><tbody><tr><td>

KM Translation Task: Assigned to me

</td><td>

A translation task was assigned.

</td><td>

User who was assigned the translation task

</td></tr><tr><td>

KM Translation Task: Closed

</td><td>

A translation task was closed after the translated version of the knowledge article was published.

</td><td>

-   User who was assigned the translation task
-   User who submitted the translation task

</td></tr></tbody>
</table>## Email notifications for expiring knowledge articles

The email notifications for expiring knowledge articles are available when your administrator activates the Knowledge Management Core plugin \(com.glideapp.knowledge\) and sets the value of the **glide.knowman.enable\_article\_expiry\_notification** property to `true`. By default, the property value is set to false.

Knowledge articles have an expiration date set using the **Valid to** field when creating the article. Articles do not appear in search results after the Valid to date.

On the first day of each month, the application sends an email notification to a list of authorized recipients to remind them about articles that are scheduled to expire in the next month. The user can then determine whether to extend the **Valid to** date to continue providing access to the article.

**Note:** To extend the **Valid to** date of a knowledge article, see [Edit a knowledge article](https://www.servicenow.com/docs/bundle/xanadu-servicenow-platform/page/product/knowledge-management/task/edit-knowledge-article.html)

The content of the email notification is determined by the number of articles expiring in the coming month.

-   Up to 10 – The email notification includes a list of article links displayed in a tabular format and arranged in ascending order by their Valid to date. Clicking a link opens the article in ServiceNow AI Platform.
-   More than 10 – The email notification includes a **View the list of expiring articles** link, which when accessed opens a list in ServiceNow AI Platform of all articles expiring in the next month.

The following table describes the recipient list of notifications for expiring knowledge articles and the associated conditions when a notification is sent.

<table id="table_q2x_4dx_ykb"><thead><tr><th>

Notification

</th><th>

Condition

</th><th>

Recipients

</th></tr></thead><tbody><tr><td rowspan="2">

KM: Article Expiry Warning

</td><td>

An article is scheduled to expire in the next month with the ownership group feature disabled.

</td><td>

-   Author
-   Knowledge base owner and managers
-   Reviser for the updated and checked-out versions

</td></tr><tr><td>

An article is scheduled to expire in the next month with the ownership group feature enabled.

</td><td>

-   Author
-   Knowledge base owner and managers
-   Reviser for the updated and checked-out versions
-   Ownership group manager and members

</td></tr></tbody>
</table>**Note:** An email notification is sent to a reviser of a knowledge article when the article versioning feature is enabled.

## Email notifications for article quality index \(AQI\) reviews

The email notifications for an article quality index review on knowledge articles are available when your administrator activates the Knowledge Management Advanced plugin \(com.snc.knowledge\_advanced\).

The following table describes the recipient list of notifications for an AQI review on knowledge articles and the associated conditions when a notification is sent.

<table id="table_ek1_rjq_mlb"><thead><tr><th>

Notification

</th><th>

Condition

</th><th>

Recipients

</th></tr></thead><tbody><tr><td>

KM: AQI on Article

</td><td>

An AQI was performed and submitted on a knowledge article with the ownership group feature disabled.

</td><td>

User \(author or reviser\) who last updated the article

</td></tr><tr><td>

KM: AQI on Ownership Group Article

</td><td>

An AQI was performed and submitted on a knowledge article with the ownership group feature enabled.

</td><td>

-   User \(author or reviser\) who last updated the article
-   Ownership group

</td></tr></tbody>
</table>**Note:** An email notification is sent to a reviser of a knowledge article when the article versioning feature is enabled.

-   **[Set knowledge notification preferences](../task/set-subscription-notifications.md)**  
Set notification preferences for knowledge bases and knowledge articles.

**Parent Topic:**[Using Knowledge Management](using-knowledge-management.md)

**Related topics**  


[Activate the Knowledge Management Advanced plugin](../task/activate-knowledge-advanced-plugin.md)

[Additional plugins for Knowledge Management](../reference/additional-plugins-km.md)

[Ownership groups](enable-ownership-group.md)

[Validity of a knowledge article](article-validity.md)

[Knowledge subscriptions](knowledge-article-subscriptions.md)

