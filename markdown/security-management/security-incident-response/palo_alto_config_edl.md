---
title: Create an EDL for Palo Alto Networks Next-Generation Firewall
description: Create an External Dynamic List \(EDL\) in your ServiceNow AI Platform instance. Once approved and activated, you can create entries for EDLs from observables determined to be malicious on ServiceNow AI Platform Security Incident Response \(SIR\) incidents and request approval to block them.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Palo Alto Networks Next-Generation Firewall integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Create an EDL for Palo Alto Networks Next-Generation Firewall

Create an External Dynamic List \(EDL\) in your ServiceNow AI Platform instance. Once approved and activated, you can create entries for EDLs from observables determined to be malicious on ServiceNow AI Platform Security Incident Response \(SIR\) incidents and request approval to block them.

## Before you begin

Role required: sn\_si.admin

## About this task

Create the EDL on your ServiceNow AI Platform instance so that the firewall can import objects — IP addresses, URLs, domains — included in the list and enforce policy. To enforce policy on the EDL entries, the list is referenced in a policy rule or profile.

The figures in the following section are shown with **Tabbed forms** cleared in System Settings. For more information about selecting and clearing tabbed forms, see the "Display tabbed forms" section in [Configuring the form layout](https://www.servicenow.com/docs/access?context=configure-form-layout&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

## Procedure

1.  After the application installation is complete, navigate to **Integrations** &gt; **Integration Configurations**.

2.  Locate the Palo Alto Networks Next-Generation Firewall tile and click **Configure**.

    ![Palo Alto Networks Next-Generation Firewall Configure button](../image/4-20-tile.png)

3.  Click **Create new EDL List**.

    ![Create New EDL List.](../image/4-20-config-tile-resize.png)

4.  On the form, fill in the fields.

<table id="table_grp_ytz_tdb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**Name**

</td><td>

Palo Alto Networks Firewall Dynamic List name. Include the observable type \(URL, IP, domain\) in this field so the security analyst can easily recognize the intention of the EDL by its name. The name should also clearly indicate what firewall policy these EDL objects are mapped to. Some examples of EDL names are, Outbound Malware IP, or Outbound Phishing URL.

</td></tr><tr><td>

**Active**

</td><td>

This check box is cleared by default to indicate that the EDL is inactive. When inactive, the EDL is unable to receive additional entries.

 When the check box is selected, the EDL is activated and available for EDL entries.

</td></tr><tr><td>

**Display tag**

</td><td>

Check box is selected by default to automatically tag the observable and the associated security incident record if the observable is blocked on an EDL. When selected, the Tag type and EDL tag for observables fields are available on the form.**Note:** A tag name is created by default from the value you enter in the **Name** field with an EDL- prefix, for example, EDL-Malware OutBound IP. You can change the tag name and color. See: [\(Optional\) Edit the security tag name for Palo Alto Networks Next-Generation Firewall](paloalto_edit_sectag_name.md). The tag name is displayed in the EDL tag for observables field once the EDL is saved.

 When the check box is cleared, no tag is created, and the Tag type and EDL tag for observables fields are not available on the form.

</td></tr><tr><td>

**Observable type**

</td><td>

Select an observable type this EDL accepts from the choice list: IP \(including CIDR\), URL, or domain.

</td></tr><tr><td>

**Tag type**

</td><td>

Tags that are available from the choice list.A Block list is a list of observables that you want the Palo Alto Networks Next-Generation Firewall to block.

 An Allow list is a list of observables you want the Palo Alto Networks Next-Generation Firewall to allow.

 By default, the Block list tag color is black, and the Allow list tag color is gray. You can change the color. See: [\(Optional\) Edit the security tag name for Palo Alto Networks Next-Generation Firewall](paloalto_edit_sectag_name.md).

</td></tr><tr><td>

**Create change request**

</td><td>

This check box is selected by default to automatically create a change request and change tasks in your ServiceNow AI Platform instance, which are attached to the EDL record. The change request is used to configure the EDL list retrieval URL in the Palo Alto Networks Next-Generation Firewall server.

 This option is recommended if your firewall administrator is also using the ServiceNow AI Platform for firewall policy or rule changes. If you create a request, once it is closed, the EDL list is automatically activated.

Clear the check box to manually activate the EDL after receiving notice via email from the firewall administrator that the configuration on Palo Alto Networks is completed.When the check box for Create change request is cleared, the Change request field is unavailable.

</td></tr><tr><td>

**EDL tag for observables**

</td><td>

This field is displayed only if the Display tag check box is selected. Field is automatically populated after the EDL is saved with a default value from the Name field. For more information on changing the default tag name and color, see [\(Optional\) Edit the security tag name for Palo Alto Networks Next-Generation Firewall](paloalto_edit_sectag_name.md)

</td></tr><tr><td>

**Change request**

</td><td>

When the Create change request check box is selected, the change request number is displayed on the ServiceNow AI Platform instance once the EDL is saved.When the check box for Create change request is cleared, this field is not displayed.

</td></tr><tr><td>

**Description**

</td><td>

Description of the Palo Alto Networks Firewall Dynamic List. The name generally contains the types of sites and observables you would expect to be on this EDL, and you can use this field for more details.

</td></tr><tr><td>

**Expiration period \(days\)**

</td><td>

Expiration period of the EDL.0 \(the default\) indicates that the EDL entry never expires.

 If you change this value, this entry is active for the number of days you enter. You can enter a minimum value of 1, and there is no maximum value.

 For example, if you enter `30` days at 2:01 PM on May 1, the EDL will expire at 2:01 PM on May 31.

 All entries in this EDL then inherit this value by default unless you override the value on individual entry basis.

</td></tr></tbody>
</table>    ![Completed EDL record ready for submission.](../image/4-30-new-edl-cmplt.png)

5.  Click **Submit**.

6.  If the Palo Alto Networks Firewall External Dynamic Lists list is not displayed, navigate to **Palo Alto Networks NGFW Integration** &gt; **Firewall EDL Configuration** and click **Firewall EDL Configuration**.

    ![Select Firewall EDL Configuration.](../image/4-30-edl-cr-message.png)

    The new EDL is displayed. The EDL status is still inactive \(`false`\), which means the EDL is not available to accept entries. If **Create change request** was configured, a message is displayed indicating a change request and tasks have been created in your ServiceNow AI Platform instance.

    ![Change request message in the EDL list.](../image/4-30-edl-cr-message-callout.png)

7.  In the **Name** column, click an item to open the record.

    The EDL record is displayed. This example shows a Malware Outbound IP EDL. The following fields, options, and links are displayed on the new record after submission and described in the following table.

    ![EDL retrieval URL, Email retrieval URL button, and link to the change request.](../image/4-30-edl-record-callouts.png)

<table id="table_dts_pxz_tdb"><thead><tr><th>

Option

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**Email FW retrieval URL**

</td><td>

Emails a notice that the EDL link is available for configuration to the Palo Alto Networks firewall administrator.

</td></tr><tr><td>

EDL retrieval URL

</td><td>

This URL is placed in the **Source** field in the External Dynamic Lists authentication dialog box on the **Create List** tab on the Palo Alto Networks website.The URL link the Palo Alto Networks firewall administrator uses for configuration in the Palo Alto Networks firewall is automatically generated and displayed.

 **Note:** If you have your System Settings set to **Tabbed forms**, this link is displayed on the **EDL Retrieval Info** tab at the bottom of the record.

</td></tr><tr><td>

ServiceNow AI Platform change request

</td><td>

A link to the change request record is displayed in the Change Requests section when configured, and the request number is displayed in the Change request field.

</td></tr><tr><td>

**Update**

</td><td>

Modify data and update the editable fields.

</td></tr><tr><td>

**Delete**

</td><td>

Delete the record.

</td></tr></tbody>
</table>8.  Create and add more EDLs as required.

    The EDLs are displayed on the Palo Alto Networks External Dynamic Lists list.


## What to do next

Activate an EDL manually, or with a ServiceNow AI Platform change request.

**Parent Topic:**[Palo Alto Networks Next-Generation Firewall integration](../concept/paloalto_integration.md)

**Previous topic:**[Supported External Dynamic Lists for Palo Alto Networks Next-Generation Firewall](../reference/paloalto_supported_edls.md)

**Next topic:**[Activate an EDL for Palo Alto Networks Next-Generation Firewall](paloalto-activate-edl.md)

