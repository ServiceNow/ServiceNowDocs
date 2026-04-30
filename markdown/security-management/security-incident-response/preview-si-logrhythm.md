---
title: Previewing the security incident with mapped LogRhythm alarm values
description: After you have completed the mapping step, preview the values that you mapped to the fields on the security incident. This preview step permits you to verify that you have mapped all the critical LogRhythm alarm fields you want displayed on the security incident.
locale: en-US
release: yokohama
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Create an alarm profile, LogRhythm Overview, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Previewing the security incident with mapped LogRhythm alarm values

After you have completed the mapping step, preview the values that you mapped to the fields on the security incident. This preview step permits you to verify that you have mapped all the critical LogRhythm alarm fields you want displayed on the security incident.

Role required: sn\_si.admin.

## Security incident

If the security incident preview is not displayed, click **Preview** in the progress bar.

An example of the preview for the entire ServiceNow AI Platform security incident is displayed in the two following figures. This example of the preview of the security incident is populated with the LogRhythm alarms fields mapped from sample alarm `13663`.

In the following figure, the `Configuration item`, `Affected user`, `Priority`, `Assignment Group`, and `Short description` fields of the security incident are populated.

![Upper half of the security incident in Preview.](../image/logrythm-preview.gif "Upper half of the security incident")

On the lower half of the security incident form, the `Description` field is populated. Under the Related Items section, the `Configuration item`, `Observable`, and `Work note` fields are populated with values. If multiple values for these fields are mapped, each value is displayed on the security incident, because each of these fields can accept more than one value.

## Error conditions in preview

The following warning messages may be displayed when previewing the security incident. If a sample alarm does not pass the filtering criteria, the entire security incident is not populated.

## Input value not found

If the alarm ID is included within the filtering conditions, a warning message may still be displayed if specific input values are not found for certain mapped fields. For the sake of the following example, in the preview of the record, assume that there is no value in the `Assigned to` field, although it was mapped.

For this type of message, in the Mapping record, verify that the input value is correct. In this case, the person in the `Assigned to` field in security incident is incorrect in the ServiceNow AI Platform instance. When this alarm is ingested and it creates a security incident with this condition, fields with this input value \(`Abel Tuter`\) are left blank in the security incident.

The remaining messages in blue are informational, and they indicate that these fields have no value to display in the preview. This preview permits the security incident administrator configuring the alarm profile to verify that these fields should have no value at the initial creation stage, because in certain cases, security incident fields may be populated later automatically. Other mapping errors are also displayed.

After you are satisfied with the mapping and the security incident preview, choose one to continue the configuration.

<table id="table_ctg_jrn_3tb"><thead><tr><th>

Option

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Click **Continue** or **Scheduling** in the progress bar.

</td><td>

Advance to the **Scheduling &amp; Alarm Retrieval** form. **Scheduling &amp; Alarm Retrieval** is selected on the progress bar. The next step is to schedule alarm retrieval.

</td></tr><tr><td>

Click **Previous**.

</td><td>

Return to the alarm profile and continue mapping.

</td></tr><tr><td>

Enter another alarm ID in the **Sample Alarm ID** choice list at the top of the preview form.

</td><td>

The **Sample Alarm ID** choice list is displayed for every alarm ID you have entered. You can select up to five alarms.This option permits you to preview another LogRhythm alarm ID on a security incident.

</td></tr></tbody>
</table>After you preview the security incident and are satisfied with the results, the next step is to [Schedule and retrieve LogRhythm alarms](../task/schedule-and-alarm-retrieval-logrhythm.md).

**Parent Topic:**[Creating an alarm profile for LogRhythm](../task/create-alarm-profile-logrhythm.md)

