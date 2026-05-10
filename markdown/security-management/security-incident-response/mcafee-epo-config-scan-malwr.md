---
title: Configure a profile to initiate malware scan
description: After you create a profile with the Initiate Malware Scan capability and any other McAfee ePO capabilities that you want the profile to run, configure the settings of the profile so that it is invoked under the specific conditions that you define.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Configure settings, Capability profiles, McAfee ePO integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Configure a profile to initiate malware scan

After you create a profile with the Initiate Malware Scan capability and any other McAfee ePO capabilities that you want the profile to run, configure the settings of the profile so that it is invoked under the specific conditions that you define.

## Before you begin

Role required: sn\_si.admin

## About this task

As a user with the sn\_si.admin role, configure the profile so it schedules a scan only when the conditions that you specify are fulfilled on ServiceNow AI Platform Security Incident Response \(SIR\) security incidents. You define which conditions on security incidents trigger the scan. Any other McAfee ePO capabilities that you select for the profile share the triggering conditions. The options to select an alternate input field for the Configuration Item \(CI\) field and set filtering conditions are available. You may prefer to set filtering so that only those SIR security incidents that are related to your triggering event automatically invoke the profile.

As with the isolate host action, you can initiate an on-demand scan directly from a SIR security incident. For more information about launching a scan manually, see [Trigger McAfee ePO profile manually from a security incident](mcafee-epo-submit-ih-fm-si.md).

## Procedure

1.  If the Configuration page is not displayed, click **Configuration** on the progress bar.

    ![Configuration form for initiate malware scan.](../image/mcafee-initiate_malware_scan_profile.png)

    The Configuration form is displayed.

2.  Fill out the form.

<table id="choicetable_mpd_zzq_1fb"><thead><tr><th align="left" id="d353327e133">

Option

</th><th align="left" id="d353327e136">

Description

</th></tr></thead><tbody><tr><td id="d353327e142">

**Enable alternate CI trigger field**

</td><td>

Alternate configuration item \(CI\) trigger field. Default is disabled. For this example, the check box is cleared.When this check box is cleared, and the alternate CI trigger field option is disabled, an alternate for the CI field is not identified. If disabled, a value for the CI field must be populated on a SIR security incident, and the value in the field must be recognized by the McAfee ePO console before the profile runs.

 When this check box is selected, and this option is enabled, the Alternate CI trigger field choice list is displayed. Choose any field from this list as an alternate field for the CI.

 For more information about the alternate CI trigger field, see [Defining triggering conditions with a Configuration item \(CI\) field](../concept/mcafee-epo-alternate-ci.md) and [Create a capability profile](mcafee-epo-create-profile.md).

</td></tr><tr><td id="d353327e186">

**Display Tags**

</td><td>

Security tags on security incidents. Default is disabled.When this check box is cleared, and the tagging option is disabled, no security tag names are displayed on the security incident. Leave this check box cleared if you do not want security tags displayed on related security incidents.

 When the check box is selected, and the tagging option is enabled, security tag names are displayed on the configuration form. These are the tag names that are displayed on related security incidents.

 Malware scans may be scheduled during off-hours and take time to complete. On the top of the security incident, when tagging is enabled, a security tag is displayed that indicates that the scan is scheduled. After the scan is successfully completed, the scheduled tag is automatically replaced by a tag that indicates that the scan is successfully completed.

 Tag names and colors can be edited. For more information, see [Edit security tags in the ServiceNow AI Platform for the McAfee ePO integration](mcafee-epo-match-tags.md).

</td></tr><tr><td id="d353327e226">

**Auto trigger based on incident**

</td><td>

Filter conditions. Default is disabled. When the check box is cleared, and the option is disabled, the profile does not automatically launch a malware scan. The profile must be launched manually from a security incident.

 When the check box is selected, and the auto trigger option is enabled, the Filter condition builder is displayed on the form. You are required to set the filtering conditions to specify when the profile runs automatically upon incident creation.

 For this example, filters for `Category is Malicious code activity` and `Business impact is 1 - Critical` are used. For more information about the filter condition builder, see [Create a capability profile](mcafee-epo-create-profile.md).

</td></tr><tr><td id="d353327e260">

**Require Approval**

</td><td>

Require approval prior to initiating the scan. Default is disabled. When the check box is cleared, and the approval option is disabled, a user with the sn\_si.analyst role initiates a malware scan without requesting prior approval.

 Select this check box and enable this option if you want a user with the sn\_si.analyst role to request approval prior to initiating a malware scan.

</td></tr></tbody>
</table>    For this example, the approval and tagging options are enabled for the profile. For more information about how to configure the Enable alternate CI trigger field and the Auto trigger based on incident options, see [Configure profiles and security incidents for system enrichment queries](mcafee-epo-configure-profile.md).

3.  Choose one option to continue.

    |Option|Description|
    |------|-----------|
    |**Previous**|Return to the Name step if you want to edit the profile.|
    |**Save**|Save your changes and remain on this page. To save your changes, in the gray banner at the top of the screen, right-click. In the menu that is displayed, click **Save**.|
    |**Continue or select Test Incident in the progress bar**|Proceed to the Test Incident and Preview step. If you leave the page without first saving your changes, your edits are not saved.|
    |**Delete**|Delete this profile from the McAfee ePO Capability Profiles list.|

    You have successfully configured the profile so a malware scan is triggered automatically upon incident creation. An alternate CI field is used to populate matching CI results from the scan. The next step is to and preview and test security incidents for this profile.


**Parent Topic:**[Configure settings](../concept/mcafee-epo-configuring-profile.md)

