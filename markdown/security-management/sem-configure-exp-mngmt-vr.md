---
title: Configure Exception Management for Security Exposure Management
description: When your organization can't comply with a vulnerability management or security policy, standard, or guideline, you can request an exception. Exception management entails requesting, reviewing, approving, or rejecting exceptions to a finding or remediation task \(RT\) that can't be remediated according to the policy.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/sem-configure-exp-mngmt-vr.html
release: australia
topic_type: task
last_updated: "2026-06-05"
reading_time_minutes: 3
breadcrumb: [Implement, Unified Security Exposure Management, Security Operations]
---

# Configure Exception Management for Security Exposure Management

When your organization can't comply with a vulnerability management or security policy, standard, or guideline, you can request an exception. Exception management entails requesting, reviewing, approving, or rejecting exceptions to a finding or remediation task \(RT\) that can't be remediated according to the policy.

## Before you begin

Use the Security Exposure Management workspace to limit the duration of an exception request and add a questionnaire to the exception or false positive request. You can also request an exception using the GRC: Policy and Compliance Management integration.

Role required: sn\_vul\_exception.admin

## About this task

If Vulnerability Response is enabled, you can limit the duration for which an exception can be requested. Similarly, if the GRC: Policy and Compliance Management module is installed, you can select GRC: Policy and Compliance Management on the configuration screen. Enabling this option enables you to request an exception that specifies the Policy and Control objective from GRC.

The exception approver requires the reason for the exception request.

## Procedure

1.  Navigate to **Workspaces** &gt; **Security Exposure Management Workspace** &gt; **Administration** &gt; **Exception Management** &gt; **Review** &gt; **Basic configuration**.

2.  Select one of the following apps: **Vulnerability Response Exception Management**, **Application Vulnerability Response Exception Management**, **Container Vulnerability Response Exception Management**, **Configure Compliance Exception Management**.

3.  On the Exception Management Configuration page, select how you want to manage an exception by selecting an option from the **Manage exceptions using** list.

    You must activate the GRC plugin to use GRC: Policy and Compliance Management to request an exception. Changing the configuration doesn't impact the existing data.

4.  If you selected the settings for any of the apps, enter the following information:

    |Field|Description|
    |-----|-----------|
    |Exception management ownership|Read-only when the GRC plugin is not installed.|
    |Questionnaire for exception request|Displays the questionnaire selected by you to request an exception. The **Exception Questionnaire** is displayed by default. You can also select questionnaire from the drop-down list.|
    |Questionnaire for compensating control|Displays the questionnaire that a remediation owner must answer for risk reduction requests. You can set questionnaire for risk reduction requests. The **Compensating Control Questionnaire** is selected by default. You can also select questionnaire from the drop-down list. \(This option is not available for CC Exception Management\).|
    |Maximum Duration for exception \(days\)|Maximum number of days for which an exception can be requested.|
    |Questionnaire to mark false positive|Questionnaire for marking a finding as a false positive. The default questionnaire is selected. Select a different questionnaire from the list.|

    **Note:**

    The questionnaire displayed to you depends on the exception type selected and which questionnaire fields are configured in this record:

    -   When only **Request for Deferral** is selected, the questionnaire for exception request is displayed if configured.
    -   When **Request for Risk Reduction** is selected \(with or without deferral\), the questionnaire for compensating control takes priority and is displayed if configured.
    -   When the relevant questionnaire field is empty, the exception request is submitted directly without prompting a questionnaire.
5.  If you selected the GRC: Policy and Compliance Management option, enter the following information:

    |Field|Description|
    |-----|-----------|
    |Questionnaire to mark false positive|Questionnaire for marking a finding as a false positive. The default questionnaire is selected.|

6.  Configure conditional questionnaires based on conditions for exception and false-positive requests:

    1.  In the Exception Management Conditional Questionnaires section, select **New**.

    2.  In the New conditional questionnaire form, fill in the fields and select **Save**.

        The created questionnaire appears in the VR Questionnaire Configuration section of the Settings for VR Exception Management form.

    For example, to configure a questionnaire for false-positive requests for critical vulnerable items, select the **False positive for vulnerable items** approval rule, provide the condition as `Risk rating is 1 - Critical` and select the desired questionnaire in the Questionnaire configuration form.

7.  Select **Design New Questionnaire**.

    Design assessment questionnaires using the templates in the Assessment Workspace.

8.  Select **Save**.


-   **[Request an exception using GRC: Policy and Compliance Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/sem-integration-with-grc.md)**  
Request policy exceptions using the GRC policy exception management capability in the Policy and Compliance Management application from within Vulnerability Response.
-   **[Specify the duration of an exception requested for a remediation task](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/sem-ex-req-sysprop.md)**  
Use system properties to limit the duration for which an exception is requested for a remediation task. Remediation of the remediation task is deferred for the specified period.

**Related topics**  


[sem-exception-ques-scenarios]

