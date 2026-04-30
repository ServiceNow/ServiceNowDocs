---
title: Create new EDL for Palo Alto Networks
description: Create new External Dynamic List \(EDLs\) for Palo Alto Networks. Once you create EDLs, you can start creating entries for those EDLs.
locale: en-US
release: xanadu
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2024-10-22"
reading_time_minutes: 2
breadcrumb: [Palo Alto Networks integration, TISC Security Tools - Firewall, TISC Security Tools integrations, TISC Integrations, Integrating Threat Intelligence Security Center, Threat Intelligence Security Center, Security Operations]
---

# Create new EDL for Palo Alto Networks

Create new External Dynamic List \(EDLs\) for Palo Alto Networks. Once you create EDLs, you can start creating entries for those EDLs.

## Before you begin

Role required: sn\_sec\_tisc.admin

## Procedure

1.  After you save the newly configured Palo Alto NGFW configuration, navigate to **EDLs** section.

2.  Click **New** to create new External Dynamic List \(EDLs\).

3.  On the form, fill in the fields.

<table id="table_uhs_45b_ddc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Palo Alto Networks Firewall Dynamic List name.

</td></tr><tr><td>

Observable Type

</td><td>

Select an observable type this EDL accepts from the choice list: IP \(including CIDR\), URL, or domain.

</td></tr><tr><td>

Expiry period \(days\)

</td><td>

Expiration period of the EDL.0 \(the default\) indicates that the EDL entry never expires. If you change this value, this entry is active for the number of days you enter. You can enter a minimum value of 1, and there is no maximum value.

For example, if you enter `30` days at 2:01 PM on Nov 1, the EDL will expire at 2:01 PM on Nov 30.

All entries in this EDL then inherit this value by default unless you override the value on individual entry basis.

</td></tr><tr><td>

Create change request

</td><td>

This check box is selected by default to automatically create a change request and change tasks in your ServiceNow AI Platform instance, which are attached to the EDL record.The change request is used to configure the EDL list retrieval URL in the Palo Alto Networks Next-Generation Firewall server.

This option is recommended if your firewall administrator is also using the ServiceNow AI Platform for firewall policy or rule changes. If you create a request, once it is closed, the EDL list is automatically activated.

</td></tr><tr><td>

Description

</td><td>

Description of the Palo Alto Networks Firewall Dynamic List. The name generally contains the types of sites and observables you would expect to be on this EDL, and you can use this field for more details.

</td></tr><tr><td>

Change Request

</td><td>

When the Create change request check box is selected, the change request number is displayed on the ServiceNow AI Platform instance once the EDL is saved.When the check box for **Create change request** is cleared, this field is not displayed.

</td></tr><tr><td>

Combine IP addresses and subnet addresses into a single entry

</td><td>

Option to combine both IP addresses and subnet addresses into a single entry. When you select this check box and if the IP of CIDR type is added then it will automatically remove the existing entries which falls in the CIDR range. For example: If there is an entry in EDL with value 192.168.1.1, and if a CIDR value of 192.168.1.0/24 is added to the same EDL, the initial IP address entry would be removed, since it falls within the CIDR range of the new entry.

**Note:** This option is displayed only when you select the **Observable Type** as IP.

</td></tr><tr><td>

EDL Retrieval URL

</td><td>

The URL link the Palo Alto Networks firewall administrator uses for configuration in the Palo Alto Networks firewall is automatically generated and displayed.

</td></tr></tbody>
</table>4.  Create and add more EDLs as required.

    The EDLs are displayed on the Palo Alto Networks External Dynamic Lists list.


**Parent Topic:**[Palo Alto Networks integration](../concept/palo-alto-networks-integration.md)

**Related topics**  


[Palo Alto EDL Approval Rules](tisc-edl-approval-rules.md)

