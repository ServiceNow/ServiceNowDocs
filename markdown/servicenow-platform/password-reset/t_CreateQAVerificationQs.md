---
title: Add a custom question to the Security Questions verification
description: To enroll for the 'Security Questions' verification, the user selects several questions and supplies confidential answers that only the user knows. You can add a custom question to the set of questions that are included with the base system.
locale: en-US
release: australia
product: Password Reset
classification: password-reset
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Customizing Password Reset processes, Configuring Password Reset, Password Reset, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Add a custom question to the Security Questions verification

To enroll for the 'Security Questions' verification, the user selects several questions and supplies confidential answers that only the user knows. You can add a custom question to the set of questions that are included with the base system.

## Before you begin

Role required: password\_reset\_admin

## About this task

The base system provides a large set of default questions in all supported languages. Questions are presented to each user in the language that the user requested during login. Creating a custom English language question is a one-step process. To create a custom question in a non-English language, you can use either of the following options:

-   Create a custom question in the non-English language.
-   Create a custom English language question plus one or more translations of the question into other languages.

## Procedure

1.  Navigate to **All** &gt; **Password Reset** &gt; **Security Questions**.

    **Note:** Each question in the list is presented to users when they enroll for the Password Reset process. The user selects each question to use by providing a confidential answer to the question.

2.  Follow this procedure to create a custom question in a single language.

    **Note:** To enter non-English question text, you must request the language when logging in.

    1.  On the Password Reset Questions page, click **New**.

    2.  Enter the text in the **Question \(Translated field\)** field and then click **Submit**.

    The question is added to the list of questions that is presented to users when they enroll. No additional steps are needed and you can skip the remaining steps.

3.  Follow this procedure to create a custom question in English and the same question in one or more other languages:

    1.  Click **New**, enter English language text in the **Question \(Translated field\)** field, and then click **Submit**.

    2.  Create a record in the **sys\_translated** table for the non-English language question.

        Details appear at [Translated Name / Field table](https://www.servicenow.com/docs/access?context=r_TranslatedNameFieldTable&version=australia&pubname=australia-platform-administration&ft:locale=en-US) and [Languages table](https://www.servicenow.com/docs/access?context=r_LanguagesTable&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

        |Field|Description|
        |-----|-----------|
        |Label \(translate\)|Non-English equivalent of the English text in the **Value** field.|
        |Element|Name of the field in the Password Reset Question \[pwd\_question\] table: `question_translated`|
        |ID|[ISO 639.2](http://www.loc.gov/standards/iso639-2/php/code_list.php) code for the language.|
        |Table|Table that you are adding the translated question to: the **Password Reset Question \[pwd\_question\]** table.|
        |Language|Language code for this translated text.|
        |Value|English-language question that you added in the Security Questions table.|

    3.  Repeat the process for each language that users might request.


**Parent Topic:**[Customizing Password Reset processes](../concept/customizing-password-reset.md)

