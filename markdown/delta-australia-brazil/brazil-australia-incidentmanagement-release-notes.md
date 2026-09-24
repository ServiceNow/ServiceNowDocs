---
title: Combined Incident Management release notes for upgrades from Australia to Brazil
description: Consolidated page of all release notes for Incident Management from Australia to Brazil.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-australia-brazil/brazil-australia-incidentmanagement-release-notes.html
release: brazil
topic_type: reference
last_updated: "2026-09-24"
reading_time_minutes: 7
breadcrumb: [Products combined by family]
---

# Combined Incident Management release notes for upgrades from Australia to Brazil

Consolidated page of all release notes for Incident Management from Australia to Brazil.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Incident Management release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Australia to Brazil.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Incident Management to Brazil

Before you upgrade to Brazil, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Brazil, new features were introduced for Incident Management.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

-   **[Introduction of granular admin roles](https://www.servicenow.com/docs/access?context=req-itsm-roles-inci-mgmt&family=australia&ft:locale=en-US)**

Configure all the incident, major incident, task outage and related communication features for both UI16 and SOW using the following granular admin roles:

    -   sn\_incident\_admin: Configure all Incident Management features including incident management properties.
    -   sn\_mim\_admin: Configure all Major Incident Management features including major incident properties and trigger rules.
    -   sn\_tcm\_admin: Configure all Task Communications Management features including communication plans and tasks.
    -   sn\_iam\_admin: Configure all Incident Communications Management features including creating, editing, or canceling incident communication plan, communication task, and managing contact information. Additionally, this role can administrate all Incident Communications Management capabilities."
    -   sn\_contact\_admin: Configure all Contact Management features including creating and editing contact definitions, contact responsibilities, configuration of MI users, recipient lists, and groups.
    -   sn\_task\_outage\_admin: Configure all Task Outage features including the mapping between the Task \[task\] table and the Outage \[cmdb\_ci\_outage\] table.
-   **[Form channel for response templates](https://www.servicenow.com/docs/access?context=working-incident-record-form&family=australia&ft:locale=en-US)**

The form channel is added to the Need more information and Schedule meeting response templates. The channel enables you to access the response templates from the incident record, copy the response templates texts to the clipboard from the incident form to be shared in the work notes, comments or other communication channels.


</td></tr><tr><td>

Brazil

</td><td>

-   **[Scheduled job for auto installation of application](https://www.servicenow.com/docs/access?context=activate-major-incident-management-plugin&family=brazil&ft:locale=en-US)**

A scheduled job is now available that executes a batch installation on a new instance to automatically install applications such as Major Incident Management only if you have the necessary entitlements for the application. This is applicable only on the newly provisioned zboot instance.

-   **[Auto resolve On-hold incident](https://www.servicenow.com/docs/access?context=incident-management-properties&family=brazil&ft:locale=en-US)**

When an incident is put to **On-Hold** state with reason as **Awaiting Caller Information**, a notification for input response is sent to the caller for a specific number of attempts or strikes within specific time intervals. The business days are considered for a time interval. If the caller adds a comment on the Service Portal or replies to the notification email, the incident automatically moves to the **In Progress** state, and the assigned agent receives a notification. If the caller does not respond after all attempts are exhausted, the incident is automatically resolved with the resolution code **Resolved - No response from caller** and a resolution note indicating no caller response. You can control the number of attempts or strikes and the time interval between the attempts, using the following incident properties:

    -   The number of attempts made before an incident that is waiting for a caller response is automatically resolved if no reply is received. Setting this value to 0 will disable the automation for this instance - By default, the value is set to 3.
    -   Wait period in business days between two attempts. Incidents will be auto resolved after all the attempts are completed - By default, the value is set to 1.
This is applicable only in the zboot instances.


</td></tr></tbody>
</table>## Changes

Between your current release family and Brazil, some changes were made to existing Incident Management features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

-   **[Incident manager role changes](https://www.servicenow.com/docs/access?context=inci-roles-instld-itsm-roles&family=brazil&ft:locale=en-US)**

The inherited itil role is now removed from the incident manager \[incident\_manager\] role and replaced with the incident\_write role. The is applicable only for the zboot instances. This change restricts access to incident records only, aligning permissions with the intended scope of the role and reducing unnecessary access to unrelated process areas.

-   **[Major incident manager and communication plan manager role changes](https://www.servicenow.com/docs/access?context=installed-with-mim&family=brazil&ft:locale=en-US)**

The major incident manager \[major\_incident\_manager\] and communication plan manager \[sn\_comm\_management.comm\_plan\_mgr\] roles no longer inherit the itil role. Instead, the roles inherit the sn\_incident\_write, sn\_problem\_write, sn\_change\_write, sn\_request\_write granular roles from the ITSM Roles plugin \(com.snc.itsm.roles\). This is applicable only for the zboot instances.

For the upgrade instances, the itil role remains inherited. Additionally, the sn\_incident\_write, sn\_problem\_write, sn\_change\_write, and sn\_request\_write granular roles are added if the ITSM Roles plugin \(com.snc.itsm.roles\) is installed.

-   **[Communication plan viewer role changes](https://www.servicenow.com/docs/access?context=components-installed-with-icm&family=brazil&ft:locale=en-US)**

The sn\_dex\_desktop.notification\_template\_admin role is now removed from the communication plan viewer \[sn\_comm\_management.comm\_plan\_viewer\] role and added to the sn\_incident\_write role when ITSM Roles plugin \(com.snc.itsm.roles\) is installed. In case, ITSM Roles plugin \(com.snc.itsm.roles\) is not installed, the sn\_dex\_desktop.notification\_template\_admin role is added to the itil role. These role changes are applicable only for the zboot instances.

-   **[Itil role check removal from comm\_channel create and write ACLs](https://www.servicenow.com/docs/access?context=components-installed-with-icm&family=brazil&ft:locale=en-US)**

The itil role reference check is now removed from the comm\_channel create and write ACLs. Create and access to the communication channel definition in the incident communication tasks is based on the commTaskGr.state.canWrite script and if you have the following roles:

    -   Communication plan manager \[sn\_comm\_management.comm\_plan\_mgr\]
    -   Communication plan admin \[sn\_comm\_management.comm\_plan\_admin\]
    -   Task communication management admin \[sn\_tcm\_admin\]
    -   ITSM granular roles such as sn\_incident\_write and the user assigned to the incident communication task and plan.
-   **[Auto close resolved incidents behavior changes](https://www.servicenow.com/docs/access?context=incident-management-properties&family=brazil&ft:locale=en-US)**

The resolved incidents are now automatically closed after a specific number of business days instead of calendar days. You can use configure the number of business days using **Number of days \(integer\) after which Resolved incidents are automatically closed. Zero \(0\) disables this feature** \[**glide.ui.autoclose.time**\] property. This changes helps the maintaining the internal organizational policies.


</td></tr></tbody>
</table>## Removed

Between your current release family and Brazil, some Incident Management features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Brazil, some Incident Management features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Activation information

Review information on how to activate Incident Management.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

-   **Activation information**

Incident Management is a ServiceNow AI Platform feature that is active by default.


</td></tr><tr><td>

Brazil

</td><td>

-   **Activation information**

Incident Management is a ServiceNow AI Platform feature that is active by default.


</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Incident Management we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for Incident Management we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for Incident Management, such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

-   **Accessibility information**
    -   Accessibility improvements were made to the Incident Management UI16 form across the full form lifecycle, including keyboard navigation, voice-over support, color contrast, and minimum target sizes. These updates benefit users who rely on screen readers or other Assistive Technology \(AT\), keyboard-only users, and users with low vision.
    -   Accessibility improvements were made to the Major Incident Management UI List component, record pages and Major Incident workbench tabs, including keyboard navigation and screen reader support. These updates benefit users who rely on screen readers or other Assistive Technology \(AT\), keyboard-only users, and users with low vision.
    -   Reflow support for Incident Management and Major Incident Management: Content can be zoomed up to 400% through your browser settings, with page layouts automatically transforming into a vertical, stacked view without loss of content or functionality. This enhancement helps users with low vision or who have trouble seeing web content due to monitor size, device type, poor lighting, or other situations.

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Incident Management we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for Incident Management we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

-   Perform the incident, major incident, task outage, and related communication features configurations using granular admin roles.
-   Enhance communication capabilities with the form channel added to response templates.

 See [Incident Management](https://www.servicenow.com/docs/access?context=c_IncidentManagement&family=australia&ft:locale=en-US) for more information.

</td></tr><tr><td>

Brazil

</td><td>

-   Log incidents in the instance or by sending email.
-   Classify incidents by impact and urgency to prioritize work.
-   Assign to appropriate groups for quick resolution.
-   Escalate as necessary for further investigation and resolution.
-   Use reports to monitor, track, and analyze service levels and improvement.

 See [Incident Management](https://www.servicenow.com/docs/access?context=c_IncidentManagement&family=brazil&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/delta-australia-brazil/rn-combined-intro.md)

