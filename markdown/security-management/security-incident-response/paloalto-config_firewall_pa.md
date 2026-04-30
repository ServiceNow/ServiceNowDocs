---
title: Configure an EDL in Palo Alto Networks Next-Generation Firewall
description: The Palo Alto Networks firewall administrator configures an EDL to the Palo Alto Networks Next-Generation Firewall once notified the Retrieval URL is available from the ServiceNow AI Platform. Before the EDL can accept EDL entries, it must be configured in Palo Alto Networks, and activated in the ServiceNow AI Platform.
locale: en-US
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Activate an EDL manually for Palo Alto Networks Next-Generation Firewall, Activate an EDL for Palo Alto Networks Next-Generation Firewall, Palo Alto Networks Next-Generation Firewall integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Configure an EDL in Palo Alto Networks Next-Generation Firewall

The Palo Alto Networks firewall administrator configures an EDL to the Palo Alto Networks Next-Generation Firewall once notified the Retrieval URL is available from the ServiceNow AI Platform. Before the EDL can accept EDL entries, it must be configured in Palo Alto Networks, and activated in the ServiceNow AI Platform®.

## Before you begin

Role required: Palo Alto Networks firewall administrator

## About this task

The Palo Alto Networks Next-Generation Firewall administrator creates an EDL object, and assigns the source \(Retrieval\) URL and policy to the EDL. These tasks are performed in Palo Alto Networks before the EDL is activated in the ServiceNow AI Platform.

The images in the following section are used by permission and are PRIVILEGED and PROPRIETARY.

## Procedure

1.  If you have not configured the EDL to the firewall, navigate to **External Dynamic Lists** &gt; **Objects** in Palo Alto Networks.

    ![Task: Navigate to the Objects tab to view EDLs.](../image/4-30-pa-3-cropped.png)

2.  In the **Name** column, select the ServiceNow EDL you want to configure from the list, for example, **ServiceNow EDL for URL**.

    ![Task: Select the EDL in the Name column.](../image/4-30-pa-3-box.png)

3.  In the External Dynamic Lists dialog box, enter the Username and Password to authenticate with the ServiceNow AI Platform®.

    These credentials are the Username and Password you created for the API account role \(sn\_sec\_panfw.api\_account\_access\) in your ServiceNow instance.

    ![Task: Enter Username and Password for the ServiceNow AI Platform API account.](../image/paloalto-acct.png)

4.  In the Source field, enter the URL that was generated on the EDL list in your ServiceNow instance.

    ![Task: Copy the Retrieval URL in the Source field.](../image/4-30-pa-1-dialog-5-7.png)

5.  Select a Certificate Profile from the choice list, `SN2`, for example.

6.  Click OK.


**Parent Topic:**[Activate an EDL manually for Palo Alto Networks Next-Generation Firewall](paloalto_activate_edl_manually.md)

