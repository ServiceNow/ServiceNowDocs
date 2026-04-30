---
title: Trigger McAfee ePO profile manually from a security incident
description: Trigger a capability profile manually from a ServiceNow AI Platform Security Incident Response \(SIR\) security incident.
locale: en-US
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [McAfee ePO integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Trigger McAfee ePO profile manually from a security incident

Trigger a capability profile manually from a ServiceNow AI Platform Security Incident Response \(SIR\) security incident.

## Before you begin

Role required: sn\_si.admin

**Note:** The approvals option in the [Configure settings](../concept/mcafee-epo-configuring-profile.md) appears only for Isolate Host and Remove Host Isolation capabilities.

## About this task

You can invoke a request to Get Host Details, Isolate Host machine, or Remove Isolation of a machine automatically if the triggering conditions you specify in the profile match the conditions on security incidents. Alternatively, if you want to submit a request manually, submit the request directly from a security incident.

Once you activate the profile, based on the configured trigger conditions, you can view the query results in the ServiceNow AI Platform security incidents. McAfee ePO integrations also enables you to run individual capabilities on Configuration Items \(CIs\) without using a profile.

## Procedure

1.  Navigate to **All** &gt; **Security Incidents** &gt; **Show All Incidents**.

2.  Select the security incident that you want to review with the McAfee ePO information.

3.  In the related lists section, select **Run EDR Profile\(s\)**.

    ![Trigger a profile manually from a security incident](../image/mcafee-edr-profile.png "McAfee Run EDR Profile")

4.  Browse and select a profile from the list of available profiles.

    The list of available profiles are Get Host Details, Isolate Host machine, and Remove Isolation. For example, let's select Get Host Details.

5.  Select **Include Related CI** to run this profile on all the related CIs of the profile.

    For example, if there are five CIs associated with the security incident, then the selected profile runs on all the five CIs.

6.  Click **Submit**.

    The selected profile is triggered manually. You can review the work notes and activities section and the profile-initiated and profile-completed tags in the work notes section.

    ![Work notes logging when capability tasks are initiated and successfully completed](../image/mcafee-edr-worknotes.png "Work notes for automation activity")

    The results appear in the form of related lists such as Get Host Details, Isolate Host machine, or Remove Isolation.

    **Note:** All the related list tables extend the base tables. In this example, the McAfee EPO System Details is an extended table of the Host Details base table.

    ![Review the related list for additional details.](../image/mcafee-test-relatedlist.png "McAfee Related lists")

7.  To run individual capabilities on a Configuration Item \(CI\), perform the following steps:

    1.  In the Configuration Items related list, select the required CI.

    2.  Click the **Actions on selected rows...** drop-down list, and select the required capability that you want to run for the selected CI.

        For example, Isolate Host.

    3.  Click **Isolate Host** to run it on the selected CI.

        The select CI gets isolated from the network.


**Parent Topic:**[McAfee ePO integration](../concept/mcaffee-epo-overview-arch.md)

**Previous topic:**[Configure a profile to initiate malware scan](mcafee-epo-config-scan-malwr.md)

**Next topic:**[Trigger additional actions in McAfee ePO integration](configure-additional-actions-mcafee.md)

