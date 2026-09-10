---
title: Translate external-facing Personal Data Rights form labels and values
description: Add translation values for the configurable fields on the external-facing Personal Data Rights \(PDR\) form, so that text specific to your organization is correctly translated.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/privacy-workspace/translate-pdr-form-text.html
release: australia
product: Privacy Workspace
classification: privacy-workspace
topic_type: task
last_updated: "2026-08-29"
reading_time_minutes: 2
keywords: [PDR form translation, translated text, localization]
breadcrumb: [Configure the external-facing PDR form, Configure, Personal Data Rights \(PDR\), Privacy Management, Governance, Risk, and Compliance]
---

# Translate external-facing Personal Data Rights form labels and values

Add translation values for the configurable fields on the external-facing Personal Data Rights \(PDR\) form, so that text specific to your organization is correctly translated.

## Before you begin

Install the language plugins for the languages you want to support. For a list of available plugins and steps to activate one, see [Activate a language](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/t_ActivateALanguage.md).

Verify that an active external form configuration record exists. For steps, see [Create a PDR external-facing form configuration record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/privacy-workspace/config-pdr-ext-form-record.md).

Role required: sn\_grc\_pdr.pdr\_admin

## About this task

The external-facing PDR form supports multiple languages. Most static field labels such as **Description** or **Request submitted by**, are hardcoded strings that are translated automatically when the corresponding language plugin is installed.

However, content that you enter manually on the external form configuration record is specific to your organization, so the system doesn't translate it automatically. These include the form title, sub-title, introduction, and guidance text that appear at different stages of the form. To provide your own translations for a field, you must create a new record in the Translated Text \[sys\_translated\_text\] table and add the translated text for these fields.

## Procedure

1.  Navigate to **All** &gt; **System Localization** &gt; **Translated Text**.

2.  To add a new translation, select **New**.

3.  On the form, fill in the fields.

<table><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**Table Name**

</td><td>

Configuration table that hosts the field you want to translate.**Note:** The options in **Field Name** depend on the table you select. For example, if you want to translate the title, sub-title, or guidance text in the form, select **PDR external facing form configuration**. If you want to translate the introductory text for a jurisdiction, select **PDR external facing form location config**.

</td></tr><tr><td>

**Document**

</td><td>

Parent external form configuration record that is currently active in your instance.

</td></tr><tr><td>

**Field Name**

</td><td>

Field whose text you want translated in the external-facing form.Create separate translation records for each field you want to translate.

</td></tr><tr><td>

**Language**

</td><td>

Language that the field value is translated into.If you want the same field translated to other languages, you must create separate translation records for each language.

</td></tr><tr><td>

**Value**

</td><td>

Translated text that appears on the external form for the selected field.

</td></tr></tbody>
</table>4.  Select **Submit**.


## Result

When a requester selects the translated language on the external-facing PDR form, the form displays the translated value.

**Parent Topic:**[External-facing Personal Data Rights form configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/privacy-workspace/configure-pdr-ext-form.md)

**Related topics**  


[Translating individual UI strings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/c_TranslateIndFieldLabelsAndValues.md)

[Translated text table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/r_TranslatedText.md)

