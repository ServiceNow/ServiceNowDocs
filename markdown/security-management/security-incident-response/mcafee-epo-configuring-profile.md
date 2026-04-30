---
title: Configuring profiles for the McAfee ePO integration
description: After you create a profile and select the McAfee ePO capabilities that you want the profile to run, configure the settings so that the profile is invoked only under the specific conditions that you define.
locale: en-US
release: yokohama
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [McAfee ePO integration capability profiles, McAfee ePO integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Configuring profiles for the McAfee ePO integration

After you create a profile and select the McAfee ePO capabilities that you want the profile to run, configure the settings so that the profile is invoked only under the specific conditions that you define.

## Configuring a profile

In this step, you configure a capability profile so that it runs only when the conditions you specify are fulfilled. You define which conditions on security incidents automatically trigger the McAfee ePO capabilities that you selected for the profile. You also have the option to select an alternate input field for the Configuration Item \(CI\) field and set filtering conditions so that only those security incidents that are related to your triggering event automatically launch the profile. The configuration step includes the following settings on the configuration form for the profile.

## Alternate configuration item \(CI\) trigger field

In cases when the Configuration item \(CI\) field on the ServiceNow AI Platform® Security Incident Response \(SIR\) security incident is not populated with a value, or a match cannot be found in the database, you can select an alternate field on the security incident to display any matching CI enrichment data found during the scan of your assets. For more information about the Configuration item and the Alternate configuration item fields on a security incident, see [Defining triggering conditions with a Configuration item \(CI\) field for a McAfee ePO profile](mcafee-epo-alternate-ci.md).

## Security tags

To help you track the status of isolated host machines and when malware scans are initiated, an optional tagging feature is available. By default, this option is disabled on the configuration form for profiles. If this option is enabled during the configuration step, security tag names are displayed on the configuration form. These are the names of the tags that are displayed on related security incidents. These tags inform you when a host isolation action is successfully initiated and when it is approved. After a host is successfully returned to the network, the security tag is automatically removed from the security incident. For malware scans, a tag is displayed on the related security incident when a scan is scheduled. After the scan is finished, the scheduled tag is automatically replaced by a tag that indicates that the scan is successfully completed.

## Auto-trigger based on incident

When the Auto-trigger based on incident option is enabled, the filter condition builder is available, and you are required to set filtering conditions that specify when the profile runs automatically. A common filter is Category is malicious code activity™ and Business impact is 1 - Critical™. With these filters, only security incidents that are related to malicious code and that have a critical business impact launch the profile. Using the Auto-trigger option can reduce the number of security incidents that automatically invoke the profile.

## Approvals

If your organization wants an extra level of control over actions such as isolating host machines and initiating malware scans, you can enable the Require approval option during the configuration step for a profile.

For example, if both the approval and tagging features are enabled for a profile, after a request to isolate a host machine or to return it to the network is submitted for approval, the associated security incident is tagged automatically that the action is initiated. Requests are sent for approval to a user with the sn\_si.admin role by default, but this approval can be reassigned to another individual or an approval group to fit the needs of your organization. Approvers process requests in **My Approvals** in their ServiceNow AI Platform® instances. Security tags are displayed on related security incidents. All workflow activities are also logged in work notes to create an audit trail.

## ServiceNow audit log in the McAfee ePO console

In version 5.10.0 of McAfee ePO, a ServiceNow tab is displayed with a log of commands that are initiated from your ServiceNow AI Platform® instance. After an action or a query is invoked from a profile in your ServiceNow AI Platform® instance on a host machine \(endpoint\) in the McAfee ePO console, an audit log of ServiceNow commands is created in the McAfee ePO console. This log is displayed in the System tree in the McAfee ePO console and helps you audit the times of the commands that are sent to specific endpoints. To view logged ServiceNow events on specific machines in a McAfee ePO console, follow these steps.

1.  Navigate to the System tree in your McAfee ePO console and locate the ServiceNow tab.
2.  Click the tab to open a list of host machines.
3.  In the Name column, click a host name to open the audit log.

In the following image, an example of a log for a host \(`PODCLIENT1`\) is displayed.

![System tree in ePO console](../image/mcafee_newtab.png "PODClient")

The events initiated from the profiles in your ServiceNow AI Platform® instance are recorded and displayed in the log. Verify by checking the status of the host machine that the events listed in the log are successfully completed on the host.

## Example profiles

The following topics include examples for how to configure profiles and test security incidents. These examples include profiles for all of the McAfee ePO capabilities that are available for this integration.

-   **[Configure profiles and security incidents for system enrichment queries for the McAfee ePO integration](../task/mcafee-epo-configure-profile.md)**  
Configure your profile settings so that the profile triggers only under the conditions that you set.

**Parent Topic:**[McAfee ePO integration capability profiles](mcafee-epo-creating-profiles.md)

