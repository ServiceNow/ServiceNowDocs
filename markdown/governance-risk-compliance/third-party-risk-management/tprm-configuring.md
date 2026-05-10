---
title: Configuring Third-party Risk Management
description: You can activate or upgrade TPRM, by downloading the applications from the ServiceNow Store and then configuring the settings to meet your needs.
locale: en-US
release: australia
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Third-party Risk Management, Governance, Risk, and Compliance]
---

# Configuring Third-party Risk Management

You can activate or upgrade TPRM, by downloading the applications from the ServiceNow Store and then configuring the settings to meet your needs.

## Configuration overview

By performing the tasks in the Setup tasks for TPRM checklist, you can upgrade or install the TPRM application. After you’ve completed the tasks, you can perform additional configuration as described in [Classic assessment configuration](../../grc-vendor-risk-implementation/concept/tprm-ongoing-config.md).

**Note:**

For any custom messages you create, it is your responsibility to generate the corresponding `sys_ui_message` records. This step is crucial if you want the custom messages to be extracted and translated.

## Initial setup and upgrade checklist for TPRM

<table id="table_ytv_tf2_kxb"><thead><tr><th>

Task

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Activate the Third-party Risk Management app \[com.sn\_vdr\_risk\_asmt\].

</td><td>

To see the instructions for downloading a GRC application from the ServiceNow® Store, see [Download a GRC application from the ServiceNow Store for the first time](../../grc-common/task/download-grc-first-time.md).**Important:** The base system includes many sample questions that you can use in your question bank. To include sample questionnaires, select **Load demo data** while installing the app.

Role required: admin

</td></tr><tr><td>

Activate the Due diligence request workflow application \[com.sn\_tprm\_dd\].

</td><td>

To see the instructions for downloading a GRC application from the ServiceNow® Store, see [Download a GRC application from the ServiceNow Store for the first time](../../grc-common/task/download-grc-first-time.md).Role required: admin

</td></tr><tr><td>

Activate the Vendor Risk Management Workspace application \[sn\_vrm\_ws\].

</td><td>

To see the instructions for downloading a GRC application from the ServiceNow® Store, see [Download a GRC application from the ServiceNow Store for the first time](../../grc-common/task/download-grc-first-time.md).Role required: admin

</td></tr><tr><td>

Add an authentication policy to enable secure access for external third parties.

</td><td>

For more information, see [Add an authentication policy to enable secure access for external third parties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/authentication/add-policy-to-context.md).

 Role required: admin

 Use the platform post-authentication policies to enable third parties to secure access to your instance. For background information on this feature, see [Post-authentication context](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/authentication/post-auth-context.md).

</td></tr><tr><td>

Assign TPRM roles to users and user groups.

</td><td>

Assign roles to users before you implement or use the Third-party Risk Management application. Assigning roles in a well-organized manner simplifies and improves process management and helps to ensure that users are promptly notified of tasks in their areas of responsibility.

 For more information, see [Assign TPRM roles to users and user groups](../../grc-vendor-risk-implementation/task/tprm-roles-assign.md).

 Role required: admin

</td></tr><tr><td>

Add users to groups based on their responsibilities.

</td><td>

Assign users to groups before you implement or use the Third-party Risk Management application. Each group contains users with particular roles. Well-organized user groups simplify and improve process management and help to ensure that users are promptly notified of tasks in their areas of responsibility.

For more information, see [Add users to groups based on responsibilities](../../grc-vendor-risk-implementation/task/tprm-groups-add-users-to.md).Role required: admin

</td></tr><tr><td>

Configure TPRM properties.

</td><td>

Configure property settings for a variety of TPRM operations.

 For more information, see [Configure TPRM properties](../../grc-vendor-risk-implementation/task/tprm-properties-configure.md).

 Role required: admin

</td></tr><tr><td>

Enable the TPRM Risk concentration map.

</td><td>

This task is optional. For more information, see [Enable the TPRM Risk concentration map](../../grc-vendor-risk-implementation/task/tprm-risk-map-configure.md).

 Role required: admin

 After you install the Risk concentration map feature, you must install a Google license to enable the feature.

</td></tr><tr><td>

Enable your emails with third-party contacts.

</td><td>

Configure email communication with third-party contacts to enable email notification of assessments and issues.

 For more information, see [Enable email with third-party contacts](../../grc-vendor-risk-implementation/task/set_sys_props_for_email.md).

 Role required: admin

</td></tr><tr><td>

Update header and footer images for email notifications.

</td><td>

Update the header and footer images used in email notifications by modifying image records.For more information, see [Update the header and footer for email notifications](../../grc-vendor-risk-implementation/task/set_logo_for_email.md).

Role required: admin

</td></tr><tr><td>

Import the existing data from other systems.

</td><td>

This task is optional. Import existing data \(third parties, engagements, assessments, questionnaires, issues, and so on\) from other systems \(like the Aravo platform, the ProcessUnity platform, and so on\). You aren’t charged for importing the data.

 For more information, see [Import existing data from other systems](../../grc-vendor-risk-implementation/task/tprm-historical-data-import.md).

 Role required: admin

</td></tr><tr><td>

Set up third-party contacts.

</td><td>

Third-party contacts are external users at the third-party organization. They use the Third-party portal to securely organize, prioritize, and perform tasks like responding to questionnaires for assessments, performing tasks, and communicating with your risk-assessment staff regarding issues. You grant access to the Third-party portal and specify the permissions for third-party contacts.

 For more information, see [Set up third-party contacts](../../grc-vendor-risk-implementation/task/tprm-tp-contact-config.md).

 Role required: admin or sn\_vdr\_risk\_asmt.vendor\_risk\_manager

</td></tr><tr><td>

Activate a language.

</td><td>

This task is optional. The ServiceNow AI Platform uses American English by default. You can configure TPRM to use a different language.

 For more information, see [Activate a language](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/system-localization/t_ActivateALanguage.md).

 Role required: admin

</td></tr><tr><td>

Run the quick-start tests for third-party risk management.

</td><td>

This task is optional. Verify that TPRM still works after you make configuration changes such as applying an upgrade or developing an application. Copy and customize the quick-start tests to pass when using your instance-specific data.

 For more information, see [Run the Quick Start tests for Third-party Risk Management](../../../administer/atf-quick-start-tests/reference/quick-start-tests-grc-vrm.md).

</td></tr><tr><td>

Configure related lists in the Vendor Management Workspace.

</td><td>

This task is optional.

 Configure the related lists that appear in the vertical navigation layout on record pages in the Vendor Management Workspace.

 For more information, see [Configure related lists for vertical navigation on record pages](../task/config-related-list-vert-nav.md).

</td></tr></tbody>
</table>**Related topics**  


[Classic assessment configuration](../../grc-vendor-risk-implementation/concept/tprm-ongoing-config.md)

[Smart assessment configuration](../../grc-vendor-risk-implementation/concept/tprm-sae-assessment-config.md)

