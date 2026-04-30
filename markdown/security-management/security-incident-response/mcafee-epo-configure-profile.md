---
title: Configure profiles and security incidents for system enrichment queries
description: Configure your profile settings so that the profile triggers only under the conditions that you set.
locale: en-US
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Configure settings, Capability profiles, McAfee ePO integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Configure profiles and security incidents for system enrichment queries

Configure your profile settings so that the profile triggers only under the conditions that you set.

## Before you begin

Role required: ServiceNow AI Platform® security incident administrator \(sn\_si.admin\)

## About this task

Define the conditions that automatically trigger the McAfee ePO capabilities that you selected for the profile. You can also select an alternate input field for the Configuration Item \(CI\) field. In this alternate field, you can set filtering conditions so that only those security incidents that are related to your triggering event automatically trigger the profile.

## Procedure

1.  If the Configuration page is not displayed, click **Configuration** on the progress bar.

2.  On the form, fill the fields

<table id="choicetable_pn4_pqb_cgb"><thead><tr><th align="left" id="d185276e84">

Option

</th><th align="left" id="d185276e87">

Description

</th></tr></thead><tbody><tr><td id="d185276e93">

**Enable alternate CI trigger field**

</td><td>

Alternate configuration item \(CI\) trigger field. Default is cleared. When this check box is cleared, and the alternate CI trigger field option is disabled, an alternate for the CI field is not identified. If disabled, a value for the CI field must be populated on a SIR security incident, and the value in the field must be recognized by the McAfee ePO console before the profile gathers enrichment data.

Select this check box if you believe the CI field will not be populated upon incident creation, but CI information will be populated in another field on the security incident. When this option is enabled, the Alternate CI trigger field choice list is displayed. Choose an alternate field from the choice list to check for your CI search criteria.

For more information on the alternate CI trigger field, see [Defining triggering conditions with a Configuration item \(CI\) field](../concept/mcafee-epo-alternate-ci.md).

</td></tr><tr><td id="d185276e125">

**Display Tags**

</td><td>

Security tags are displayed on security incidents. Default is cleared.When this check box is cleared, and the tagging option is disabled, no security tag names are displayed on the configuration form, and tags are not displayed on related security incidents. For this example, the security tags option is disabled.

</td></tr><tr><td id="d185276e137">

**Auto trigger based on incident**

</td><td>

Filter conditions. Default is cleared. When the check box is cleared, and the option is disabled, the profile must be invoked manually from a security incident.

When this option is enabled, the Filter condition builder is displayed. You are required to set the filtering conditions to specify when the profile runs automatically upon incident creation.

A common example of a filter for a profile that runs enrichment queries is `Category is Malicious code activity` and `Business impact is 1-Critical`. These filter conditions help you locate the incidents that are related to specific types of security events, and they help you limit the number of security incidents you have to review.

These filter settings remain saved until you change them, and they are available for editing during the preview and test incident step of the configuration.

</td></tr><tr><td id="d185276e159">

**Require approval**

</td><td>

Request approval option. Default is cleared.This approval option is available for any profile. Usually, approvals are used for capabilities that invoke actions such as host isolation and malware scans.

When the check box is cleared, and this option is disabled, no approval requests are submitted. For this example, no prior permission is required for system enrichment queries.

</td></tr></tbody>
</table>    ![Configure McAfee capability profile](../image/mcafee-epo-profile-config.png)

3.  To enable the alternate CI field option and set the filtering conditions that automatically invoke this profile, follow these steps.

    1.  Select the **Enable alternate CI trigger field** check box.

        The Alternate CI trigger field is displayed. For this example, as a user with the sn\_si.admin role, you believe that the CI field will not be populated on the security incident upon incident creation. Alternatively, you think CI information for a FQDN, host name, or IP address will be populated in the `Identified CI` field on the security incident, and you select the Identified CI field as an alternate. The Identified CI is selected for this example, but you can use any field on the security incident for the alternate CI.

    2.  From the **Alternate CI trigger** field choice list that is displayed, select the **Identified CI** field.

        All the available fields on the security incident are displayed in the list including any custom fields. In the Alternate CI trigger field, `Identified CI` is displayed.

        When this profile is invoked, and the CI field is not populated on the associated security incident upon the initial event trigger, the profile alternatively uses the value from the Identified CI field in the search.

    3.  Select the **Auto trigger based on incident** check box.

        The filter conditions builder is displayed. With this option, set filtering conditions and specify when the profile is invoked automatically upon creation of a security incident.

    4.  Define the SIR incident conditions that will automatically trigger the ePO capabilities selected for this particular profile.

    5.  If the profile capabilities that execute an action on an endpoint require approval, select the **Require Approval** check box.

    6.  Select an approve using the search icon.

4.  Click **Finish**.

    You have successfully configured the profile so it is triggered automatically upon incident creation, and an alternate field is used to populate matching CI results.


**Parent Topic:**[Configure settings](../concept/mcafee-epo-configuring-profile.md)

