---
title: Fulfill a localization task
description: Fulfill a localization task created for each selected language in the translation request.
locale: en-US
release: australia
product: Localization Framework
classification: localization-framework
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Create translation projects, Localization Framework, Translation and localization, Configure core features, Administer the ServiceNow AI Platform]
---

# Fulfill a localization task

Fulfill a localization task created for each selected language in the translation request.

## Before you begin

Role required: localization\_fulfiller

## Procedure

1.  Navigate to **All** &gt; **Localization Framework** &gt; **My Tasks**.

2.  Select a localization task in the Open state.

3.  On the Localization Task page, select **Translate** in the form header.

    **Note:** The **Translate** UI action is visible in all states except Awaiting Business Approval, Close Complete, and Incomplete.

    A two-column comparison UI page opens with the Source Language column on the left and the Target Language column on the right.

    Each Localization requested item has the following options:

    -   **Expand all**: Expand all the groups on the comparison UI.
    -   **Collapse all**: Collapse all the groups on the comparison UI.
    -   **Show groups with missing translations**: See only the groups that have missing translations when the content is translated.
4.  Translate the content manually or select one of the following translation modes from the task header.

<table id="table_sxs_djm_ypb"><thead><tr><th>

Translation mode

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Machine Translate

</td><td>

Translates content using the translation service provider configured in the translation preferences. If there is more than one LRITM, then the operation is asynchronous.

</td></tr><tr><td>

Send to TMS

</td><td>

Sends the artifact to the translation management system configured in translation preferences for translation. If there are more than is LRITM, then the operation is asynchronous.

</td></tr><tr><td>

Export Source File

</td><td>

Exports the source file for translation in the file format configured in the translation preferences or as per the selected file format in the comparison UI.

</td></tr><tr><td>

Import Translated File

</td><td>

Imports the translated file in the file format configured in the translation preferences from the third-party translator. A merge conflict occurs when you have certain fields pre-populated with translations, but those fields get updated when you import the translated file. These conflicts are shown right below the fields updated with the latest translations.

 ![Merge conflict when importing translations.](../image/import-file-merge-conflict.png)

 To resolve the merge conflict, do the following:

1.  Click **See versions**.
2.  Choose a version that you want to retain.
3.  Click **Save**.


</td></tr><tr><td>

Send Source File via Email

</td><td>

Sends the source file to the email addresses configured in translation preferences for translation. If there is more than one LRITM, then the operation is asynchronous.

</td></tr></tbody>
</table>    **Note:** When any translation mode is selected to translate the content, the content is saved as a draft to retain changes done by the user and then the translation process is initiated.

5.  If you want to make any changes to the verified translations, click the lock icon \(![Lock icon](../image/lock-icon.png)\) beside the field with verified translations.

    Verified translations are pre-existing translations available in the database for the given text. The framework automatically fetches the existing translations and locks the fields.

6.  Save the translated content by clicking **Save as Draft**.

    You can later revisit the content or send the content for translation approval.

    This option moves the task state to Translation in Progress.

7.  Click **Submit for Approval**.

    **Note:** This option is available only for tasks where the workflow configured for the target language needs translation approval.

    The task is sent for translation approval.

8.  Click **Publish Translations**.

    **Note:** This option is available only for tasks where the workflow configured for the target language has the **Publish** option.


## Result

The translations of the localization task are published and the task is updated with the Closed Complete state.

You can move translation records across instances by using update sets. The translation-related XML files are saved to the update set specified in the settings. For more information, see [Localization Framework Properties: Update Set Strategies](../concept/lf-update-set-strategies.md).

