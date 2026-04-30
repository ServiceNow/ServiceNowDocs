---
title: Additional options for LogRhythm alarms
description: The LogRhythm Enterprise integration provides you the ability to automatically update or close the LogRhythm alarms based on the security incidents.
locale: en-US
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Create an alarm profile, LogRhythm Overview, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Additional options for LogRhythm alarms

The LogRhythm Enterprise integration provides you the ability to automatically update or close the LogRhythm alarms based on the security incidents.

## Before you begin

Role required: sn\_si.analyst

## About this task

When you enable the Alarm initial updates option, the alarms are automatically updated in the LogRhythm comments with the initial alarm updates. Similarly, when you enable the Alarm closure updates option, the alarms are automatically closed in LogRhythm along with the SIR Closure Code and and closure comments.

The LogRhythm alarm ID is connected to the ServiceNow AI Platform security incident ID throughout the course of the incident's life cycle. This correlation permits a simultaneous and automated security incident/alarm closure to occur. When the Security Incident Response \(SIR\) security incident record is closed, there is a comment posted in the alarm on the LogRhythm web console. This comment indicates that the alarm was closed out based on the closure of the ServiceNow AI Platform security incident. The incident number and a URL that links back to the security incident for reference are also included in the comment section in the LogRhythm alarm.

## Procedure

1.  Click the **Additional Options** step on the progress bar.

2.  To use the automated alarm update for SIR Incident creation, choose from the following options to configure your alarm retrieval.

<table id="choicetable_lvr_kdr_f2b"><thead><tr><th align="left" id="d362519e99">

Option

</th><th align="left" id="d362519e102">

Description

</th></tr></thead><tbody><tr><td id="d362519e108">

**Update LogRhythm alarms upon SIR Incident Creation**

</td><td>

Default is cleared. Select this option to automatically update the LogRhythm alarms when the SIR Incident is created.

</td></tr><tr><td id="d362519e120">

**Initial comments posted back to LogRhythm alarm**

</td><td>

Indicates the initial comments that are posted for the LogRhythm alarm.

 Edit the default text that is displayed in the comments section by adding or modifying the substitution variables using the format $⁠\{field name\}$ for any field on the SIR incident form.

 For example, `The related ServiceNow security incident, ${Number}$ has been created and assigned to ${Assignment group}$. Additional details can be found on the security incident located here - ${URL}$`.

</td></tr></tbody>
</table>3.  To use the automated alarm update for SIR Incident closure, choose from the following options to configure your alarm retrieval.

<table id="choicetable_xkc_b44_3tb"><thead><tr><th align="left" id="d362519e153">

Option

</th><th align="left" id="d362519e156">

Description

</th></tr></thead><tbody><tr><td id="d362519e162">

**Close LogRhythm alarms upon SIR Incident Closure**

</td><td>

Default is cleared. Select this option to automatically close the LogRhythm alarms when the SIR Incident is closed.

</td></tr><tr><td id="d362519e174">

**Closure comments posted back to LogRhythm alarm**

</td><td>

Indicates the closure comments that are posted for the LogRhythm alarm.

 Edit the default text that is displayed in the comments section by adding or modifying the substitution variables using the format $⁠\{field name\}$ for any field on the SIR incident form.

 For example, `The related ServiceNow security incident, ${Number}$ has been closed by SOC Analyst-${Closed by}$ with the following closure notes - ${Close notes}$. Additional details can be found on the security incident located here - ${URL}$`.

</td></tr></tbody>
</table>4.  Click **Finish** to save the alarm profile.


If you do not see notes indicating the alarm has closed successfully in the security incident, review the work notes for more information about how to proceed to fix the problem. Also, check your server connection. If you confirm the ServiceNow AI Platform security incident has been closed and the server has not timed out, you may have to manually close the alarm on the LogRhythm Web Console.

**Parent Topic:**[Creating an alarm profile for LogRhythm](create-alarm-profile-logrhythm.md)

