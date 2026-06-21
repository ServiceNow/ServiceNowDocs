---
title: View users' consent management policies
description: View and analyze details regarding users and their tracking selection preferences.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/now-intelligence/usage-insights/uxa-view-user-decision.html
release: yokohama
product: Usage Insights
classification: usage-insights
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Types of tracking consent policies, User privacy, tracking, and consent, Configuring User Experience Analytics, User Experience Analytics, Platform Analytics]
---

# View users' consent management policies

View and analyze details regarding users and their tracking selection preferences.

## Before you begin

Role required: analytics\_admin

## Procedure

1.  Navigate to **All**.

2.  In the navigator, enter `sys_analytics_user_consent_decision.list` to open the Usage Insights User Consent Decisions page.

3.  Review the data that applies to your users’ tracking selections.

    The table also includes the detection policy provider and the date of the migration from the deprecated table \[m2m\_user\_consent\_info\].

    -   **Note:** When a user either explicitly consents to or opts out of advanced tracking through the Explicit Opt In or Notice modal window, or if they manually update their tracking preference, a corresponding record is created or updated in the sys\_analytics\_user\_consent\_decision table. This record is only created if it doesn't exist. However, a record isn’t created if a user doesn't actively select an advanced tracking preference. This can happen, for instance, when a No Consent Required policy is assigned to a user and they don't manually adjust their tracking preference within the application.

    -   **Note:** A ServiceNow® Instance can disable the tracking of usage analytics data with its custom script and system property. Contact customer support for assistance.

    Users who fall under an Explicit Opt In or Notice consent policy receive an annual opt-in or notice message based on the date set in the User Consent Decision record.

    See [How users consent to tracking in Usage Insights](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/now-intelligence/usage-insights/user-exp-analytics-user-set.md) for information on how users manually update their preference.


**Parent Topic:**[Types of tracking consent policies in Usage Insights](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/now-intelligence/usage-insights/uxa-tracking-types.md)

