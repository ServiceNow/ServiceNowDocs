---
title: Incident Management release notes
description: The ServiceNow Incident Management application restores normal service operations while minimizing the impact to business operations and maintaining quality. Incident Management was enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 5
---

# Incident Management release notes

The ServiceNow® Incident Management application restores normal service operations while minimizing the impact to business operations and maintaining quality. Incident Management was enhanced and updated in the Yokohama release.

## Incident Management highlights for the Yokohama release

-   Increase the operational efficiency of the tier 1 service desk agents with the dedicated sn\_service\_desk\_agent role.
-   Control whether an incident or major incident record link in an email notification redirects you to the record in the classic UI16 interface or Service Operations Workspace \(SOW\).
-   Enable agents with incident write access, callers, requesters, and **Opened by** end users to reopen a resolved incident from the Incident Management classic UI16 form, SOW, or Portal UIs.
-   Restrict unauthorized access to incident-related tables using deny ACLs.
-   Search for a configuration item \(CI\) in a list alphabetized by the CI name with an improved search performance.

See [Incident Management](https://www.servicenow.com/docs/access?context=c_IncidentManagement&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US) for more information.

## New in the Yokohama release

-   **[User role for service desk agents](https://www.servicenow.com/docs/access?context=inci-roles-instld-itsm-roles&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

    With the sn\_service\_desk\_agent user role, increase the operational efficiency by streamlining the process of asking about, gathering, and verifying information, as well as delivering quick resolutions. This role is designed for tier 1 service desk agents and is accessible when the ITSM Roles plugin \(com.snc.itsm.roles\) installed.

    The sn\_service\_desk\_agent role includes the following user roles:

    -   sn\_incident\_write
    -   sn\_problem\_write
    -   sn\_change\_write
    -   sn\_request\_write
    -   tracked\_file\_reader
    Additionally, with the installation of the ITSM Gen AI \(com.sn.itsm.gen.ai\) plugin, the knowledge\_user, and now\_assist\_panel\_user roles are integrated within the sn\_service\_desk\_agent role.

    The sn\_service\_desk\_agent role can be used starting with SOW version 6.1.

-   **[Enhanced security model adoption for incident tables](https://www.servicenow.com/docs/access?context=activate-itsm-enhanced-security-inci-mangmnt&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

    Help prevent unauthorized access to incident-related tables using Deny-Unless ACLs. A Deny-Unless authentication ACL restricts access for a non-authenticated user, such as a public role user. Without access, the user can't perform any actions on incident-related tables, including reading, writing, deleting, creating, or accessing the report view.

    This feature is activated automatically and applicable on the following incident-related tables:

    -   kb\_template\_incident\_kcs\_articl
    -   kb\_template\_incident\_kcs\_template
    Additionally, this feature is available on the following incident-related tables of new or zBoot instances after installing the ITSM Enhanced Security Features \(com.snc.itsm.enhanced\_security\) plugin:

    -   incident
    -   incident\_task
    -   task\_ci
    -   task outage
    The ITSM Enhanced Security Features \(com.snc.itsm.enhanced\_security\) plugin can be installed and activated by an admin via a support request. Existing or upgrade users must test and evaluate the results in their non-production instance, and then install the plugin and implement the security change in their production instance.

    For more information, see [Deny-Unless ACL](https://www.servicenow.com/docs/access?context=acl-denial-behavior&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).


## Changed in this release

-   **[Email redirection behavior for major incident email notification links](https://www.servicenow.com/docs/access?context=email-notif-redirt-inci-major-inci&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

    In major incident email notifications, you can now decide where the links to a major incident record are redirected. Instead of a major incident record automatically opening in the classic UI16 interface in Major Incident Management, the record can be opened in SOW. The major incident record link in an email notification opens in SOW only if the following conditions are met:

    -   The **Redirect SOW Email notification** \(**sow\_email\_notification\_redirect**\) property is set to `true`. Setting this property to true enables the email redirection behavior for all tables including major incident.
    -   The **Redirect SOW Email notification for Major Incident Management** \(**sn\_major\_inc\_mgmt.sow\_email\_notification\_redirect.mim**\) property is set to `true`.
    -   You have the sn\_sow\_user role.
    The ITSM Notifications Redirection \(com.snc.itsm.notifications\_redirection\) plugin is installed and activated automatically to support this behavior.

-   **[Email redirection behavior for incident email notification links](https://www.servicenow.com/docs/access?context=email-notif-redirt-inci-major-inci&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

    In incident email notifications, you can now decide where the links to an incident record are redirected. Instead of an incident record automatically opening in the classic UI16 interface in Incident Management, the record can be opened in SOW. The incident record link in an email notification opens in SOW only if you have the sn\_sow\_user role and any of the following conditions are met:

    -   The **Redirect SOW Email notification** \(**sow\_email\_notification\_redirect**\) property is set to `true`. Setting this property to true enables the email redirection behavior for all tables including incident.
    -   The **Redirect SOW Email notification for Incident Management** \(**sow\_email\_notification\_redirect.incident**\) property is set to `true`. You can create this property if you want to enable or restrict the email redirection behavior specifically for the incident table. This property, if created and set, overrides the **Redirect SOW Email notification** \(**sow\_email\_notification\_redirect**\) base system property.
    The ITSM Notifications Redirection \(com.snc.itsm.notifications\_redirection\) plugin is installed and activated automatically to support this behavior.

    To ensure consistency, the email notification templates for incident tasks are also updated to send the notification from Service Operations Workspace \(SOW\) in the same format as sent from classic UI16 interface similar to incident. Also, the template theme is updated to match the Next Experience theme.

-   **[Incident and problem workflow changes](https://www.servicenow.com/docs/access?context=incident-management-properties&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

    When a problem is fixed and the **Share fix** option is triggered, the event is added to the **Work notes \(Private\)** field instead of the **Additional comments \(Customer visible\)** field for the incident associated with the problem record.

    This feature is available in the base system for the new customers. For existing or upgrade customers, admin must set the **Communicate problem workaround to incident worknotes** \(**com.snc.incident.communicate\_prb\_workaround\_to\_inc\_worknotes**\) system property to `true` to enable the feature.

-   **[Changes in the reopening incident behavior](https://www.servicenow.com/docs/access?context=reopening-incident&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

    Enable the agents with incident write access, callers, requesters, or **Opened by** end users to reopen a resolved incident. Both the caller and the requester can view and use the **Reopen** option on the incident classic UI16 form and the Portal UIs, such as Service Portal and Employee Service Center \(ESC\) portal.

    An agent can view and use the **Reopen** option on the incident classic UI16 form to reopen any incident that is assigned to them or to other agents. However, on the Portal UI, an agent can only view and use the **Reopen** option to reopen an incident if it’s assigned to them.

-   **[Sorting CIs in incident forms](https://www.servicenow.com/docs/access?context=create-an-incident&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

    The search performance of the available CIs for the **Configuration item** field on an incident form is enhanced to promote a clean UI and quick loading and sorting of the CIs. The search results that list the CIs are sorted alphabetically by CI name instead of by CI class and then CI name. The **ref\_ac\_order\_by=sys\_class\_name** attribute is removed from the default attributes on the **cmdb\_ci** field of the Task \[task\] table, which increases the performance of the field.

    This change is applicable to new and existing users using the default attributes. You can use the **Override attributes** option to restrict this change for any required child tables that extend to the **cmdb\_ci** field of the Task \[task\] table.


## Activation information

Incident Management is a ServiceNow AI Platform feature that is active by default.

**Parent Topic:**[IT Service Management release notes](it-service-management-rn-landing.md)

