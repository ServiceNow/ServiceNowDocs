---
title: Configure a block list as a Custom Intelligence Feed on the Check Point NGTP integration
description: The firewall administrator must configure the Custom Intelligence Feed corresponding to the Block List created in NOW platform.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Working with block lists, Check Point Next Generation Threat Prevention integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Configure a block list as a Custom Intelligence Feed on the Check Point NGTP integration

The firewall administrator must configure the Custom Intelligence Feed corresponding to the Block List created in NOW platform.

## Before you begin

Role required: admin

## About this task

This task needs to be performed on each of the Check Point NGTP Gateway. The firewall administrator would need the SSH access of the Gateway servers. If your organization has ServiceNow AI Platform change management and approval processes, verify that email send/receive capability is enabled.

The firewall administrator would need the retrieval URL of Block List and the ServiceNow user credentials with role Check Point API Account Access Role \(sn\_sec\_checkpoint.api\_account\_access\).

If Firewall administrator is not using NOW platform, the NOW Security Incident Administrator can provide the required information via an Email. Alternately, if firewall administrator is using NOW platform, the Change Request associated with Block List can be assigned to firewall administrator. This Change Request has the required information to configure Custom Intelligence Feed.

For more information on setting up Custom Intelligence Feed on Check Point Gateways, refer to: [https://supportcenter.checkpoint.com/supportcenter/portal?eventSubmit\_doGoviewsolutiondetails=&amp;solutionid=sk132193](https://supportcenter.checkpoint.com/supportcenter/portal?eventSubmit_doGoviewsolutiondetails=&solutionid=sk132193)

## Procedure

1.  Verify that email send/receive capability is enabled in your ServiceNow AI Platform instance by navigating to **Email properties** &gt; **Administration** &gt; **Email Properties**.

2.  Under Outbound Email Configuration, verify that **Email sending** and **Email receiving** are selected.

3.  Modify SSH to Check Point Gateway with expert mode.

4.  Execute the command to add Custom Intelligence Feed.

    The command execution is interactive and prompts for feed format and password.

    -   When prompted for Feed Format, enter ‘cp\_csv’
    -   When prompted for NOW platform user password with API Access.
    The command execution would warn about the server certificate \(NOW platform\) not being trusted by the machine and would prompt to add the server security certificate to machine’s trusted store. Enter **Y**.

    “Status:Succeed” message would appear, confirming that the Feed is successfully added.

    ![Custom Intelligence Feed status message](../image/custom-intell-feed-code.png)


