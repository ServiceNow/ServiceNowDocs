---
title: Automate incident updates and closures
description: Automate incident updates and closures based on the incident status. The Microsoft Defender integration has a bi-directional interface that enables incidents to create security incidents and to update the incidents after the security incident is created or closed.
locale: en-US
release: yokohama
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-01-17"
reading_time_minutes: 2
breadcrumb: [Microsoft Defender integration for Security Operations, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Automate incident updates and closures

Automate incident updates and closures based on the incident status. The Microsoft Defender integration has a bi-directional interface that enables incidents to create security incidents and to update the incidents after the security incident is created or closed.

## Before you begin

Role required: sn\_si.admin, sn\_si.ingestion\_profile\_admin

## Procedure

1.  If you aren’t continuing from the previous section of the Scheduling process, access the profile you’re defining.

    1.  Navigate to **All** &gt; **Microsoft Defender Integration** &gt; **Defender Incident Profiles**.

    2.  Select the profile that you’re continuing to define.

    3.  Select **Additional Options** in the progress bar.

2.  On the form, fill in the fields.

<table id="table_kyc_qbg_p4b"><thead><tr><th>

Category

</th><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td rowspan="3">

Incident Creation Updates

</td><td>

Update Defender Incident status upon SIR Incident Creation

</td><td>

Option to use the automated incident update functionality. The Defender incident status is updated with the comments after the SIR incident is created in the ServiceNow AI Platform.

</td></tr><tr><td>

Initial incident status update

</td><td>

Initial incident status that is updated in the Microsoft Defender environment. Options include: Active, In Progress, and Redirected.

</td></tr><tr><td>

Initial comments posted back to Incident

</td><td>

Initial comments that are posted to the incident in the Defender environment.

</td></tr><tr><td rowspan="4">

Incident Closure Updates

</td><td>

Close Defender Incident upon SIR Incident Closure

</td><td>

Option to use the automated incident status update functionality. Incidents will be closed in Defender with the comments given after the SIR incident is closed in the ServiceNow AI Platform.

</td></tr><tr><td>

Closure Incident Status Update

</td><td>

Status update in Defender when the security incident is closed in SIR.

</td></tr><tr><td>

Closure Comments Posted back to incident

</td><td>

Comments posted to the incident in Defender when the security incident is closed in SIR.

</td></tr><tr><td>

Incident classification

</td><td>

Option to automatically update Microsoft Defender Incident Classification based on SIR Close Code.

 When a SIR is closed in ServiceNow, the selected SIR Close Code will automatically determine and update the Incident Classification field in the corresponding Microsoft Defender incident.

 Options include:

-   Default incident classification.
-   Incident classification-SIR close code mapping.


</td></tr><tr><td>

Defender Pull Closed Incidents

</td><td>

Pull Closed Incidents

</td><td>

Option to fetch closed incidents during ongoing ingestion and one-time retrieval. Closed SIR incidents won’t be updated with new data from Defender.

</td></tr><tr><td rowspan="2">

Defender Incident Comments and SIR Work notes synchronization

</td><td>

Update SIR work notes with Defender incident comments

</td><td>

Option to synchronize Security Incident work notes to Defender incident comments. Work notes added to the Security Incidents in ServiceNow appears with the prefix- Comment from Defender ID.

</td></tr><tr><td>

Update Defender incident comments with SIR work notes

</td><td>

Option to update your SIR work notes in the Defender incident comments. The comment in Microsoft Defender appears with the prefix- Comment from ServiceNow.

</td></tr></tbody>
</table>    ![Options for automating incidents](../image/ms-def-additional-op.png)

3.  Select **Finish**.

4.  Activate the profile.

    1.  Select the **Name** section of the progress bar.

    2.  Select the **Active** check box.

    3.  Select **Continue**.


