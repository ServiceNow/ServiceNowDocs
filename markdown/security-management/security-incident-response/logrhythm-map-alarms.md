---
title: Map LogRhythm alarm fields to security incident fields
description: You map individual alarm fields to the security incident fields. The preconfigured mapping can be edited, and color coding provided for the fields helps you monitor alarms you have already mapped. This step helps you visualize how your edits impact the fields on the security incident.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Mapping, Create an alarm profile, LogRhythm Overview, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Map LogRhythm alarm fields to security incident fields

You map individual alarm fields to the security incident fields. The preconfigured mapping can be edited, and color coding provided for the fields helps you monitor alarms you have already mapped. This step helps you visualize how your edits impact the fields on the security incident.

## Before you begin

Role required: sn\_si.admin

If you are unfamiliar with the LogRhythm alarms, navigate to the LogRhythm Client Console and review a few sample Alarm IDs. For the following example, LogRhythm alarms `9468` and `9474` were used to map the alarms to the security incident.

## About this task

Using this form, you map the LogRhythm alarm rules on the left to the security incident fields on the right.

The following figure shows the default mapping of alarms that is preconfigured for each alarm profile. This default mapping can be edited, and with this form, you customize the fields that populate the security incident. After you complete this mapping, you can see how adding or removing alarm fields potentially impacts the field values on the security incident.

On the left side of this form in the following figure, the LogRhythm alarm rules are outlined. The values of these alarm rules are mapped to the security incident fields on the right side of the form.

## Procedure

1.  After creating an alarm profile for LogRhythm, click **Mapping** on the progress bar.

2.  In the **Alarm Sample Ingestion** field, enter up to five sample LogRhythm Alarm IDs separated by commas \(`9468,9474`\).

    ![Task: Enter alarms to pull for an alarm profile.](../image/profilemapping01__pull_alarms_entered_but_not_submitted.png)

3.  Next to the alarm field, click **Pull Alarms**.

    The pull for sample alarms may take a few moments. A message indicating that the transaction is working is displayed at the top of the screen.

    After the sample Alarm IDs are submitted and successfully pulled from the LogRhythm server, the alarm fields and their corresponding values are displayed in tabs.

    **Note:** After an alarm ID is successfully pulled, the ServiceNow AI Platform may return the following message: `The following new fields will be available for filtering shortly. Please reload this profile in a few minutes if filtering based on these fields is required. itemspacketsin, itemspacketsout`.

    This message occurs when the single alarm that has been pulled contains field names not previously processed by the ServiceNow AI Platform. These fields are available for mapping, however, if this message is displayed, reload the form so that these fields are displayed and available in the filter choice lists of the conditions builder when you are ready to set filtering conditions.

    Ingesting these sample alarms in the alarm profile configuration helps you prevent mapping alarm fields to the security incident that contain no values. It also aligns alarm fields with values to the appropriate fields in the security incident. This step ensures that all critical alarm fields are mapped and that there are no missing field values on the security incident.

    To help you ensure that no alarms are overlooked or duplicated in the mapping process, alarm fields are color-coded. A light blue alarm field \(`Account`, `AlarmRuleID`, `AlarmStatus`, etc.\) indicates that a field is not yet selected for mapping to a security incident.

    A gray field \(`AlarmDate`, `AlarmID`, and `AlarmRuleName`\) indicates that a field has already been selected and has been mapped to a field on the security incident. This color coding helps you track the mapping, because in certain cases, an alarm field can be mapped to more than one field on a security incident. For instance, the `Observables` and `Work Note` fields can have more than one value.

4.  To clear the sample alarm data, click **Clear Sample Alarm Data**.

5.  To edit the default configuration on the security incident, follow these steps to add a field:

    ![Example illustrates how to search and add a field and map it.](../image/logrhythm-map-alarm.png)

    1.  On the lower right of the form, click the plus icon.

        A new field is displayed.

    2.  In the Security Incident column, select an available field from the choice list.

        In the expanded choice list, some of the fields are shaded. For example, `Category` has a gray background, which indicates it has been mapped in the security incident. Similar to the color coding for LogRhythm alarm fields, this color coding for the security incident fields ensures that values from the alarm fields are not inadvertently mapped to the same security incident field.

        In the illustration above, the alarm rule `${Alarm:classificationName}$` is already mapped to the `Category` field in the security incident in this profile.

        **Note:** The Observable field can be mapped to more than field on the same security incident so that multiple observables can be displayed. Similarly, the `Configuration Item` and `Work notes` fields can be mapped to display multiple values.

        On the Alarm Sample Ingestion side of the form, blue indicates that an alarm rule field has not been mapped. Gray indicates that it has been mapped. In the choice list on the SIR Incident Field Mapping side of the form, white indicates that a field has not been mapped. Gray indicates that a field has been mapped. Use this color coding to help you track your field mapping.

        In the above illustration, `Affected user` has been selected from the choice list as a new field on the security incident.

    3.  From the Alarm Sample Ingestion section on the left side of the form, left-click to select the Alarm ID you want in the Input Expression field.

        In the above illustration, `Login` has been selected.

    4.  Drag it to the cleared field and release it.

        In the left column in the SIR Incident Field Mapping section, the new value for the `Affected User` field is displayed. In this case, the `Login` value from the LogRhythm alarm is displayed in the `Affected user` field on the security incident.

6.  Alternatively, to manually enter a value for fields in the Input Expression column, place your cursor in the input expression field, and enter a desired alarm value.

    For example, in the above illustration another field has been added \(`Assignment group`\) to the security incident form, and `Security Incident Assignment` has been entered manually in the field.

7.  Continue editing the preconfigured mapping as required.

    If you need to translate values from LogRhythm alarm fields to values that are supported by the fields on the security incident, you can use the script editor. See [Use the script editor to format LogRhythm values](add-scripted-values-logrhythm.md).


## What to do next

After you complete the field mapping, the next step is to [Filter alarms for LogRhythm](filter-alarms-logrhythm.md).

**Parent Topic:**[Mapping](../concept/mapping-logrhythm.md)

