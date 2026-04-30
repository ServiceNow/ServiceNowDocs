---
title: Instance Security Center
description: Monitor the compliance level of instance security controls, view security event monitoring metrics, and configure and maintain instance security settings all from within the Instance Security Center. The Instance Security Center consolidates several key security components into a single control console that helps you detect, protect, and respond to instance-based security events.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 14
breadcrumb: [Platform Security]
---

# Instance Security Center

Monitor the compliance level of instance security controls, view security event monitoring metrics, and configure and maintain instance security settings all from within the Instance Security Center. The Instance Security Center consolidates several key security components into a single control console that helps you detect, protect, and respond to instance-based security events.

**Important:**

Instance Security Center \(ISC\) has reached the end of sales as of September 2024, and is no longer supported or available for new activation.

ServiceNow Security Center \(SSC\) is the recommended solution going forward. For more information, see [Instance Security Center to ServiceNow Security Center migration](../../security-center/concept/instance-security-center-to-security-center-migration.md).

## Instance Security Center components

To access the Instance Security Center, navigate to **System Security** &gt; **Instance Security Center** or the System Administration homepage.

![Instance security center homepage](../image/instance-security-center.png)

The Instance Security Center homepage contains the following security components:

-   Administrator messages
-   Rotating security banner
-   Search
-   Security event ribbon
-   Daily compliance score
-   PCI Configuration Controls Score
-   Session Management
-   Hardening
-   Auditor
-   Metrics \(user, email, and antivirus\)
-   Resources
-   Security notifications
-   Tours
-   Security testing portal
-   Security center
-   Help
-   Virtual Agent access

From the Instance Security Center homepage, you can view the security compliance score for your instance and monitor its overall security health. You can then configure or update system properties that are related to your instance security so that they comply with security requirements.

**Note:** The Instance Security Center does not support domain separation.

## User roles

To use the Instance Security Center, you must have the admin or security\_dashboard\_user role.

To learn more about managing per-user subscriptions, see [Managing per-user subscriptions in Subscription Management](https://www.servicenow.com/docs/access?context=managing-user-subscriptions-v2&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US) and contact your account representative.

<table id="table_td4_gmj_fzb"><thead><tr><th>

Required role

</th><th>

User

</th><th>

Benefits

</th></tr></thead><tbody><tr><td>

admin

</td><td>

This role has access to all system features, functions, and data because administrators can override access control list \(ACL\) rules and pass all role checks. Avoid assigning this role to your users when more targeted roles are available.

</td><td>

Leverage Security Center tools to improve instance security posture and monitor security related behaviors.

</td></tr><tr><td>

sn\_vsc.security\_center\_viewer

</td><td>

This role allows users who are not Admins to view the information in Security Center but not make changes to the Security Center tools or make instance configurations change leveraging the Security Center tools.

 For example, platform owners, security operations analysts or compliance stakeholder might want or need to view some of the security KPIs, security insights and security learning material available in Security Center.

</td><td>

Gain visibility into Security Center tools to monitor instance security posture and monitor security behaviors.

</td></tr></tbody>
</table>**Warning:** To ensure that the Instance Security Center receives up-to-date security information with every upgrade, do not customize this module. If you change any security settings on your instance, make sure that you test them in a non-production environment first.

## Administrator messages

Messages and reminders, intended mostly for administrators, appear above the rotating security banner.

For example, a `Configure Security Notifications` message appears to remind administrators to configure preferences for security notifications if they have not done so. It also points them to the proper page to do so.

**Note:** The administrator messages banner does not appear for non-admin users, or if there are no actionable items for admin users.

## Rotating security banner

To assist you in monitoring the security health of your instance, critical instance security messages appear in the rotating banner.

-   Two to three security messages normally rotate at a regular interval.
-   The dots at the bottom of the banner show you the total number of current security messages.
-   To navigate through them, select the dots, or select the arrows that appear on either side of the messages.

The banner background colors indicate the relative severity of the messages.

|Color|Description|
|-----|-----------|
|Red|Critical security situation requiring a timely response, or a recommendation on how to protect or respond to critical security events.|
|Dark gray|Non-critical warning message.|
|Blue|General information message.|

To collapse or minimize the text content in the banner, select ![Collapse/expand banner](../image/Inst_sec_center_banner_collapse_expand.png). To maximize the text content, select it again.

-   When you use the Instance Security Center again, the text content appeared as collapsed or expanded, depending on how you used it during your previous session.
-   If the text content itself changes, it appears as maximized for all users.

## Search

Use the search bar to search the entire Instance Security Center for security resources that assist you with understanding and resolving security issues. You can search the following security-related resources:

-   Now Support Knowledge Base articles
-   Instance Security Center pages
-   External Now Support links
-   PA security widgets, such as the Daily Compliance Score and External Incoming Emails
-   Banner content

## Event ribbon

Use the event ribbon to view key security event monitoring metrics for the current instance.

-   To manually scroll through the metrics, select the right or left arrow keys.
-   To configure the event ribbon, select **Edit**.

To learn more about the event ribbon and how to configure it, see [Monitor security events](instance-sec-center-event-ribbon.md) and [Configure the security event ribbon](../task/instance-sec-center-configure-event-ribbon.md).

## Daily compliance score

The Daily Compliance Score section contains the **Daily Compliance Score**, **Session Management**, **Hardening**, **Auditor**, and **Resources** tiles.

You use the Daily Compliance Score to gauge how healthy your instance is from a security standpoint.

The Daily Compliance Score is a percentage score. It is based on how compliant the current settings of your instance security properties are with the compliance values published in the [Hardening settings](../../security-center/reference/security-hardening-settings.md).

-   To learn more about Daily Compliance Score calculations, and how hardening settings impact it, see [Check the daily compliance score and configure security property settings](instance-sec-center-hardening.md).
-   The **Refresh** button enables an administrator to instantly recalculate the Daily Compliance Score. To learn more, see [How Daily Compliance score, trend, and graph data is refreshed](how-daily-compl-score-trend-date-refreshed.md).

## Hardening

Use this process to adjust the specific security configuration properties that affect the Daily Compliance Score:

1.  To access the Hardening Compliance Configurations page and perform instance security hardening, select the **Daily Compliance Score** tile or the **Hardening** link.
2.  Specify whether you want to view all or only recommended security controls. Then, select the category you want to work in.
3.  Set each security configuration property in the selected category. Click **More Info** to view detailed information for a property.

To learn more about hardening and optimizing security configuration properties to further increase compliance, see [Adjust instance security settings to increase compliance](../task/update-security-hardening-params.md).

To learn more about how trend and graph data is refreshed, see [How Daily Compliance score, trend, and graph data is refreshed](how-daily-compl-score-trend-date-refreshed.md).

## Auditor

Run the Auditor to scan your instance and find incorrect security definitions. It provides findings you can correct to help improve the security posture of your instance.

To access the Auditor page, select the **Auditor** tile or the **Auditor** link. To learn more, see [Scan for incorrect security definitions](scan-for-incorrect-security-definitions.md).

## Session management

Use Session Management to:

-   View and manage user login sessions.
-   See the user login session of the current node that you are connected to.
-   See detailed information about each session, such as the user name and IP address.
-   Isolate and lock out specific user sessions that pose security risks.

To access the Session Management page, select the **Session Management** tile or link.

<table id="table_kxg_qzk_ddb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

User

</td><td>

Name of the user associated with this login session. -   To locate a specific user session, select the spotlight search icon \( ![Search](../image/Search.png)\) to search by user, user agent keyword, or IP address.

For example, if you want to find all current logins from a specific type of browser, enter the browser name as a keyword into the **User Agent** field.

-   Click a user name to access the user profile record. You can modify the user profile only if you have an assigned admin role.

**Note:** To learn more about user profiles, see [Create a user](https://www.servicenow.com/docs/access?context=t_CreateAUser&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).


</td></tr><tr><td>

MFA

</td><td>

Check box indicating if Multi-factor Authentication \(MFA\) is enabled for the logged in user. To learn more about MFA, see [Multi-factor authentication \(MFA\)](../../../integrate/authentication/concept/c_MultifactorAuthentication.md).

</td></tr><tr><td>

Active

</td><td>

Check box indicating if the logged in user is active or inactive.

</td></tr><tr><td>

User Agent

</td><td>

Type of browser and the device operating system for the user login session.

</td></tr><tr><td>

IP Address

</td><td>

IP address of the logged in user.

</td></tr><tr><td>

Last Accessed

</td><td>

Date and time this user session last accessed the instance.**Note:** To view detailed information for a particular login session, or to lock out the session itself, select the **User Agent**, **IP Address**, or **Last Accessed** fields.

</td></tr></tbody>
</table>## Metrics

View detail for the following types of metrics:

<table id="table_wgs_mkq_nnb"><thead><tr><th>

Type of metric

</th><th>

Description

</th></tr></thead><tbody><tr><td>

User

</td><td>

Security metrics that are associated with user activity in the instance. To access the User Metrics page, select the **Metrics** link, and then select **User Metrics**.

</td></tr><tr><td>

Export

</td><td>

Security metrics that are associated with data exported from the instance. To access the Export Metrics page, select the **Metrics** link, and then select **Export Metrics**.

</td></tr><tr><td>

Authentication

</td><td>

Security metrics that are associated with authentication, such as infrequently used IP addresses, failed logins, and types of authentication schemes used by your users.To access the Export Metrics page, select the **Metrics** link, and then select **Authentication Metrics**.

</td></tr><tr><td>

Email

</td><td>

Security metrics associated with anomalous behaviors related to the incoming emails to your instance. To access the Email Metrics page, select the **Metrics** link, and then select **Email Metrics**.

</td></tr><tr><td>

Antivirus

</td><td>

Security metrics that are associated with antivirus event activity in the instance. To access the Antivirus Metrics page, select the **Antivirus** tile or select the **Metrics** link, and then select **Antivirus**.

</td></tr></tbody>
</table>**Note:** To learn more about monitoring each type of metric, see [Monitor instance metrics](monitoring-user-email-antivirus-metrics.md).

## Resources

Access Now Support Knowledge Base articles, resources, and blogs that are related to instance security. These resources include security settings, coding, compliance, fixes, and related topics. To access the Resources page:

1.  Click the **Resources** tile or link.
2.  In the Resources page, select a category:

<table id="table_xwr_xvz_1jb"><thead><tr><th>

Category

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Recommended Guidelines

</td><td>

Access to recommended security guidelines, including the [Hardening settings](../../security-center/reference/security-hardening-settings.md) and [Secure Coding Guide](https://support.servicenow.com) \[KB0623354\] articles.

</td></tr><tr><td>

Security Resources

</td><td>

Access to security-related resources in the Knowledge Base, including:-   Customer Instance Security Testing
-   Cloud Security, Trust, and Compliance Center KB articles


</td></tr></tbody>
</table>
## Security notifications

A notifications bell icon \(![Notification icon](../image/Inst_sec_center_notif_bell_icon.png)\) appears in the Instance Security Center, with a count total of unread security notifications. Notifications persist and are included in this count until you mark them as read.

1.  Click the bell icon to view the first five unread security notifications.

    A notification appears when **Admin Login**, **Admin Unlocked**, **Failed Login**, **High Privilege Role**, **Impersonation**, **Security Elevation**, and **Weekly Digest** events take place in your instance. To learn more about these security events, see [Monitor security events](instance-sec-center-event-ribbon.md).

2.  To view detailed information for a specific security event, select the notification.

    For example, if you select a High Privilege Role notification, you can view the Roles \(sys\_user\_role\) table. Use this table to see which users were assigned privileged roles during the calendar day. Using this history helps you to determine if roles have been properly assigned.

3.  If there are more than five unread notifications, select **View All Notifications** to access an All Notifications page with a listing of all unread notifications.
    -   To view detailed information for a specific security event, select the notification.
    -   To mark all listed notifications as read, select **Mark All as Read**.

**Note:** As an administrator, you can also configure preferences for sending specific types of notifications for each type of security event. To learn more, see [Set preferences for security event notifications](../task/enable-notification-preferences.md).

## Tours

Click the **Tours** link to view a guided visual tour of the Instance Security Center.

-   The guided tour includes only the security monitoring functions that are listed on the homepage.
-   It does not include the security functions that you access when you select the tiles or links on the homepage.

## Security testing portal, security center, and help

The Now Support Service Portal is a central resource that you use to manage instances, tasks, and accounts. You can also access useful resources you can use to diagnose and resolve security and technical issues in your instance.

To access these resources, select **Learn More** or **Get Help** in the following tiles:

<table id="table_ahj_jph_z3b"><thead><tr><th>

Tile

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Security Testing Portal

</td><td>

Access to the Security Dashboard in the Now Support Security Testing Portal.

</td></tr><tr><td>

Security Center

</td><td>

Access to Security Compliance in the Now Support Security Portal.

</td></tr><tr><td>

Help

</td><td>

Access to the following help resources in the Now Support Security Portal:-   Ask an expert to find answers to common questions.
-   Report an issue or outage to ServiceNow Global Technical Support by opening a case.
-   Self-Service Support Resources, including:
    -   Videos
    -   Documentation
    -   ServiceNow Community
    -   Knowledge Base
    -   Known Error Portal
    -   Security RFX Database
-   ServiceNow Community questions that are recommended for your use.

</td></tr></tbody>
</table>## Virtual Agent access

The Virtual Agent is a platform for providing user assistance through conversations within a messaging interface.

With the associated plugins installed, administrators can access the Virtual Agent and Natural Language Understanding \(NLU\) functions by selecting the Virtual Agent icon:

![Virtual Agent icon](../image/instance-sec-center-virtual-agent.png)

It enables you to perform the following tasks:

-   Ask security-related questions, then get quick summary answers and reference links to learn more.
-   Get answers related to processes such as:
    -   Instance Security Center
    -   Platform Security
    -   ServiceNow security policies
    -   Trust, Governance, and Risk
-   Search for security-related resources, such as Knowledge Base topics in the Now Support Security Portal.

**Note:** To learn more about how to use and activate the Virtual Agent, see:

-   [Virtual Agent](https://www.servicenow.com/docs/access?context=virtual-agent-landing-page&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US)
-   [Activate the ISC Virtual Agent interface](../task/activating-virtual-agent-interface.md)

-   **[Instance Security Center to ServiceNow Security Center migration](../../security-center/concept/instance-security-center-to-security-center-migration.md)**  
Learn the key differences when migrating from Instance Security Center \(ISC\) to ServiceNow Security Center \(SSC\).
-   **[Monitor security events](instance-sec-center-event-ribbon.md)**  
Analyze the event metrics in your instance so that you can identify and prevent potential security events.
-   **[Check the daily compliance score and configure security property settings](instance-sec-center-hardening.md)**  
Review the Daily Compliance Score metric and security configuration properties to see if your instance complies with the suggested security requirements. You can affect the daily compliance score by updating non-compliant security properties in the Hardening Compliance Configurations page.
-   **[Scan for incorrect security definitions](scan-for-incorrect-security-definitions.md)**  
Run the Auditor to scan your instance and find incorrect security definitions. It provides findings you can correct to help improve the security posture of your instance.
-   **[Monitor instance metrics](monitoring-user-email-antivirus-metrics.md)**  
Monitor user, export, authentication, email, and antivirus metrics for your instance. For example, you can monitor your email security by checking metrics for spam, external emails, and inbound emails from untrusted and trusted domains for your instance. Analyze these metrics to look for anomalous security behaviors that are related to activities that take place in your instance.
-   **[Activate the ISC Virtual Agent interface](../task/activating-virtual-agent-interface.md)**  
If you have the admin role, you can activate the ISC Virtual Agent Conversations plugin \(com.glide.isc\_virtualagent\). Activating this plugin installs the Virtual Agent and Natural Language Understanding \(NLU content packs, providing Virtual Agent access from the Instance Security Center.

**Parent Topic:**[Platform Security](../../general/concept/platsec-sublanding.md)

