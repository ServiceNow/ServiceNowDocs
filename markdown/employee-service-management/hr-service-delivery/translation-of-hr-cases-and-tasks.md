---
title: Translations for HR cases and tasks
description: Enable translations on HR case and task templates so that employees can view the short descriptions and descriptions of their HR cases and tasks in their preferred language.Configure an HR case or task template to enable translations. You can provide the global descriptions for translations in multiple languages so that users can view the short descriptions and descriptions of their HR cases and tasks in their preferred language.
locale: en-US
release: zurich
product: HR Service Delivery
classification: hr-service-delivery
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [HR Administration, Configure, Case and Knowledge Management, HR Service Delivery, Employee Service Management]
---

# Translations for HR cases and tasks

Enable translations on HR case and task templates so that employees can view the short descriptions and descriptions of their HR cases and tasks in their preferred language.

**Parent Topic:**[HR Administration](c_AdministerHRServiceManagement.md)

## Configure the global descriptions for translations for an HR template

Configure an HR case or task template to enable translations. You can provide the global descriptions for translations in multiple languages so that users can view the short descriptions and descriptions of their HR cases and tasks in their preferred language.

### Before you begin

Make sure to activate the languages that you want to support translations for.

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **HR Administration** &gt; **HR Services** &gt; **HR Templates**.

2.  Click **New** or open a record.

3.  Fill in the fields on the form, as appropriate.

    For details on how to how to configure an HR case or task template, see:

    -   [Configure an HR case template](../task/configure-hr-case-template.md)
    -   [Configure an HR task template](../task/configure-hr-task-template.md)
4.  To enable translations, make sure that the **Use global descriptions for translations** field is selected.

    When selected, the **Global short description** and **Global description** fields display.

5.  Provide the global short description and description for each of your activated languages.

    **Note:** Make sure to provide global descriptions for each supported language. You cannot select the **Use global descriptions for translations** option within a single HR template for some languages and not others.

    1.  Go to **System Systems** &gt; **General**, and select the language that you want to provide translations for.

        For example, you can set the language to Spanish.

    2.  On the HR template form, provide the global short description and description in the selected language.

        For example, you can provide the global short description and description for dental benefits in Spanish.

    3.  Repeat the process for each language you are supporting.

        For example, if English, Spanish, and Korean are activated on your instance, then make sure to provide global translations for each of those languages in the HR template.

6.  Click **Submit** or **Update**.

7.  If you are configuring an HR case template, then you can also update the corresponding HR service to use case headers that support the use of global descriptions.

    1.  Navigate to **HR Administration** &gt; **HR Services** &gt; **HR Service Configuration**.

    2.  Open the corresponding HR service record.

    3.  Update the following fields:

        |Field|Value|
        |-----|-----|
        |Opened for / Approver view|Opened for/approver case header configuration using global descriptions|
        |Subject person / Task assignee view|Subject person/task assigned to case header configuration using global descriptions|

    4.  Click **Update**.


### Dental benefits enrollment

This is an example of how the global short description and description displays for the Dental Benefits Enrollment/Modification HR service in the Employee Service Center when the language is set to Spanish.

