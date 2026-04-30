---
title: Create Onboarding modals
description: Create your own Onboarding modals to introduce your users to a new experience or application in your ServiceNow instance.
locale: en-US
release: zurich
product: Adoption Services
classification: adoption-services
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 5
keywords: [Create onboarding modal]
breadcrumb: [Configure, Onboarding modals, Adoption services, Configure user experiences]
---

# Create Onboarding modals

Create your own Onboarding modals to introduce your users to a new experience or application in your ServiceNow instance.

## Before you begin

Role required: admin

Ensure you have:

-   Planned your onboarding content, including the key concepts to cover and the optimal sequence for presenting information
-   Identified target user roles who should see the Onboarding modals
-   Prepared any images, videos, or custom HTML content to include in the modal
-   Determined the application or workspace where the modal will appear

## Procedure

1.  Navigate to **All** &gt; **Adoption Services** &gt; **Create Guidance**.

2.  To create your Onboarding modals, do the following:

    1.  On the guidance form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Order|Order that the guidance displays. The lowest number displays first and the next chronological number follows.|
        |Name|Name of the onboarding experience.|
        |Type|Type of guidance that appears in the UI. Select **Modal**.|
        |Roles|Roles for this guidance.|
        |Application|Application for the guidance.|
        |Status|Status of the guidance.|
        |Active|Select to enable or disable the guidance.|

    2.  Select **Submit**.

3.  To create embedded help guidance steps, do the following:

    1.  Select your guidance from the Guidances list.

    2.  On the Help Guidance Steps related list, select **New**.

    3.  On the form, fill in the fields.

<table id="table_fdb_lmn_jsb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of your guidance.

</td></tr><tr><td>

Layout

</td><td>

Selected layout of the guidance.-   Video
-   Image
-   Text
-   Question
-   Image and Text
-   Image and Question


</td></tr><tr><td>

Order

</td><td>

Order that the guidance displays. The lowest number displays first and the next chronological number follows.

</td></tr><tr><td>

Action Label

</td><td>

Button labels that enable the user to navigate the guidance modal.

</td></tr><tr><td>

Application

</td><td>

Application scope for the guidance. This guidance applies to the Global scope.

</td></tr><tr><td>

Guidance

</td><td>

The guidance that this Help Guidance Step applies to.

</td></tr></tbody>
</table>    4.  Select **Submit**.

4.  To create help contents for your help guidance steps, do the following:

    1.  Select your help guidance step in the related list.

    2.  On the Help Contents related list, select **New**.

    3.  **Note:** Form fields are different for each type of guidance. Refer to the correct form for your guidance.

        On the text form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Title|Title of the help content.|
        |Subtitle|Subtitle that's displayed in the modal of the help content in the UI.|
        |Type|Type of guidance that's selected.|
        |Application|Application scope for the guidance.|
        |Guidance Step|Help Guidance Step that this Help Content is associated with. For example, Intro/welcome, All menu, and History.|
        |Default|Help content that is the default for the guidance step.|
        |Footer|Footer that's displayed in the modal of the help content in the UI.|
        |Provide Custom HTML|Custom HTML for your help content.|
        |Text|Text that displays in the modal of the help content in the UI.|

    4.  Click **Submit**.

    5.  On the video form, fill in the fields.

<table id="table_mkw_g24_2cc1"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Title

</td><td>

Title of the help content.

</td></tr><tr><td>

Subtitle

</td><td>

Subtitle that's displayed in the modal of the help content in the UI.

</td></tr><tr><td>

Type

</td><td>

Type of guidance that's selected.

</td></tr><tr><td>

Video Link

</td><td>

The link for your video to display.**Note:** Only YouTube and Vimeo are supported.

</td></tr><tr><td>

Application

</td><td>

Application scope for the guidance.

</td></tr><tr><td>

Guidance Step

</td><td>

Help Guidance Step that this Help Content is associated with. For example, Intro/welcome, All menu, and History.

</td></tr><tr><td>

Default

</td><td>

Help content that is the default for the guidance step.

</td></tr><tr><td>

Footer

</td><td>

Footer that's displayed in the modal of the help content in the UI.

</td></tr><tr><td>

Provide Custom HTML

</td><td>

Custom HTML for your help content.

</td></tr><tr><td>

Alternate Text

</td><td>

Alternate text that displays in the modal of the help content in the UI.

</td></tr></tbody>
</table>    6.  Click **Submit**.

    7.  On the image form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Title|Title of the help content.|
        |Subtitle|Subtitle that's displayed in the modal of the help content in the UI.|
        |Type|Type of guidance that's selected.|
        |Image|The image selected to display in your guidance.|
        |Application|Application scope for the guidance.|
        |Guidance Step|Help Guidance Step that this Help Content is associated with. For example, Intro/welcome, All menu, and History.|
        |Default|Help content that is the default for the guidance step.|
        |Footer|Footer that's displayed in the modal of the help content in the UI.|
        |Provide Custom HTML|Custom HTML for your help content.|
        |Provide Image Link|The image link is displayed in the guidance.|
        |Alternate Text|Alternate text that displays in the modal of the help content in the UI.|

    8.  Click **Submit**.

    9.  On the question form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Title|Title of the help content.|
        |Subtitle|Subtitle that's displayed in the modal of the help content in the UI.|
        |Type|Type of guidance that's selected.|
        |Application|Application scope for the guidance.|
        |Guidance Step|Help Guidance Step that this Help Content is associated with. For example, Intro/welcome, All menu, and History.|
        |Default|Help content that is the default for the guidance step.|
        |Footer|Footer that's displayed in the modal of the help content in the UI.|
        |Provide Custom HTML|Custom HTML for your help content.|

    10. Select **Submit**.

    11. Select **New** in the Help Question related field.

<table id="table_rkd_yf4_2cc4"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Question

</td><td>

The content of the question to add in the guidance.

</td></tr><tr><td>

Order

</td><td>

The order of the question in the guidance.

</td></tr><tr><td>

Variant

</td><td>

The variant of the question.-   Radio is selected for questions with only one answer.
-   Checkbox is selected for questions with multiple answers.


</td></tr><tr><td>

Application

</td><td>

Application scope for the guidance.

</td></tr><tr><td>

Help Content

</td><td>

The Help Content that the question is created for.

</td></tr><tr><td>

Mandatory

</td><td>

The question is Mandatory when selected.

</td></tr></tbody>
</table>    12. Select **New** in the Help Answers related field to create answers.

        |Field|Description|
        |-----|-----------|
        |Label|The label for the answer.|
        |Value|The value for the answer.|
        |Order|The order of the answer.|
        |Application|Application scope for the guidance.|
        |Question|The question the answer is created for.|

    13. Select **Submit**.

5.  Create any additional guidance that you want to build your onboarding experience.

6.  When you're done building your onboarding guidance, confirm that the status of your guidance is set to **Published** on the Guidance form.

7.  On the Guidance form, select **Update**.


## Result

Your onboarding modal is created and published. The modal contains all configured guidance steps with their associated help content. Users with the specified roles can now see the modal when it is triggered.

## What to do next

Configure a launch trigger for your modal. See Launch an onboarding modal.

**Parent Topic:**[Configure](../concept/configure-onboarding-modals.md)

