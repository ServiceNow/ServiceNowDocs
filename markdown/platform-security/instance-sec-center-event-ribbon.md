---
title: Monitor security events
description: Analyze the event metrics in your instance so that you can identify and prevent potential security events.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 9
breadcrumb: [Instance Security Center, Platform Security]
---

# Monitor security events

Analyze the event metrics in your instance so that you can identify and prevent potential security events.

**Important:**

Instance Security Center \(ISC\) has reached the end of sales as of September 2024, and is no longer supported or available for new activation.

ServiceNow Security Center \(SSC\) is the recommended solution going forward. For more information, see [Instance Security Center to ServiceNow Security Center migration](../../security-center/concept/instance-security-center-to-security-center-migration.md).

In the event ribbon, which is on the Instance Security homepage, you can analyze these metrics and accompanying detail to identify potential security events in the instance.

-   For each event metric, a real-time single score count appears, indicating how many times that the event occurred during the day in this instance. These single score reports are updated automatically as the corresponding events take place.
-   Each event metric also contains compliance trend and graph information over a range of dates. This information updates on a daily basis when you run the performance analytics job. To learn more, see the **Analyzing event trend detail** section.

## Event types

You can monitor at least six of the following types of events. For more than six events, use the left or right arrows below the event ribbon to scroll through them. To learn how to configure the event ribbon, see [Configure the security event ribbon](../task/instance-sec-center-configure-event-ribbon.md).

<table id="table_rpk_b5z_4lb"><thead><tr><th>

Notification preference

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Admin Logins

</td><td>

Number of login attempts in this instance, during the calendar day, by users who have an assigned admin role.

</td></tr><tr><td>

Admin Users Added

</td><td>

Number of users with an admin role that were added in this instance during the calendar day. For example, your instance may have a security issue if the count is 10, but 4 users are known to have an assigned admin role.

</td></tr><tr><td>

External Incoming Email

</td><td>

To learn more, see [Email metrics](instance-sec-center-email-metrics.md).

</td></tr><tr><td>

External Logins

</td><td>

Number of users with an assigned snc\_external role who logged into this instance during the calendar day. These logins typically occur for maintenance, support, consulting, or audit purposes. Monitoring this metric enables you to verify that the external login attempts are legitimate and not potential security issues.To learn more about assigning external user roles, see [Explicit Roles](../../contextual-security/concept/explicit-roles.md#).

</td></tr><tr><td>

Failed Logins

</td><td>

Number of attempted logins that failed in this instance during the calendar day.This metric may indicate that attempts are being made to log in and compromise your instance security.

</td></tr><tr><td>

Impersonations

</td><td>

Number of impersonation logins in this instance during the calendar day. To learn about impersonating users, see [Impersonate a user](https://www.servicenow.com/docs/access?context=c_ImpersonateAUser&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

</td></tr><tr><td>

Quarantined Files

</td><td>

Number of files that were quarantined when you ran Antivirus Scanning in this instance during the calendar day. To learn more about quarantined files and Antivirus Scanning, see [Antivirus metrics](instance-sec-center-antivirus-metrics.md) and [Antivirus Scanning](antivirus-protection.md).

</td></tr><tr><td>

Security Elevations

</td><td>

Number of times that a security administrator has elevated security for standard users by changing their assigned user role to a high privilege security role during the calendar day. These high privilege security roles include oauth\_admin, admin, security\_admin, and impersonator. -   This metric indicates that someone might have tried to elevate the security of an unauthorized user. Do not use this metric by itself to detect a specific security compromise. Instead, treat this metric as an indication that you should check another metric to see if a security compromise has occurred.
-   To learn more about elevating user security, see [Elevate to a privileged role](../task/t_ElevateToAPrivilegedRole.md) and [Elevated privilege roles](c_ElevatedPrivilege.md).

</td></tr><tr><td>

SNC Logins

</td><td>

Number of Customer Service and Support personnel who logged into this instance using the hi-hopping technique during the calendar day. These logins typically occur for maintenance, support, consulting, or audit purposes.For information on how to control ServiceNow corporate employee access, see [ServiceNow access control](c_SNCAccessControl.md).

</td></tr><tr><td>

Spam

</td><td>

To learn more, see [Email metrics](instance-sec-center-email-metrics.md).

</td></tr><tr><td>

Trusted Incoming Email

</td><td>

To learn more, see [Email metrics](instance-sec-center-email-metrics.md).

</td></tr><tr><td>

Untrusted Incoming Email

</td><td>

To learn more, see [Email metrics](instance-sec-center-email-metrics.md).

</td></tr><tr><td>

Virus Types

</td><td>

Number of different types of antivirus events that occurred in this instance during the calendar day. To learn more about antivirus event types, see [Antivirus metrics](instance-sec-center-antivirus-metrics.md).

</td></tr></tbody>
</table>## Analyzing event trend detail

To view trend details for an event metric, click the event count to access the Analytics Hub page. The details that appear for the instance depend on the type of metric.

For example, to view a listing of each failed attempt on the Security Dashboard Event Logs page:

-   Select the **Failed Logins** metric.
-   In the Analytics Hub page, click **Show Records**.
-   Click one of the failed login attempts.
-   The detail includes the name of the user who attempted to log in, their IP address, and the table name that they tried to access.

You can set up event threshold triggers in the Core UI Analytics Hub or Platform Analytics KPI Details to provide alerts when a certain event occurs within a range of scores for an [indicator](https://www.servicenow.com/docs/access?context=performance-analytics-glossary&version=zurich&pubname=zurich-now-intelligence&section=gloss-indicator&ft:locale=en-US). You can also set targets that enable you to visualize the difference between the desired score and the actual score of an event.

For example, you can set a threshold of `10` for the **Failed Logins** metric. When ten or more failed login attempts occur during the day, an alert is sent to specific security personnel. You can also set a similar target that provides a visual highlight in the Analytics Hub when 10 failed logins occur during a day.

Trend data and graphs that appear in Event ribbon tile and the Analytics Hub are updated after the performance analytics job executes at 02:00 local time. To learn more, see [How Daily Compliance score, trend, and graph data is refreshed](how-daily-compl-score-trend-date-refreshed.md).

-   **[Configure the security event ribbon](../task/instance-sec-center-configure-event-ribbon.md)**  
Configure the security event ribbon on the Instance Security Center homepage to include only those events that are relevant for tracking instance security in your operations. You can also change the order in which the security event tiles appear on the ribbon.
-   **[Set preferences for security event notifications](../task/enable-notification-preferences.md)**  
Configure preferences for the types of notifications you want to receive for occurrences of specific security events. For each type, you designate whether to receive notifications by email, by push notification in Now Mobile, or in third party messaging applications such as Slack or Microsoft Teams.

**Parent Topic:**[Instance Security Center](instance-security-center.md)

**Related topics**  


[Instance Security Center to ServiceNow Security Center migration](../../security-center/concept/instance-security-center-to-security-center-migration.md)

[Check the daily compliance score and configure security property settings](instance-sec-center-hardening.md)

[Scan for incorrect security definitions](scan-for-incorrect-security-definitions.md)

[Monitor instance metrics](monitoring-user-email-antivirus-metrics.md)

[Activate the ISC Virtual Agent interface](../task/activating-virtual-agent-interface.md)

[Instance Security Center](instance-security-center.md)

[Now Intelligence](https://www.servicenow.com/docs/access?context=c_performanceAnalyticsAndReporting&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US)

[Analytics Hub](https://www.servicenow.com/docs/access?context=c_UsePerformanceAnalyticsScorecards&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US)

[Performance Analytics targets and thresholds](https://www.servicenow.com/docs/access?context=pa-targets-thresholds&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US)

