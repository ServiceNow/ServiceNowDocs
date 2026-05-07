---
title: Create EDL for Palo Alto Networks
description: Create External Dynamic List \(EDLs\) for Palo Alto Networks. After you create EDLs, you can start creating entries for those EDLs.
locale: en-US
release: australia
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Palo Alto Networks integration, Firewall integration, TISC Security Tools integrations, TISC Integrations, Integrate, Threat Intelligence Security Center, Security Operations]
---

# Create EDL for Palo Alto Networks

Create External Dynamic List \(EDLs\) for Palo Alto Networks. After you create EDLs, you can start creating entries for those EDLs.

## Before you begin

Role required: sn\_sec\_tisc.admin

**Important:** You must save the newly configured Palo Alto Networks configuration before proceeding.

## Procedure

1.  Navigate to **EDLs** section.

2.  Select **New** to create External Dynamic List \(EDLs\).

3.  On the form, fill in the fields.

<table id="table_uhs_45b_ddc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Palo Alto Networks - Firewall Dynamic List name.

</td></tr><tr><td>

Observable Type

</td><td>

Select an observable type this EDL accepts from the list:-   IP \(including CIDR\)
-   URL
-   Domain


</td></tr><tr><td>

Expiry period \(days\)

</td><td>

Expiration period of the EDL.The default value of 0 indicates that the EDL entry never expires. If you change this value, this entry is active for the number of days you enter. You can enter a minimum value of 1, and there is no maximum value.

For example, if you enter `30` days at 2:01 PM on Nov 1, the EDL will expire at 2:01 PM on Nov 30.

All entries in this EDL then inherit this value by default unless you override the value on individual entry basis.

</td></tr><tr><td>

Create change request

</td><td>

This check box is selected to automatically create a change request and change tasks in your ServiceNow AI Platform instance, which are attached to the EDL record.The change request is used to configure the EDL list retrieval URL in the Palo Alto Networks - Firewall server.

This option is recommended if your firewall administrator is also using the ServiceNow AI Platform for firewall policy or rule changes. If you create a request, after it is closed, the EDL list is automatically activated.

</td></tr><tr><td>

Description

</td><td>

Description of the Palo Alto Networks - Firewall Dynamic List. The name generally contains the types of sites and observables you would expect to be on this EDL, and you can use this field for more details.

</td></tr><tr><td>

Change Request

</td><td>

When the Create change request check box is selected, the change request number is displayed on the ServiceNow AI Platform instance after the EDL is saved.When the check box for **Create change request** is cleared, this field is not displayed.

</td></tr><tr><td>

Combine IP addresses and subnet addresses into a single entry

</td><td>

Option to combine both IP addresses and subnet addresses into a single entry. When you select this check box and add an IP of CIDR type, the system automatically removes existing entries that fall in the CIDR range. For example: If there is an entry in EDL with value 192.168.1.1, and if a CIDR value of 192.168.1.0/24 is added to the same EDL, the initial IP address entry would be removed, since it falls within the CIDR range of the new entry.

**Note:** This option is displayed only when you select the **Observable Type** as IP.

</td></tr><tr><td>

EDL Retrieval URL

</td><td>

The configuration URL for Palo Alto Networks is automatically generated and displayed for the administrator.**Note:** To access this EDL URL on the Palo Alto Networks Next-Generation Firewall \(NGFW\), verify that user credentials are configured with the appropriate role \[`sn_tisc_pa.api_account_access`\].

</td></tr></tbody>
</table>4.  Create and add more EDLs as required.

    The EDLs are displayed on the Palo Alto Networks EDLs.


**Parent Topic:**[Palo Alto Networks integration](../concept/palo-alto-networks-integration.md)

**Related topics**  


[Define Palo Alto Networks Approval Rules](tisc-edl-approval-rules.md)

