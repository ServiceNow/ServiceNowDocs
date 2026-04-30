---
title: Use the script editor to format LogRhythm values
description: In addition to the directly mapped fields from the pulled alarm values, and the alarm values you enter manually, you can use the script editor to format field values on the security incident during the mapping step which is optional.
locale: en-US
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Additional configurations, LogRhythm Overview, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Use the script editor to format LogRhythm values

In addition to the directly mapped fields from the pulled alarm values, and the alarm values you enter manually, you can use the script editor to format field values on the security incident during the mapping step which is optional.

## Before you begin

Role required: sn\_si.admin

The script editor changes the values of a LogRhythm alarm so the values that are mapped to the `Priority` and `Category` fields on the security incident are supported.

## About this task

In certain cases, if LogRhythm alarm values are mapped to the `Priority` and `Category` fields on the security incident, you may want to edit the mapped values. If you want to translate the value of a LogRhythm alarm to a value that is supported by the `Priority` or `Category` fields on the security incident, use the script editor.

## Procedure

1.  With the mapping form displayed, in the SIR Incident Field Mapping section, click the bracket icon `[{}]` to open the script editor.

    ![Bracket icon used to open the script editor.](../image/logrhythm-map-alarm.png)

    The default values are included for the `Priority` and `Category` fields on the security incident. You can edit these values.

    For this example, in the open editor, verify that **Priority** is displayed in the **Destination Field** choice list, as shown in the following figure. Note that this field is the security incident priority, not the LogRhythm risk-based priority.

    ![Script editor for the Priority field.](../image/lr-script-editor.png)

    In certain instances, a script include may be appropriate for the `Priority` field. For a LogRhythm alarm, for example, a risk-based priority score is assigned a value between 0-100. However, in the ServiceNow AI Platform, the priority field on a security incident supports values between 1-5. As illustrated in the preceding figure, a script include translates the LogRhythm alarm field values to the appropriate values supported by the field on the security incident in the ServiceNow AI Platform.

    In this example for the `Priority` field, if the LogRhythm alarm value is `80` or greater, `1` is displayed in the security incident field \(`Priority`\). This value translates to a `Critical` priority in the security incident. If there is no value for the alarm, the field on the security incident is set to null.

2.  Enter any changes, and click **Update** to save your changes.

    The LogRhythm Field Translations table is displayed.

3.  Close the table to return to the Mapping form.

    The following figure shows the script editor with `Category` selected in the Destination Field choice list.

    ![Script editor for the Category field on the security incident.](../image/profiletranslationscript01__category_script.png)

4.  If you want to add a new field to the Field Translations list, follow these steps to add a new record.

    1.  With the mapping form displayed, in the SIR Incident Field Mapping section, click the **Click here** link.![Click here link to script editor highlighted.](../image/profilemapping_script_click_link.png)

        The LogRhythm Field Translation list with the `priority` and `category` destination fields are displayed.

    2.  Click New.

        ![New button highlighted on LogRhythm Field Translation list.](../image/lr_field_translation.png)

        A new record is displayed.

    3.  From the Destination Field choice list, select a destination field on the security incident that you want to display your scripted values.

        ![Choice list on new record.](../image/lr-new_script_field.png)

    4.  Click **Submit**.

        The script editor is displayed.

    5.  Enter any changes into the editor, and click **Submit** to save your changes.

        The LogRhythm Field Translations table with your new record is displayed.

5.  Close the table to return to the Mapping form.


**Parent Topic:**[Additional configurations for the LogRhythm integration](configure-system-and-troubleshooting-properties.md)

