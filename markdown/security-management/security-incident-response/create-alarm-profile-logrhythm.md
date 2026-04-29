---
title: Creating an alarm profile for LogRhythm
description: In an alarm profile that you create and name, you specify which alarms you want to pull from the LogRhythm Client Console. You also define how they are mapped to fields on a ServiceNow AI Platform security incident.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [LogRhythm Overview, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Creating an alarm profile for LogRhythm

In an alarm profile that you create and name, you specify which alarms you want to pull from the LogRhythm Client Console. You also define how they are mapped to fields on a ServiceNow AI Platform security incident.

## Before you begin

Role required: sn\_si.admin

## About this task

Based on the Alarm Profile configured, one alarm profile can ingest all types of alarms out of the box, but you can use filter criteria to ingest specific types of alarms. Using this ServiceNow AI Platform integration, all configured alarm rules or specific ones based on the profile created are ingested. Alarm rules such as only high-risk level alarms can then be filtered to specify which alarms should create security incidents. Before security incidents are created, individual field values on the filtered alarms are mapped to corresponding fields on the ServiceNow AI Platform security incident. This configuration is done via an alarm profile within your ServiceNow AI Platform instance.

## Procedure

1.  Navigate to **All** &gt; **LogRhythm Integration**.

2.  Select the **LogRhythm Alarm Profiles** module to display the **Alarm Profiles** list.

    ![Create an alarm profile](../image/logrhythm-alarm-profile.gif "Alarm Profile")

3.  To create a new alarm profile, click **New**.

    A new alarm profile form is displayed. At the top of the page in the progress bar, **Name** is selected. This bar tracks your progress during the configuration.

4.  On the form, fill the fields.

<table id="table_zg3_n1r_2tb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name for the alarm profile. This name helps you identify the alarm types such as Unauthorized access \(VPN\), malware, or phishing.

</td></tr><tr><td>

Short description

</td><td>

Short text for additional information about the alarm profile, which may include the type of alarms, or an alarm category. An example description: All alarms associated with unauthorized Powershell and Sudo access attempts.

</td></tr><tr><td>

Source

</td><td>

Source server from the choice list. The list consists of LogRhythm configurations you have already set up, for example, `logrhythm-server-a`. See [Install the plugin and configure LogRhythm](install-and-config-logrhythm.md).

</td></tr><tr><td>

Order

</td><td>

Alarm profile priority. This field indicates the order in which the alarm profiles are executed when two or more alarm profiles share the triggering conditions.

</td></tr><tr><td>

Active

</td><td>

By default this option is not selected. After you complete all alarm profile setup steps and click **Finish**, you are prompted to select this check box to activate the alarm profile. When the alarm profile is active, it pulls alarms from the LogRhythm Client Console automatically.

</td></tr></tbody>
</table>5.  Click **Continue** to save your data and proceed to the Mapping form.

    If the validation is successful, the page reloads and the **Mapping** form is displayed. You cannot proceed with the configuration until you have successfully validated your connection and credentials.


-   **[Mapping](../concept/mapping-logrhythm.md)**  
After selecting the LogRhythm source that you want to ingest, you need to map individual LogRhythm alarm fields to the ServiceNow AI Platform security incident fields.
-   **[Filter alarms for LogRhythm](filter-alarms-logrhythm.md)**  
Setting filtering criteria for alarms after you have mapped fields helps you determine which alarms should be ingested into the SIR application. Filtering alarms helps you significantly reduce the number of alarms you ingest when the alarm profile is activated.
-   **[Previewing the security incident with mapped LogRhythm alarm values](../concept/preview-si-logrhythm.md)**  
After you have completed the mapping step, preview the values that you mapped to the fields on the security incident. This preview step permits you to verify that you have mapped all the critical LogRhythm alarm fields you want displayed on the security incident.
-   **[Schedule and retrieve LogRhythm alarms](schedule-and-alarm-retrieval-logrhythm.md)**  
After you preview the security incident with the LogRhythm alarms that you have selected and mapped, you are ready to schedule alarm retrieval. After you complete this step, the alarm profile is ready to be activated.
-   **[Additional options for LogRhythm alarms](verify-alarm-closure-logrhythm.md)**  
The LogRhythm Enterprise integration provides you the ability to automatically update or close the LogRhythm alarms based on the security incidents.

**Parent Topic:**[LogRhythm Overview](../concept/ovrview-logrhythm.md)

**Previous topic:**[Install the plugin and configure LogRhythm](install-and-config-logrhythm.md)

**Next topic:**[Mapping](../concept/mapping-logrhythm.md)

**Related topics**  


[Mapping](../concept/mapping-logrhythm.md)

