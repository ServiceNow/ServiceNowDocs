---
title: Incident Management release notes
description: The ServiceNow Incident Management application helps you to restore normal service operations while minimizing the impact to business operations and maintaining quality. Incident Management was enhanced and updated in the Brazil release. See the following sections for release notes by version.The brazil release adds features to help in automatic application installation and follow-up notifications for on-hold incidents. It also includes automatic state changes from On-hold and inherited role changes for major incident and communication managers.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/incident-management-rn.html
release: brazil
topic_type: topic
last_updated: "2026-09-10"
reading_time_minutes: 4
breadcrumb: [IT Service Management release notes, Features and changes by product, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# Incident Management release notes

The ServiceNow® Incident Management application helps you to restore normal service operations while minimizing the impact to business operations and maintaining quality. Incident Management was enhanced and updated in the Brazil release. See the following sections for release notes by version.

## About Incident Management

-   Log incidents in the instance or by sending email.
-   Classify incidents by impact and urgency to prioritize work.
-   Assign to appropriate groups for quick resolution.
-   Escalate as necessary for further investigation and resolution.
-   Use reports to monitor, track, and analyze service levels and improvement.

See [Incident Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/c_IncidentManagement.md) for more information.

## Activation and other requirements

-   **Activation information**

    Incident Management is a ServiceNow AI Platform feature that is active by default.


## Accessibility and localization

-   **Accessibility information**
    -   Accessibility improvements were made to the Incident Management UI16 form across the full form lifecycle, including keyboard navigation, voice-over support, color contrast, and minimum target sizes. These updates benefit users who rely on screen readers or other Assistive Technology \(AT\), keyboard-only users, and users with low vision.
    -   Accessibility improvements were made to the Major Incident Management UI List component, record pages and Major Incident workbench tabs, including keyboard navigation and screen reader support. These updates benefit users who rely on screen readers or other Assistive Technology \(AT\), keyboard-only users, and users with low vision.
    -   Reflow support for Incident Management and Major Incident Management: Content can be zoomed up to 400% through your browser settings, with page layouts automatically transforming into a vertical, stacked view without loss of content or functionality. This enhancement helps users with low vision or who have trouble seeing web content due to monitor size, device type, poor lighting, or other situations.

**Parent Topic:**[IT Service Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/it-service-management-rn-landing.md)

## Brazil Early Availability

The brazil release adds features to help in automatic application installation and follow-up notifications for on-hold incidents. It also includes automatic state changes from On-hold and inherited role changes for major incident and communication managers.

### What's new

-   **[Scheduled job for auto installation of application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/activate-major-incident-management-plugin.md)**

    A scheduled job is now available that executes a batch installation on a new instance to automatically install applications such as Major Incident Management only if you have the necessary entitlements for the application. This is applicable only on the newly provisioned zboot instance.

-   **[Auto resolve On-hold incident](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/incident-management-properties.md)**

    When an incident is put to **On-Hold** state with reason as **Awaiting Caller Information**, a notification for input response is sent to the caller for a specific number of attempts or strikes within specific time intervals. The business days are considered for a time interval. If the caller adds a comment on the Service Portal or replies to the notification email, the incident automatically moves to the **In Progress** state, and the assigned agent receives a notification. If the caller does not respond after all attempts are exhausted, the incident is automatically resolved with the resolution code **Resolved - No response from caller** and a resolution note indicating no caller response. You can control the number of attempts or strikes and the time interval between the attempts, using the following incident properties:

    -   The number of attempts made before an incident that is waiting for a caller response is automatically resolved if no reply is received. Setting this value to 0 will disable the automation for this instance - By default, the value is set to 3.
    -   Wait period in business days between two attempts. Incidents will be auto resolved after all the attempts are completed - By default, the value is set to 1.
    This is applicable only in the zboot instances.


### What's changed

-   **[Incident manager role changes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/inci-roles-instld-itsm-roles.md)**

    The inherited itil role is now removed from the incident manager \[incident\_manager\] role and replaced with the incident\_write role. The is applicable only for the zboot instances. This change restricts access to incident records only, aligning permissions with the intended scope of the role and reducing unnecessary access to unrelated process areas.

-   **[Major incident manager and communication plan manager role changes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/installed-with-mim.md)**

    The major incident manager \[major\_incident\_manager\] and communication plan manager \[sn\_comm\_management.comm\_plan\_mgr\] roles no longer inherit the itil role. Instead, the roles inherit the sn\_incident\_write, sn\_problem\_write, sn\_change\_write, sn\_request\_write granular roles from the ITSM Roles plugin \(com.snc.itsm.roles\). This is applicable only for the zboot instances.

    For the upgrade instances, the itil role remains inherited. Additionally, the sn\_incident\_write, sn\_problem\_write, sn\_change\_write, and sn\_request\_write granular roles are added if the ITSM Roles plugin \(com.snc.itsm.roles\) is installed.

-   **[Communication plan viewer role changes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/components-installed-with-icm.md)**

    The sn\_dex\_desktop.notification\_template\_admin role is now removed from the communication plan viewer \[sn\_comm\_management.comm\_plan\_viewer\] role and added to the sn\_incident\_write role when ITSM Roles plugin \(com.snc.itsm.roles\) is installed. In case, ITSM Roles plugin \(com.snc.itsm.roles\) is not installed, the sn\_dex\_desktop.notification\_template\_admin role is added to the itil role. These role changes are applicable only for the zboot instances.

-   **[Itil role check removal from comm\_channel create and write ACLs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/components-installed-with-icm.md)**

    The itil role reference check is now removed from the comm\_channel create and write ACLs. Create and access to the communication channel definition in the incident communication tasks is based on the commTaskGr.state.canWrite script and if you have the following roles:

    -   Communication plan manager \[sn\_comm\_management.comm\_plan\_mgr\]
    -   Communication plan admin \[sn\_comm\_management.comm\_plan\_admin\]
    -   Task communication management admin \[sn\_tcm\_admin\]
    -   ITSM granular roles such as sn\_incident\_write and the user assigned to the incident communication task and plan.
-   **[Auto close resolved incidents behavior changes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/incident-management-properties.md)**

    The resolved incidents are now automatically closed after a specific number of business days instead of calendar days. You can use configure the number of business days using **Number of days \(integer\) after which Resolved incidents are automatically closed. Zero \(0\) disables this feature** \[**glide.ui.autoclose.time**\] property. This changes helps the maintaining the internal organizational policies.


