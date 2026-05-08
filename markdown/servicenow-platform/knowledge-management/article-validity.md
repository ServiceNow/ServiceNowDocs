---
title: Validity of a knowledge article
description: Knowledge article validity is the date a knowledge article expires. Articles do not appear in search results after the Valid to date or if the Valid to date is blank.
locale: en-US
release: australia
product: Knowledge Management
classification: knowledge-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Knowledge Management reference, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Validity of a knowledge article

Knowledge article validity is the date a knowledge article expires. Articles do not appear in search results after the **Valid to** date or if the **Valid to** date is blank.

Decide when to expire a knowledge article by using the **Valid to** field in the Knowledge form. The Knowledge form is available when creating or editing a knowledge article.

When you create or edit a knowledge article, a default value appears in the **Valid to** field. As an article author or editor, you can select whether to keep or change the default **Valid to** date.

**Note:** If the system date format or user preferences is set to use `yy` year format, you might face issues when the **Valid to** date is set to the default date. Contact your system administrator or modify the user preferences to use a date format with the `yyyy` year format. For more information, see Global date and time field format and Personalize the system date format topics.

## Default article validity when creating a knowledge article

The default value of the **Valid to** field is derived from the **Article Validity** field configured for the knowledge base \(see [Create a knowledge base](../task/create-a-knowledgebase.md)\). The **Valid to** date starts from the date the article was created until the number of days specified in the **Article Validity** field. If the **Article Validity** field is blank, the default date in the **Valid to** field for the knowledge article is set to January 1, 2100.

## Default article validity when editing a knowledge article

If the article versioning feature is enabled, the default value of the **Valid to** date in the updated article version is automatically set as described in the following table.

|Article Validity value in the associated knowledge base|Valid to default value|Notes|
|-------------------------------------------------------|----------------------|-----|
|Blank|Earlier version **Valid to** date value|If the **Article Validity** field in the knowledge base associated with the article is blank, the **Valid to** date value from the earlier version of the article is retained.|
|Is not blank|Article updated date + article validity|If the **Article Validity** field in the knowledge base associated with the article is not blank, the **Valid to** date is automatically updated to start from the date the article was updated until the number of days specified in the **Article Validity** field.|

If you move a knowledge article to another knowledge base, the default value of the **Valid to** date in the updated article is automatically set as described in the following table.

|Article Validity value in the updated knowledge base|Valid to default value|Notes|
|----------------------------------------------------|----------------------|-----|
|Blank|Earlier **Valid to** date value|If the **Article Validity** field in the selected knowledge base is blank, the earlier **Valid to** date value is retained for the knowledge article.|
|Is not blank|Article updated date + article validity|If the **Article Validity** field in the selected knowledge base isn't blank, the **Valid to** date is automatically updated to start from the date the article was updated until the number of days specified in the **Article Validity** field.|

**Note:** If the dictionary value of the **Valid to** field is modified, this dictionary value overrides the default value of the **Valid to** field calculated according to the **Article Validity** field.

## Email notifications for expiring knowledge articles

On the first day of each month, the application sends an email notification to a list of authorized recipients to remind them about articles that are about to expire in the next month. The recipient can then extend the **Valid to** date to continue using the article. For more information, see [Managing email notifications in Knowledge Management](email-notifications-km.md).

