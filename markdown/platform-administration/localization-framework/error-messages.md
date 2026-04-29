---
title: Error messages in the Localization Framework
description: Error messages are displayed when the appropriate settings are not configured for the translation and workflow preferences.
locale: en-US
release: australia
product: Localization Framework
classification: localization-framework
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Localization Framework reference, Localization Framework, Translation and localization, Configure core features, Administer the ServiceNow AI Platform]
---

# Error messages in the Localization Framework

Error messages are displayed when the appropriate settings are not configured for the translation and workflow preferences.

|Error message|Scenario|
|-------------|--------|
|Internal name cannot be modified for the existing record.|When someone tries to modify the internal name of the existing artifact record.|
|Either a Processor script or a Read script is required for an active artifact configuration|When there is no processor script or read script available for the artifact configuration record.|
|A configuration record exists for the table: \{table\_name\}|When you provide a table name for an artifact configuration record that exists for another artifact.|
|A configuration record exists with internal name: \{internal\_name\}|When you provide an internal name for an artifact configuration record that exists for another artifact.|

|Error message|Scenario|
|-------------|--------|
|Contains invalid Email Address\(es\): \{comma-separated email addresses\}.|When some of the email addresses fail the validation.|
|Selected Localization Fulfiller group does not have localization\_fulfiller role.|When the selected user group does not have the localization\_fulfiller role.|
|Selected Business Approver group does not have localization\_fulfiller role.|When the selected user group doesn’t have the localization\_fulfiller role.|
|Selected Translation Approver group does not have localization\_fulfiller role.|When the selected user group does not have the localization\_fulfiller role.|
|Ensure that the corresponding translation preference for your auto translation option is enabled.|When auto translate is selected in the workflow preference.|
|\{Translator\_name\} translator is not of version v3.|When the corresponding translator version is not v3.|
|\{Translator\_name\} translator has no translate subflow configured.|When the corresponding translator's translate subflow is empty.|
|Selected translator is not active.|When the corresponding translator configuration is inactive.|
|There are no languages available for the selected artifact. All the possible languages were configured in other localization setting records.|A warning message when there are no languages available for the selected artifact.|
|A setting record exists for the artifact - language pair\(s\): \{pair of artifact and language\}. Resolve the conflict\(s\) to proceed.|When a user tries to add a language or artifact in settings and that record exists in another record.|
|The Default recipient\(s\) list contains invalid email address\(es\): \{comma\_separated\_email\_adddresses\}.|When the provided email addresses of the recipients are invalid.|
|\{0\} translator is not active.|When the translator is not active.|

|Error message|Scenario|
|-------------|--------|
|Your request for translations failed. Please reinitiate the request.|When there is an error in submitting the translation request.|
|Error in requesting translations for the following artifact item and language pair\(s\): \{pair of artifact and language\}. Reinitiate the request for the listed pairs.|Error is seen only on the list view when there is an error requesting translations for certain language pair\(s\): \{pair of artifact and language\}.|

<table id="table_rtz_d35_tnb"><thead><tr><th>

Error message

</th><th>

Scenario

</th></tr><tr><th colspan="2" align="left">

**Machine Translate**

</th></tr></thead><tbody><tr><td>

Failed to machine translate using \{translator name\}. \{Reason for failure\}.**Note:** The reason is fetched from Dynamic Translation.

</td><td>

This message appears in two scenarios:-   Error message shown in the comparison UI for machine translation.
-   Message logged in the activity stream when failed to machine translate the content.

</td></tr><tr><td>

Failed to machine translate using \{translator name\}. Translations for one or more fields have failed.

</td><td>

This message appears in two scenarios: -   Error message shown in the comparison UI when translations for one or more fields fail.
-   Message logged in the activity stream when translations for one or more fields fail.

</td></tr><tr><td>

Failed to machine translate.

</td><td>

Error message shown in the comparison UI in case the call for machine translate fails.

</td></tr><tr><td>

Error while saving the draft. Contact your system administrator.

</td><td>

Error message shown in the comparison UI when content that is requested for translation, is not saved as a draft message successfully. For any translation mode selected to translate the content, the content is saved as a draft to retain changes done by user and then the translation process is initiated.

</td></tr><tr><td colspan="2" align="left">

**Send via Email**

</td></tr><tr><td>

Failed to send source file via email to: \{email addresses\}.

</td><td>

Message logged in the activity stream when sending source file via email fails.

</td></tr><tr><td>

Failed to send email.

</td><td>

This error message appears in two scenarios:-   Error message persisted and shown in the comparison UI when sending the source file via email fails.
-   Error message shown in the comparison UI in case the call for sending email fails.

</td></tr><tr><td>

Following are the invalid email addresses: \{comma separated invalid email addresses\}, please try again.

</td><td>

When one of the email addresses provided are incorrect while sending via email.

</td></tr><tr><td colspan="2" align="left">

**Send to TMS**

</td></tr><tr><td>

Error while sending the task to \{tms name\} TMS for translation. \{Reason for failure\}.

</td><td>

This error message appears in two scenarios: -   Message logged in the activity stream when sending translatable content to TMS fails.
-   Error message persisted and shown in the comparison UI when sending translatable content to TMS fails.

</td></tr><tr><td>

Failed to send to TMS.

</td><td>

Error message shown in the comparison UI in case the call for sending translatable content to TMS fails.

</td></tr><tr><td>

A record related to \{0\} exists.

</td><td>

when you try to create another TMS with the same name.

</td></tr><tr><td colspan="2">

**Retrieval from TMS**

</td></tr><tr><td>

Failed to retrieve translations from \{tms name\} TMS. \{Reason for failure\}.

</td><td>

This error appears in two scenarios:-   Message logged in the activity stream when retrieving translations from XTM TMS fails.
-   Error message persisted and shown in the comparison UI when retrieving translations from XTM TMS fails.

</td></tr><tr><td>

Failed to retrieve translations from \{tms name\} TMS.

</td><td>

Error message shown in the comparison UI in case the call for retrieving translations from XTM TMS fails.

</td></tr><tr><td colspan="2">

**Export Source File**

</td></tr><tr><td>

Failed to export the \{CSV/XLIFF\} file. \{Reason for failure\}.

</td><td>

This error message appears in two scenarios:-   Error message persisted and shown in the comparison UI when exporting the source file for translations fails.
-   Message logged in the activity stream when exporting the source file for translations fails.

</td></tr><tr><td>

Failed to export file.

</td><td>

Error message shown in the comparison UI in case the call for exporting the source file for translation fails.

</td></tr><tr><td colspan="2">

**Import Translated File**

</td></tr><tr><td>

Failed to import translations from \{CSV/XLIFF\} file. \{Reason for failure\}.

</td><td>

This message appears in two scenarios:-   Message logged in the activity stream when importing the translated file fails.
-   Error message persisted and shown in the comparison UI when importing the translated file fails.

</td></tr><tr><td>

Import failed.

</td><td>

Error message shown in the comparison UI in case the call for importing the translated file fails.

</td></tr><tr><td>

Failed to publish translations.

</td><td>

When failed to publish the translations.

</td></tr><tr><td colspan="2">

**Save as Draft**

</td></tr><tr><td>

Error while creating the draft.

</td><td>

When there is an error after clicking Save as draft.

</td></tr><tr><td colspan="2">

**Approve Translations**

</td></tr><tr><td>

Error while requesting for changes.

</td><td>

When an error occurs while an approver requests changes for the translations.

</td></tr><tr><td colspan="2">

**Publish Translations**

</td></tr><tr><td>

Error in publishing the translations.

</td><td>

When attempting to translate content that has already been translated.

</td></tr><tr><td>

Error while submitting the translations.

</td><td>

When publishing translations or when sending translations for approval.

</td></tr></tbody>
</table>|Error message|Scenario|
|-------------|--------|
|Insights generation job is already running, please try again later|When you try to generate the insights record multiple times.|
|Your request for translations failed for the selected insights. Click here to see the list of insights for failed requests and reinitiate the request.|Lists the insights records for which it failed to request translations.|
|Localization setting does not exist for the following table and language pair\(s\): \{pair of table name and language\}. Uncheck the record\(s\) of the mentioned pair\(s\) and resubmit.|Lists the language pair\(s\): \{pair of table name and language\} for which a settings record does not exist.|

**Parent Topic:**[Localization Framework reference](../concept/reference-localization-framework.md)

