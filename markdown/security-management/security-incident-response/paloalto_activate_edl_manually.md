---
title: Activate an EDL manually for Palo Alto Networks Next-Generation Firewall
description: If the Palo Alto Networks firewall administrator is not using the ServiceNow AI Platform, and you are directly notified that the Palo Alto Networks Next-Generation Firewall is configured, you can activate the External Dynamic List \(EDL\) manually.
locale: en-US
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Activate an EDL for Palo Alto Networks Next-Generation Firewall, Palo Alto Networks Next-Generation Firewall integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Activate an EDL manually for Palo Alto Networks Next-Generation Firewall

If the Palo Alto Networks firewall administrator is not using the ServiceNow AI Platform, and you are directly notified that the Palo Alto Networks Next-Generation Firewall is configured, you can activate the External Dynamic List \(EDL\) manually.

## Before you begin

In Palo Alto Networks, assign an EDL object, policy, and the source URL to the EDL you created. For more information about configuring the EDL to the Palo Alto Networks Next-Generation Firewall in Palo Alto Networks, see [Configure an EDL in Palo Alto Networks Next-Generation Firewall](paloalto-config_firewall_pa.md).

Role required: sn\_si.admin

## About this task

As the ServiceNow AI Platform security incident administrator, you are notified by the Palo Alto Networks firewall administrator when the EDL configuration is complete in the Palo Alto Networks Next-Generation Firewall.

## Procedure

1.  Navigate to **All** &gt; **Palo Alto Networks NGFW Integration** &gt; **Firewall EDL Configuration**.

    ![Select Firewall EDL Configuration.](../image/4-30-fedl-nav.png)

2.  Select the **Firewall EDL Configuration** module.

3.  In the Palo Alto Networks Firewall External Dynamic Lists list, click an item in the **Name** column to open it.

4.  On the record that opens, select the **Active** check box.

    ![Select Active check box.](../image/4-30-active-edl.png)

5.  Click **Update**.

    In the **Active** column of the Palo Alto Networks Firewall External Dynamic Lists list, `true` is displayed for the state of the EDL.

    ![EDL activated (true) in Active column.](../image/4-30-edl-list-active.png)


## Result

The EDL is activated and ready to receive EDL entries

## What to do next

Submit EDL entries from a security incident or from the blocklist.

-   **[Configure an EDL in Palo Alto Networks Next-Generation Firewall](paloalto-config_firewall_pa.md)**  
The Palo Alto Networks firewall administrator configures an EDL to the Palo Alto Networks Next-Generation Firewall once notified the Retrieval URL is available from the ServiceNow AI Platform. Before the EDL can accept EDL entries, it must be configured in Palo Alto Networks, and activated in the ServiceNow AI Platform®.

**Parent Topic:**[Activate an EDL for Palo Alto Networks Next-Generation Firewall](paloalto-activate-edl.md)

