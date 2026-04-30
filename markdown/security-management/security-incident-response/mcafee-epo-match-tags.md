---
title: Edit security tags in the ServiceNow AI Platform for the McAfee ePO integration
description: As part of the setup for the integration, edit the security tag names that you created in your McAfee ePO console in your ServiceNow AI Platform instance. Edit the tag names in your ServiceNow AI Platform instance so that they match the names of the tags in your McAfee ePO console.
locale: en-US
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [McAfee ePO integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Edit security tags in the ServiceNow AI Platform for the McAfee ePO integration

As part of the setup for the integration, edit the security tag names that you created in your McAfee ePO console in your ServiceNow AI Platform instance. Edit the tag names in your ServiceNow AI Platform instance so that they match the names of the tags in your McAfee ePO console.

## Before you begin

Role required: ServiceNow AI Platform security incident administrator \(sn\_si.admin\)

## About this task

The security tag names in your McAfee ePO console for the initiate malware scan and isolate host actions must match the security tag names in the records for these capabilities of your ServiceNow AI Platform instance.

Before you create a capability profile to run your capabilities, view the list of available McAfee ePO capabilities and edit the security tags in your ServiceNow AI Platform instance so that they match the security tag names in your McAfee ePO console.

For more information about creating the security tag names in your McAfee ePO console, see [Set up your McAfee ePO console to integrate with Security Incident Response \(SIR\)](mcafee-epo-setup-mcafee.md).

## Procedure

1.  Navigate to **All** &gt; **McAfee ePO Integration** &gt; **Default Settings**.

2.  To edit the security tag name of the McAfee ePO integration, click **Default Configuration**.

    **Note:** Makes sure you perform this configuration after you install the McAfee ePO integration.

3.  In the Initiate Malware Scan Tag Name field, enter the name of the security tag that you created in your McAfee ePO console for the initiate scan action.

    For example, ServiceNow - Malware Scan

4.  In the Isolate Host Tag Name field, enter the name of the security tag that you created in your McAfee ePO console for the isolate host action.

    For example, ServiceNow - Isolate Host

5.  If you want to do not wish to use the CI trigger field upon incident creation, select the **Define Alternate field** check box.

    When this option is enabled, the Alternate CI trigger field choice list is displayed.

    ![Edit security tags in the ServiceNow AI Platform for the McAfee integration](../image/mcafee-default-config.png "Edit security tags")

6.  Choose an alternate field from the choice list to check for your CI search criteria.

    For this example, as a user with the sn\_si.admin role, you believe that the CI field will not be populated on the security incident upon incident creation. Alternatively, you think CI information for a FQDN, host name, or IP address will be populated in the `Identified CI` field on the security incident, and you select the Identified CI field as an alternate. The Identified CI is selected for this example, but you can use any field on the security incident for the alternate CI.

7.  In the Domain field, select a domain or group for this configuration using the search option.

    For example, global.

8.  In the Require Approval field, select the **Require Approval** check box if you are using Isolate Host and Remove isolation capabilities.

    **Note:** The Initiate Malware Scan, List Threat Events, and Get System Details capabilities do not need approval.

9.  Click **Update**.

    The EPO Tag Name is updated and displayed on the McAfee ePO Default Configurations list. The security tag name for the malware scan action in your ServiceNow AI Platform instance matches the name for the scan in your McAfee ePO console.

    You have successfully edited the EPO Tag Names for the malware scan and the isolate host capabilities in your ServiceNow AI Platform instance. The next step is to create a profile for your capabilities.


**Parent Topic:**[McAfee ePO integration](../concept/mcaffee-epo-overview-arch.md)

**Previous topic:**[Install the application and configure a server for the McAfee ePO integration](mcaffe-epo-install.md)

**Next topic:**[Create an approval group](create-approval-group-mcafee.md)

**Related topics**  


[McAfee Product Documentation](https://docs.mcafee.com/bundle?value=225)

