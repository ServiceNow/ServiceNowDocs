---
title: Configure abuse reporting
description: Configure whether users can report content and profile abuse, set an abuse reporting threshold, and define reasons for abuse reporting.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/communities/configure-abuse-reporting.html
release: brazil
product: Communities
classification: communities
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Moderate a community, Configuring communities, Communities, Customer Service Management]
---

# Configure abuse reporting

Configure whether users can report content and profile abuse, set an abuse reporting threshold, and define reasons for abuse reporting.

## Before you begin

Role required: sn\_communities.admin or sn\_communities.moderation\_admin

**Important:**

Starting with the Brazil release, Communities is being prepared for future deprecation. It will be hidden and no longer installed on new instances but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

## Procedure

1.  Navigate to **All** &gt; **Community** &gt; **Moderation** &gt; **Moderation Settings**.

2.  Click the **Abuse** related list.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Enable Content Abuse Reporting|Check box to enable users to report inappropriate content.|
    |Enable Profile Abuse Reporting|Check box to enable users to report inappropriate profiles.|
    |Abuse Reporting Threshold|Number of abuse reports on a specific content \(question, blog, video, answer, comment\) that lead to the content being hidden from other users.|
    |Content Abuse Reporting Reasons List|Phrases that are possible reasons for the user to report inappropriate content contributions. Separate each phrase using the pipe symbol\|. For example, This content is abusive\|This content used an offensive word\|Spam\|Inappropriate media.|
    |Profile Abuse Reporting Reasons List|Phrases that are possible reasons for the user to report an inappropriate user profile. Separate each phrase using the pipe symbol\|.|

4.  Click **Update**.


**Parent Topic:**[Moderate a community](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/communities/moderate-communities.md)

