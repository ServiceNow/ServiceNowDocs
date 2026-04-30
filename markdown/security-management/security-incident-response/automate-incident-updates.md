---
title: Automate the incident updates and closures by the SIR incident status
description: Automate the incident updates and closures by the SIR incident status. The Microsoft Azure Sentinel integration has a bi-directional interface that enables both incidents to create security incidents and to update the incidents after the security incident is created or closed.
locale: en-US
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Microsoft Azure Sentinel integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Automate the incident updates and closures by the SIR incident status

Automate the incident updates and closures by the SIR incident status. The Microsoft Azure Sentinel integration has a bi-directional interface that enables both incidents to create security incidents and to update the incidents after the security incident is created or closed.

## Before you begin

**Important:**

Microsoft has extended the deprecation of the Azure Sentinel experience in the Azure portal from March 2026 to March 2027.

If you are currently using the Azure Sentinel integration with Security Incident Response \(SIR\), we strongly recommend migrating to the new Defender portal integration as soon as possible. The Defender integration includes a built-in migration utility that automatically converts your existing Sentinel profiles into Defender profiles, while ensuring continuity of incidents created through Sentinel after the transition. For more information, see [Microsoft Sentinel to Defender Migration Guide](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2795226).

Role required: sn\_si.ingestion\_profile\_admin

**Note:** Users with the sn\_si.admin role can perform all operations available to a profile admin, as the sn\_si.admin role inherits the required permissions by default.

## Procedure

1.  If you aren’t continuing from the previous section of the Scheduling process, access the profile you’re defining.

    1.  Navigate to **All** &gt; **Microsoft Azure Sentinel Integration** &gt; **Azure Sentinel Incident Profile**.

    2.  Select the profile that you’re continuing to define.

    3.  Select **Additional Options** in the progress bar.

2.  On the form, fill in the details.

    Follow the instructions to complete the configuration for updating incidents when you create or close a security incident in SIR.

<table id="table_kyc_qbg_p4b"><thead><tr><th>

Category

</th><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td rowspan="3">

Incident Creation Updates

</td><td>

Update Azure Sentinel Incidents Status upon SIR Incident creation

</td><td>

Option that enables you to use the automated incident update functionality. The Microsoft Azure Sentinel incident status is updated in Microsoft Azure incident with the comments after the SIR incident is created in the ServiceNow AI Platform.

</td></tr><tr><td>

Initial incident status update

</td><td>

Initial incident status that is updated in the Microsoft Azure Sentinel environment. You can select **New** or **Active** as the status.

</td></tr><tr><td>

Initial comments posted back to Incident

</td><td>

Initial comments that are posted to the incident in the Microsoft Azure Sentinel environment. Edit the default text that is displayed in the comments section by adding or modifying the substitution variables using the format $⁠\{field name\}$ for any field on the SIR incident form.

</td></tr><tr><td rowspan="4">

Incident Closure Updates

</td><td>

Close Azure Sentinel incidents upon SIR Incident Closure

</td><td>

Option that enables you to use the automated incident status update functionality. Microsoft Azure Sentinel incidents are closed in the Microsoft Azure incident with the comments given after the SIR incident is closed in the ServiceNow AI Platform.

</td></tr><tr><td>

Closure incident status update

</td><td>

Status update in the Microsoft Azure Sentinel incident when the incident is closed in SIR.

</td></tr><tr><td>

Closure Comments Posted back to incident

</td><td>

Comments that are posted to the incident in the Microsoft Azure Sentinel incident when the incident is closed in SIR.Edit the default text that is displayed in the comments section by adding or modifying the substitution variables using the format $⁠\{field name\}$ for any field on the SIR incident form.

</td></tr><tr><td>

Incident classification and closing reason

</td><td>

Method for the incident classification and closing reason that is used to close the incident in the Microsoft Azure Sentinel environment.Select the **Default incident classification and closing reason** method to close the incident in the Microsoft Azure Sentinel environment. When you select this method, you must define the **Default incident classification and closing reason**. When you close an incident in SIR, the incident status in Azure Sentinel is also closed with the specified **Default incident classification and closing reason**.

 Select the **Incident classification and closing reason-SIR close code mapping** method to close the incidents and to map the classification reasons with the SIR close codes. You can map multiple SIR close codes to a single classification reason. After you close an incident in SIR using the close code, the incident status in Azure Sentinel is also closed with the mapped incident classification and closing reason.

 If the classification reason and SIR close codes are not mapped, or a match is not found, then the incident is closed using the default classification reason as 'Undetermined' in the Microsoft Azure Sentinel environment.

</td></tr><tr><td rowspan="2">

Azure Sentinel Incident Comments and SIR Work notes synchronization

</td><td>

Update SIR work notes with Azure Sentinel incident comments

</td><td>

Option that you can select to update your Microsoft Azure Sentinel comments in the SIR work notes. The comment in the SIR work notes appears with the prefix `Comment from Sentinel`. The comment also contains the Sentinel ID, Analyst details, and the Time stamp.

</td></tr><tr><td>

Update Azure Sentinel incident comments with SIR work notes

</td><td>

Option that you can select to update your SIR work notes in the Microsoft Azure Sentinel incident comments. The comment in Microsoft Azure Sentinel appears with the prefix `Comment from ServiceNow`.

</td></tr></tbody>
</table>    The following example shows the configuration options that are available for automating incident updates.

    ![Options for automating incidents.](../image/sentinel-automating-incidents.png)

3.  Click **Finish**.


## What to do next

The profile moves to the Waiting state. When the confirmation message shows that the setup and configuration is complete, you can activate the profile.

