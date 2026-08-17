---
title: Create an issue
description: Track a problem identified with an AI asset, such as a performance or compliance gap, and document the action plan for resolving it.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/ac-create-issue.html
release: australia
topic_type: task
last_updated: "2026-07-16"
reading_time_minutes: 3
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Issues, Manage tasks and approvals, Address action items, AI Control Tower, Enable AI experiences]
---

# Create an issue

Track a problem identified with an AI asset, such as a performance or compliance gap, and document the action plan for resolving it.

## Before you begin

Role required: sn\_ai\_governance.ai\_steward or sn\_ai\_asset\_mgmt.ai\_asset\_owner

## About this task

An issue tracks a problem identified with an AI asset that needs a resolution or an action plan, such as a gap surfaced during a governance review. For more information about governance records associated with AI systems, see [Governance record types](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/gov-airc-governance-records.md).

## Procedure

1.  Navigate to **All** &gt; **AI Control Tower** &gt; **Home** &gt; **Activity Center** &gt; **Work** &gt; **Assigned to you**.

2.  Select the **Issues** sub-tab.

3.  Select **New**.

4.  Fill in the fields that describe the issue.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the issue.|
    |Issue type|Type of issue.|
    |Classification|Classification of the issue.|
    |Location|Location associated with the issue.|
    |State|Current state of the issue. Defaults to **New**.|
    |Substate|More specific status within the current state.|
    |Priority|Priority of the issue.|
    |Issue rating|Severity rating assigned to the issue.|
    |Description|Description of the issue.|

5.  In the Assignment section, specify who should work the issue.

    |Field|Description|
    |-----|-----------|
    |Assignment group|Group responsible for working the issue.|
    |Assigned to|User assigned to work the issue.|
    |Issue manager group|Group responsible for managing the issue.|
    |Issue manager|User responsible for managing the issue.|
    |Watch list|Users who want to stay informed about the issue.|

6.  In the Schedule section, set the dates and duration for resolving the issue.

    |Field|Description|
    |-----|-----------|
    |Due date|Date and time the issue must be resolved by.|
    |Confirmed date|Confirmation date for the issue. This field is auto-filled.|
    |Planned start date|Planned date and time to start work on the issue. Defaults to the current date and time.|
    |Planned end date|Planned date and time to finish work on the issue. Defaults to the current date and time.|
    |Duration \(duration\)|Planned length of time to resolve the issue, in days, hours, minutes, and seconds.|
    |Created|Date on which the issue is created. This field is automatically set to the current date and time.|
    |Closed|Date on which the issue is closed.|
    |Actual start date|Actual date and time work on the issue started.|
    |Actual end date|Actual date and time work on the issue ended.|
    |Actual duration|Actual length of time spent resolving the issue, in days, hours, minutes, and seconds.|

7.  If the issue is part of a group of related issues, associate it with its parent in the Issue grouping section.

    |Field|Description|
    |-----|-----------|
    |Parent issue|Parent issue that this issue belongs to, if the issue is part of a group.|

    **Note:** When advanced issue grouping is enabled, the form also shows a **Group level** field that indicates whether the issue is a parent, child, or standalone issue, and a **Management method** field that indicates whether the issue is managed from the parent or from child issues individually.

8.  In the Action plan section, describe how the issue will be resolved.

    |Field|Description|
    |-----|-----------|
    |Recommendation|Recommended action to resolve the issue.|
    |Action plan|Plan for resolving the issue.|

9.  In the Confidentiality section, restrict visibility of the issue if needed.

    |Field|Description|
    |-----|-----------|
    |Confidential|Options that restricts visibility of the issue to confidential users and members of confidential user groups.|
    |Allowed users|Users who can access the issue if it's marked confidential.|
    |Allowed groups|Groups who can access the issue if it's marked confidential.|

10. In the Activity section, add any supporting notes or comments.

    |Field|Description|
    |-----|-----------|
    |Work notes \(Private\)|Internal notes about the issue that aren't visible to the customer.|
    |Additional comments \(Customer visible\)|Comments about the issue that are visible to the customer.|

11. In the Settings section, specify the functional domain that the issue belongs to.

    |Field|Description|
    |-----|-----------|
    |Functional domain|Functional domain that the issue belongs to, such as **AI Risk and Compliance** or **IT risk and compliance**.|

12. Save the issue.


## Result

The issue is created and appears in the **Issues** sub-tab, where the assigned user or group can work it through to resolution.

