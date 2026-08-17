---
title: Create alert rule
description: Create alert rules to track the usage of generative AI skills in AI Admin Hub and notify you in the instance and via email, when the set thresholds are reached.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/create-alert-rule.html
release: australia
topic_type: task
last_updated: "2026-08-04"
reading_time_minutes: 1
keywords: [Create usage alert rule]
breadcrumb: [Usage alerts, AI Admin Hub Settings, Exploring AI Admin Hub, AI Admin Hub, Enable AI experiences]
---

# Create alert rule

Create alert rules to track the usage of generative AI skills in AI Admin Hub and notify you in the instance and via email, when the set thresholds are reached.

## Before you begin

Role required: sn\_nowassist\_admin

## Procedure

1.  Navigate to **Admin** &gt; **AI Admin Hub** &gt; **Settings**.

2.  Go to **Usage Alerts**.

3.  Select **Alerts** to view previously created alerts.

    \[Omitted image "ai-admin-usage-alerts-alerts.png"\] Alt text: View created alerts

4.  Select **Rules** to view and create alert rules.

    \[Omitted image "ai-admin-usage-create-alerts.png"\] Alt text: Create rule for alert usage

    1.  Enter a rule name for the alert you're creating.

    2.  Select the skill you want to apply the alert rule to.

    3.  Select the usage metric or the usage criteria.

        -   assist consumption: assists consumed in the given time frame
        -   execution count: number of times the affected skill is executed
    4.  Enter the threshold value for the selected metric.

    5.  Select an alert timeline window for the rule execution frequency.

        For example: If you choose 'daily', the rule will send an alert every day when the threshold is met.

    6.  Select the severity of the alert notification.

        You can choose from All, Critical, Warning or Info type of notification severity. This is displayed with the email notification received.

    7.  Choose to get notified via email using 'Send email notifications' toggle.

        If you opted in, you can select one or more users with an email address.

    8.  Enter email recipients to be notified with the alert.

    9.  Select **Create rule** to submit or **Cancel** to revert.


**Parent Topic:**[Usage alerts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/usage-alerts.md)

