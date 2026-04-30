---
title: User metrics
description: Analyze user metrics to look for anomalous behaviors that are related to specific types of user activity in your instance.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2025-04-22"
reading_time_minutes: 3
breadcrumb: [Monitor instance metrics, Instance Security Center, Platform Security]
---

# User metrics

Analyze user metrics to look for anomalous behaviors that are related to specific types of user activity in your instance.

## Not Logged in Last Month / Last Six Months / Last Year

Indicates the number of users who have not logged into the instance within the last month, within the last six months, and within the last calendar year. To view user detail for a specific metric:

-   Click the metric to view a listing of users that have not logged in to the instance during the indicated time period.
-   Click a user name to view more details about that user.

## Users with High Privilege Roles

Indicates the number of users with the following high privilege role types:

|User role|Description|
|---------|-----------|
|admin|Primary administrator role that has access to all system features, functions, and data, regardless of security constraints.|
|ais\_high\_security\_admin|Elevated privilege role that enables a user to access High Security settings for AI Search. To learn more, see [Assign roles to AI Search administrators and users](https://www.servicenow.com/docs/access?context=assign-ais-admin-role&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).|
|password\_reset\_admin|Administrator role that enables a user to view the status of password reset activities, identify potential security threats, and monitor for compliance with password security policies. To learn more, see [Password Reset and Password Change reports and logs](https://www.servicenow.com/docs/access?context=c_MonitorPasswordResetActivity&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).|
|script\_include\_admin|Administrator role that also has access to script includes.|
|security\_admin|Elevated privilege role that enables a user to create and change access controls and High Security Settings. To learn more, see [Security\_admin role](security-admin-role.md)|
|user\_admin|Administrator role that can also manage users, roles, user groups, roles, and department assignments.|

**Note:** To learn more about these administrative role types, see [Special administrative roles](https://www.servicenow.com/docs/access?context=r_SpecialAdministrativeRoles&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

To view user detail for a specific user role metric:

-   Click the user count role metric to view a listing of users with that high privilege role type.
-   Click a user name to view more details about that user. You can then determine if these security-critical roles are assigned to the proper personnel.

## Users Trend

Shows count trend information over a time period for the following types of users:

|Count type|Description|
|----------|-----------|
|Active Users|Number of users who are marked as Active in the instance.|
|Inactive Users|Number of users who are marked as Inactive in the instance.|
|Locked Out|Number of users who are locked out of the instance.|

To view user detail for a specific user count \(for example, Locked Out Users\):

-   Click the **Locked out users** metric.
-   In the Analytics Hub page, click **Show Records**.
-   Click a user name to view more details about that user. You can then determine if there is a reason this person is locked out and remedy the situation.

## Events Trend

Shows count trend information for specific types of events, over a time period:

|Event type|Description|
|----------|-----------|
|Admin login|Number of users with high privilege administrator user roles who logged in on a specific day.|
|External login|Number of users with an assigned snc\_external role who logged into this instance during the calendar day. These logins typically occur for maintenance, support, consulting, or audit purposes. Monitoring this metric enables you to verify that the external login attempts are legitimate and not potential security issues.|
|Failed login|Number of failed login attempts on a specific day.|
|Impersonation|Number of users logged in on a specific day who are impersonating other users.|
|Security elevation|Number of times that a security administrator has elevated security for standard users by changing their assigned user role to a high privilege security role during the calendar day. These high privilege security roles include oauth\_admin, admin, security\_admin, and impersonator.|
|SNC login|Number of Customer Service and Support who logged in to this instance using the hi-hopping technique during a specific day.|

To view user detail for a specific event count \(for example, Impersonation\):

-   Click the user count metric. The Security Dashboard Event Logs page lists event logs for that type of event.
-   Click a user name to view more details about that event.

**Parent Topic:**[Monitor instance metrics](monitoring-user-email-antivirus-metrics.md)

**Related topics**  


[Analytics Hub](https://www.servicenow.com/docs/access?context=c_UsePerformanceAnalyticsScorecards&version=xanadu&pubname=xanadu-now-intelligence&ft:locale=en-US)

