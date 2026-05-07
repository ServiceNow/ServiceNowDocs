---
title: Filter alarms for LogRhythm
description: Setting filtering criteria for alarms after you have mapped fields helps you determine which alarms should be ingested into the SIR application. Filtering alarms helps you significantly reduce the number of alarms you ingest when the alarm profile is activated.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Create an alarm profile, LogRhythm Overview, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Filter alarms for LogRhythm

Setting filtering criteria for alarms after you have mapped fields helps you determine which alarms should be ingested into the SIR application. Filtering alarms helps you significantly reduce the number of alarms you ingest when the alarm profile is activated.

## Before you begin

Role required: sn\_si.admin

## About this task

Use the filtering conditions at the bottom of the mapping form to filter out specific alarms or limit ingestion to only alarms that meet certain field-level criteria. Filtering significantly reduces the number of alarms you ingest once the alarm profile is activated. Use filtering to ingest a manageable quantity of alarms that your Security Operations Center \(SOC\) staff can support.

**Note:** The following example shows a default filter setting in which `Alarm status-does-not-contain-Closed` is the default setting. This filter only pulls active alarms, and this setting reduces the number of pulled alarms. The following steps illustrate how to add another useful filter which includes only alarms with the highest severity or priority values.

## Procedure

1.  To edit the filtering criteria, select the **Filter based on conditions** check box.

    ![Filter based on conditions check box selected and highlighted.](../image/profilemapping06__add_filter_condition_button.png)

2.  To the right of the **Filter conditions** field, click **OR** or **AND**.

3.  In the new line that is displayed, select the filtering conditions from the choice lists.

    The following image shows an additional filter added to the criteria in which risk-based priority \(`RBP max`\) is greater than `50`. With this filter setting, only LogRhythm alarms with a risk-based priority value that is greater than 50 are pulled.

    ![Add a new filter condition to ingest alarms with a risk-based priority greater than 50.](../image/profilemapping07__added_risk_based_priority_filter.png)

4.  After you have verified that all critical LogRhythm alarm fields are mapped to the ServiceNow AI Platform security incident, and you have set filtering criteria to limit alarm ingestion, choose one to continue the configuration.

<table id="choicetable_r4p_krl_f2b"><thead><tr><th align="left" id="d93496e139">

Option

</th><th align="left" id="d93496e142">

Description

</th></tr></thead><tbody><tr><td id="d93496e148">

**Continue or Preview**

</td><td>

The Preview form of the security incident with your mapping configuration is displayed.**Preview** is selected on the progress bar. The next step is to view the security incident with your mapped alarms.

</td></tr><tr><td id="d93496e162">

**Update**

</td><td>

Save your data and return to the **Alarm Profiles** list.

</td></tr><tr><td id="d93496e174">

**Previous**

</td><td>

The alarm profile record is displayed.

</td></tr><tr><td id="d93496e183">

**Delete**

</td><td>

Delete this alarm profile and the **Alarm Profiles** list is displayed.

</td></tr></tbody>
</table>
## What to do next

The next step is to preview your mapped fields on the security incident. See [Previewing the security incident with mapped LogRhythm alarm values](../concept/preview-si-logrhythm.md).

**Parent Topic:**[Creating an alarm profile for LogRhythm](create-alarm-profile-logrhythm.md)

