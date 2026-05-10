---
title: Configure Exception Management for Security Exposure Management
description: When your organization can't comply with a published vulnerability management or security policy, standard, or guideline, you can request an exception. Exception management entails requesting, reviewing, approving, or rejecting exceptions to a finding or remediation task \(RT\) that cannot be remediated according to the policy.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-05-09"
reading_time_minutes: 3
breadcrumb: [Implement, Unified Security Exposure Management, Security Operations]
---

# Configure Exception Management for Security Exposure Management

When your organization can't comply with a published vulnerability management or security policy, standard, or guideline, you can request an exception. Exception management entails requesting, reviewing, approving, or rejecting exceptions to a finding or remediation task \(RT\) that cannot be remediated according to the policy.

## Before you begin

Limit the duration of an exception requested and add a questionnaire to the exception or false positive request using the Security Exposure Management workspace. You can also request an exception using the GRC: Policy and Compliance Management integration.

Role required: sn\_vul\_exception.admin

## About this task

If Vulnerability Response is enabled, you can limit the duration for which an exception can be requested. Similarly, if the GRC: Policy and Compliance Management module is installed, you can select GRC: Policy and Compliance Management on the configuration screen. Enabling this option lets you request an exception that specifies the Policy and Control objective from GRC.

It’s useful for the exception approver to understand the reason for requesting the exception.

## Procedure

1.  Navigate to **Workspaces** &gt; **Security Exposure Management Workspace** &gt; **Administration** &gt; **Exception Management** &gt; **Review** &gt; **Basic configuration**.

2.  You can select any one of the apps **Vulnerability Response Exception Management**, **Application Vulnerability Response Exception Management**, **Container Vulnerability Response Exception Management**, **Configure Compliance Exception Management**.

3.  On the Exception Management Configuration page, select how you want to manage an exception by selecting an option from the **Manage exceptions using** list.

    You can select either **Security Exposure Management** or GRC: Policy and Compliance Management. You must activate the GRC plugin to use GRC: Policy and Compliance Management to request an exception. Changing the configuration doesn’t impact the existing data.

4.  If you selected the settings for any of the apps, enter the following information:

    |Field|Description|
    |-----|-----------|
    |Exception management ownership|This is a read-only field if GRC plugin is not installed.|
    |Questionnaire for exception request|Displays the questionnaire selected by you to request an exception. The **Exception Questionnaire** is displayed by default. You can also select questionnaire from the drop-down list.|
    |Questionnaire for compensating control|Displays the questionnaire that a remediation owner must answer for risk reduction requests. You can set questionnaire for risk reduction requests. The **Compensating Control Questionnaire** is selected by default. You can also select questionnaire from the drop-down list. \(This option is not available for CC Exception Management\).|
    |Maximum Duration for exception \(days\)|Add the maximum number of days for which an exception can be requested.|
    |Questionnaire to mark false positive|Displays the questionnaire selected by you to mark as false positive. The questionnaire for false positive request is displayed by default. You can also select questionnaire from the drop-down list.|

5.  If you selected the GRC: Policy and Compliance Management option, enter the following information:

    |Field|Description|
    |-----|-----------|
    |Questionnaire to mark false positive|Displays the questionnaire selected by you to mark as false positive. The questionnaire for false positive request is displayed by default.|

6.  To configure **Conditional questionnaires** based on conditions for exception and false-positive requests:

    1.  In the Exception Management Conditional Questionnaires section, select **New**.

    2.  In the New conditional questionnaire form, fill in the fields and select **Save**.

        The created questionnaire appears in the VR Questionnaire Configuration section of the Settings for VR Exception Management form.

    For example, if you want to configure questionnaire for false-positive requests for critical vulnerable items, then select the **False positive for vulnerable items** approval rule, provide the condition as `Risk rating is 1 - Critical` and select the desired questionnaire in the Questionnaire configuration form.

7.  Select **Design New Questionnaire** to design new assessment questionnaires using the templates present in the Assessment Workspace.

8.  Select **Save**.


-   **[Request an exception using GRC: Policy and Compliance Management](sem-integration-with-grc.md)**  
Request policy exceptions using the GRC policy exception management capability in the Policy and Compliance Management application from within Vulnerability Response.
-   **[Specify the duration of an exception requested for a remediation task](sem-ex-req-sysprop.md)**  
Use system properties to limit the duration for which an exception is requested for a remediation task. Remediation of the remediation task is deferred for the specified period.

