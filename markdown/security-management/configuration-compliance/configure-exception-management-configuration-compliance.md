---
title: Configure Exception Management for Configuration Compliance
description: Limit the duration of an exception requested and add a questionnaire to the exception using the Configuration Compliance module. By default, an exception is requested using the ServiceNow Vulnerability Response module. You can also request an exception using the GRC: Policy and Compliance Management integration.
locale: en-US
release: australia
product: Configuration Compliance
classification: configuration-compliance
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Configuration Compliance, Unified Security Exposure Management, Security Operations]
---

# Configure Exception Management for Configuration Compliance

Limit the duration of an exception requested and add a questionnaire to the exception using the Configuration Compliance module. By default, an exception is requested using the ServiceNow® Vulnerability Response module. You can also request an exception using the GRC: Policy and Compliance Management integration.

## Before you begin

Role required: sn\_vulc.admin

## About this task

If Vulnerability Response is enabled, you can limit the duration for which an exception can be requested. Similarly, if the GRC: Policy and Compliance Management module is installed, you can select GRC: Policy and Compliance Management on the configuration screen. Enabling this option lets you request an exception that specifies the Policy and Control objective from GRC.

If you add a questionnaire, it’s sent to the person raising the exception or the false positive request. You can either use the default questionnaire or create one based on your requirements.

It’s useful for the exception approver to understand the reason for requesting the exception.

## Procedure

1.  Navigate to **All** &gt; **Configuration Compliance** &gt; **Administration** &gt; **Exception Management**.

2.  On the Exception Management Configuration form, select how you want to manage an exception by selecting an option from the Manage exceptions using list.

    -   Vulnerability Response

        **Note:** Starting from 22.0 of Vulnerability Response, you can set up questionnaire for false positive requests for the Vulnerability Response option also.

    -   GRC: Policy and Compliance Management

        **Note:** You must activate the GRC plugin to use GRC: Policy and Compliance Management to request an exception.

    **Note:** Changing the configuration doesn’t impact the existing data.

3.  Fill the fields on the form.

    |Field|Description|
    |-----|-----------|
    |Duration|Period for which an exception can be requested.|
    |Unit|Unit of time for the specified period.|
    |Enable questionnaire to request exception|Option to add a questionnaire to the exception request being raised.|
    |Questionnaire to request exception|Option to display the questionnaire selected by you to request an exception. The Exception Questionnaire is displayed by default.|
    |Enable questionnaire to mark false positive|Option to add a questionnaire to the false positive request being raised.|
    |Questionnaire to mark false positive|Option to display the questionnaire selected by you to mark as a false positive. The questionnaire for a false positive request is displayed by default.|

4.  Select **Save**.


