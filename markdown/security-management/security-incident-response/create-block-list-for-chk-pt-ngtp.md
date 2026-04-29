---
title: Create a block list for the Check Point NGTP integration
description: Create a Block List in your ServiceNow AI Platform instance. Once approved and activated, you can create entries for these Block Lists from observables determined to be malicious on Now Platform Security Incident Response \(SIR\) incidents and request approval to block them.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Working with block lists, Check Point Next Generation Threat Prevention integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Create a block list for the Check Point NGTP integration

Create a Block List in your ServiceNow AI Platform instance. Once approved and activated, you can create entries for these Block Lists from observables determined to be malicious on Now Platform Security Incident Response \(SIR\) incidents and request approval to block them.

## Before you begin

Role required: Security Incident Administrator \(sn\_si.admin\)

## About this task

Create the Block List on your ServiceNow AI Platform instance so that the Check Point can import objects — IP addresses, URLs, domains — included in the list. Custom Intelligence Feed is configured on Check Point Gateway which pulls the IP addresses, URLs, Domains from Now platform at pre-configured interval. To ensure blocking the observables, the Threat Prevention Policy should be configured with Anti-Bot and Anti-Virus Blades activated.

**Note:** The figures in this topic are shown with **Tabbed forms** cleared in System Settings.

![System Settings > Forms](../image/system-settings.png)

## Procedure

1.  After the application installation is complete, navigate to **Integrations** &gt; **Integration Configurations**.

2.  Locate the **Check Point Next Generation Threat Prevention** card and click **Configure**.

    ![Check Point NGTP integration card](../image/check-point-card.png)

    **Note:** Privileged and Proprietary content used with permission from Check Point Software Technologies, Ltd.

3.  Click **Create new Block List**.

    ![Check Point NGTP configuration](../image/check-point-configure.png)

4.  On the form, fill in the fields.

<table id="table_kpf_lrk_ls"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Check Point Block Request List name.Include the observable type \(URL, IP, domain\) in this field so the security analyst can easily recognize the intention of the Block List by its name. The name should also clearly indicate what firewall policy these Block List objects are mapped to. Some examples of Block List names are, Outbound Malware IP, or Outbound Phishing URL.

</td></tr><tr><td>

Active

</td><td>

This check box is cleared by default to indicate that the Block List is inactive.When inactive, the Block List is unable to receive additional entries.

 When the check box is selected \(When Change Request is closed or change request is not generated\), the Block List is activated and available for Block List entries.

</td></tr><tr><td>

Display Tag

</td><td>

Check box is selected by default to automatically tag the observable and the associated security incident record if the observable is blocked on Block List. When selected, the “Tag for observables” field is available on the form.**Note:** A tag name is created by default from the value you enter in the Name field with a Check Point-prefix, for example, Check Point-Malware OutBound IP. You can change the tag name and color. The tag name is displayed in the field “Tag for observables”, once the Block List is saved.

 When the check box is cleared, no tag is created, and the “Tag for observables” field is not available on the form.

</td></tr><tr><td>

Observable Type

</td><td>

Select an observable type this Block List accepts from the list: IP Address \(including CIDR for allow list\), URL, or domain.

</td></tr><tr><td>

Tag Type

</td><td>

Tags that are available from the list.A Block list is a list of observables that you want the Check Point Next Generation Threat Prevention to block.

 A allow list is a list of observables you do not want to block in Check Point Next Generation Threat Prevention in any case.

 By default, the Block list tag color is black, and the allow list tag color is Gray. You can change the color.

</td></tr><tr><td>

Create Change Request

</td><td>

This check box is selected by default to automatically create a change request and change tasks in your ServiceNow AI Platform instance, which are attached to the Block List record.The change request is used to configure the Block List retrieval URL in the Check Point Next Generation firewall gateway.

 This option is recommended if your firewall administrator is also using the ServiceNow AI Platform for firewall policy or rule changes. If you create a request, once it is closed, the Block List is automatically activated.

 Clear the check box to manually activate the Block List after receiving notice via email from the firewall administrator that the Custom Intelligence Feed has been configured on all the Check Point Gateways.

 When the check box for Create change request is cleared, the Change request field is unavailable.

</td></tr><tr><td>

Request Approval

</td><td>

This check box is selected by default to request approvals for activating/removing Block List entries from Block Lists. Approval is requested from the users having role Security Incident Administrator\(sn\_si.admin\). Approval request will be sent via email to the approvers. Once the approval is accepted, the entry will be activated on that Block List.

 When the check box is not selected, the entries for that Block List will not follow approval workflow and will be directly activated on block list.

</td></tr><tr><td>

Tag for Observable

</td><td>

This field is displayed only if the Display tag check box is selected. Field is automatically populated after the Block List is saved with a default value from the Name field. If Block List is created with name ‘Malware URL’, the tag name derived is ‘Block List – Malware URL’

</td></tr><tr><td>

Change Request

</td><td>

When the Create change request check box is selected, the change request number is displayed on the Now Platform instance once the Block List is saved. When the check box for Create change request is cleared, this field is not displayed.

</td></tr><tr><td>

Description

</td><td>

Description of the Check Point Block List. The name generally contains the types of sites and observables you would expect to be on this Block List, and you can use this field for more details.

</td></tr><tr><td>

Expiration Period \(days\)

</td><td>

Expiration period of the Block List.0 \(the default\) indicates that the Block List entry never expires.

 If you change this value, this entry is active for the number of days you enter. You can enter a minimum value of 1 which is 24 hours, and there is no maximum value.

</td></tr><tr><td>

Retrieval URL

</td><td>

Retrieval URL will be generated automatically, once the Block List is saved. To configure this Block List on Check Point Gateways, you must use this URL. Once this URL is configured, Check Point fetches observables to be blocked in csv format.

</td></tr></tbody>
</table>    ![Block list request list](../image/block-request-list.png)

5.  Click **Submit**.

6.  If the Check Point Block Request List is not displayed, navigate to **Check Point NGTP Integration** &gt; **Block Request Lists**.

    ![Block List Request Lists](../image/new-block-request.png)

    The new Block List is displayed. The Block List status is still inactive \(false\), which means the Block List is not available to accept entries. If Create change request was configured, a message is displayed indicating a change request and tasks have been created in your ServiceNow AI Platform instance.

    ![Block List Request entries](../image/block-request-list2.png)

7.  In the **Name** column, click an item to open the record.

    The Block List record is displayed. This example shows a Malware Outbound IP Block List. The following fields, options, and links are displayed on the new record after submission and described in the following table.

    ![Retrieved URL](../image/requested-url-redbox.png)

<table id="table_twk_jcd_qgb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Email Retrieval URL

</td><td>

Emails a notice that the Block Link is available for configuration to the Check Point firewall administrator.

</td></tr><tr><td>

Retrieval URL

</td><td>

This URL is used to configure Custom Intelligence Feed on Check Point Gateways.**Note:** If you have your System Settings set to Tabbed forms, this link is displayed on the Block List Retrieval Info tab at the bottom of the record.

</td></tr><tr><td>

ServiceNow AI Platform change request

</td><td>

A link to the change request record is displayed in the Change Requests section when configured, and the request number is displayed in the Change request field.

</td></tr><tr><td>

Update

</td><td>

Modify data and update the editable fields.

</td></tr><tr><td>

Delete

</td><td>

Delete the record.

</td></tr></tbody>
</table>8.  Create and add more Block Lists as required.

    The Block Lists are displayed on the Check Point Block Request Lists Page.


## What to do next

Activate the Block Request List manually, or with a ServiceNow AI Platform change request.

