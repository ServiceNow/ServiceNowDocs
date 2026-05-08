---
title: Activate an EDL for Palo Alto Networks Next-Generation Firewall
description: After the External Dynamic List \(EDL\) has been created in your ServiceNow AI Platform and the URL is available, the Palo Alto Networks firewall administrator configures the EDL in the Palo Alto Networks Next-Generation Firewall. The retrieval URL is used by the Palo Alto Networks firewall administrator to configure the EDL in the Palo Alto Networks Next-Generation Firewall server. Before it can accept EDL entries, the EDL must be configured in Palo Alto Networks and activated in the ServiceNow AI Platform.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Palo Alto Networks Next-Generation Firewall integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Activate an EDL for Palo Alto Networks Next-Generation Firewall

After the External Dynamic List \(EDL\) has been created in your ServiceNow AI Platform® and the URL is available, the Palo Alto Networks firewall administrator configures the EDL in the Palo Alto Networks Next-Generation Firewall. The retrieval URL is used by the Palo Alto Networks firewall administrator to configure the EDL in the Palo Alto Networks Next-Generation Firewall server. Before it can accept EDL entries, the EDL must be configured in Palo Alto Networks and activated in the ServiceNow AI Platform®.

## Before you begin

Role required: sn\_si.admin

## About this task

After the EDL is configured, as the security incident administrator, you can activate the EDL manually, or, the EDL is automatically activated upon completion of a ServiceNow AI Platform® Change Request. The EDL must be approved and moved from the inactive state to the active state before it can accept EDL entries.

## Procedure

1.  Navigate to **All** &gt; **Palo Alto Networks NGFW Integration** &gt; **Firewall EDL Configuration** and select the **Firewall EDL Configuration** module.

    ![Select Firewall EDL Configuration module.](../image/4-30-fedl-nav.png)

2.  In the Palo Alto Networks Firewall Dynamic Lists list that is displayed, select your new EDL in the Name column.

3.  On the record that is displayed, note the **Email FW retrieval URL** buttons, the active EDL Retrieval URL link, and, if configured, the ServiceNow AI Platform® change request in the Change Requests section.

    Make sure that the **Active** check box is cleared.

    ![Malware IP EDL not activated.](../image/4-30-edl-record.png)

    **Note:** With **Tabbed forms** cleared in your system settings, the EDL Retrieval URL appears in **EDL Retrieval Info** section as shown in the previous figure.

    The following figure shows the **EDL Retrieval Info** displayed as a tab with **Tabbed forms** selected in your system settings. Click the **EDL Retrieval Info** tab to display the retrieval URL. The link to the change request \(**CH0030015**\) is also displayed.

    ![Change request link highlighted.](../image/4-30-edl-app-notactive.png)

4.  To complete the configuration and move the EDL from inactive to active, you must choose one of the following options to notify the firewall administrator that the retrieval URL is available.

<table><thead><tr><th align="left" id="d171189e187">

Option

</th><th align="left" id="d171189e190">

Description

</th></tr></thead><tbody><tr><td id="d171189e196">

**Click __Email FW retrieval URL__.**

</td><td>

Email EDL Retrieval URL directly to the firewall administrator. This option permits the firewall administrator to finish the configuration on the Palo Alto Networks platform. Choose this option if the firewall administrator is not using the ServiceNow AI Platform® .

 **Note:** The security incident administrator manually activates the EDL in the ServiceNow AI Platform® after receiving notice that the Palo Alto Networks Next-Generation Firewall configuration is completed. See: [Activate an EDL manually](paloalto_activate_edl_manually.md).

</td></tr><tr><td id="d171189e245">

**Complete the ServiceNow AI Platform® change request and assign the configuration tasks to the firewall administrator.**

</td><td>

This option is available only if the firewall administrator for Palo Alto Networks is also using the ServiceNow AI Platform®, and the ServiceNow AI Platform® change management and approval processes are configured. **Note:** Users with the sn\_si.admin role can approve the ServiceNow AI Platform® change request. Once the configuration tasks are completed and the change request has been closed, the EDL is activated automatically. See: [Activate an EDL for Palo Alto Networks Next-Generation Firewall with a change request](paloalto_sncr_edl.md).

</td></tr></tbody>
</table>    After you notify the firewall administrator that the retrieval URL is available and you confirm the EDL has been configured in Palo Alto Networks, as the security incident administrator, your next step is to activate the EDL. You either activate the EDL manually, or, if configured, use the ServiceNow AI Platform change request form to activate the EDL.


-   **[Activate an EDL manually](paloalto_activate_edl_manually.md)**  
If the Palo Alto Networks firewall administrator is not using the ServiceNow AI Platform, and you are directly notified that the Palo Alto Networks Next-Generation Firewall is configured, you can activate the External Dynamic List \(EDL\) manually.
-   **[Activate an EDL for Palo Alto Networks Next-Generation Firewall with a change request](paloalto_sncr_edl.md)**  
If configured, the ServiceNow change request form is used to activate the External Dynamic List \(EDL\). This option is recommended if your firewall administrator is also using the ServiceNow AI Platform for firewall policy or rule changes. The EDL is activated automatically and ready to receive EDL entries upon closure of the ServiceNow AI Platform change request.

**Parent Topic:**[Palo Alto Networks Next-Generation Firewall integration](../concept/paloalto_integration.md)

**Previous topic:**[Create an EDL for Palo Alto Networks Next-Generation Firewall](palo_alto_config_edl.md)

**Next topic:**[Activate an EDL manually](paloalto_activate_edl_manually.md)

**Related topics**  


[Configure an EDL](paloalto-config_firewall_pa.md)

