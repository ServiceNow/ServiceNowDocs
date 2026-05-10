---
title: Configure translated values for decorative slider
description: Add translated values to your decorative slider.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure a decorative slider, Number render types and compatible input attributes, Input form screen attributes for inputs, Configure inputs, Configure an input form screen, Input form screen, Mobile screen types, Mobile screens, Mobile app components, Building mobile apps, Mobile Platform]
---

# Configure translated values for decorative slider

Add translated values to your decorative slider.

## Before you begin

Role required: admin

You first need to create a decorative slider before you can add translated values. For more information, see [Configure a decorative slider](decorative-slider.md).

Access your decorative slider record from your input form screen and keep a record of all the Label values contained within the JSON script. These are the name values that you will be identifying for translation.

## Procedure

1.  Navigate to the Input record in the navigation tree within Mobile App Builder, which contains the decorative slider input attribute for translating.

    **Note:** For instructions on creating a decorative slider, see [Configure a decorative slider](decorative-slider.md).

2.  Select **New** from the Inputs attribute area.

3.  Enable the **Translated value attribute** field.

4.  Enter the `Label` name for each of your entries in your JSON script.

    In the JSON example provided, the Label names are: `Critically low`, `Low`, `Medium`, and `High`.

    **Note:** The **Translated value** field is automatically populated with the value entered in the **Name** field.

5.  Select **Save**.

6.  Repeat steps 4 and 5 for each Label name you have in your JSON script.

7.  Select **Save**.

8.  Select the more menu option \(![Mobile App Builder option menu.](../image/mab-option-menu.png)\) and select **Open in platform**.

9.  Navigate to **All** &gt; **sys\_translated.list**.

    The Translated Name / Field table displays.

10. Select **New** in the Inputs attribute table, and then complete the table as follows.

    1.  In the **Label \(translate\)** field, enter the translated word that corresponds to the word in the **Value** field. For example, for an Italian translation, the **Value** field may contain the word **high**, the **Label \(translate\)** field would contain the word **alto**.
    2.  In the Language field, enter the abbreviation for translated language you want the word to appear. For example, **it** for Italian or **es** for Spanish. For more information on abbreviations for languages, see [Languages table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/system-localization/r_LanguagesTable.md).
    3.  In the **Element** field, enter the text `translated_value`.
    4.  In the **Value** field, enter the word that needs translating.

        **Note:** The word in the **Value** field must correspond to the words defined in **Label** value within the JSON script.

    5.  In the **Table** field, enter the following `Input Attribute [sys_sg_input_attribute]`.
    6.  Leave the **ID** field empty.
    7.  Select **Submit**.
    8.  Repeat all the steps in step 10, for each Label value defined in the JSON. You will also need to create a new record in the Translated Name/Field table for each Label value that requires translation into an alternative language.

