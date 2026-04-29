---
title: Activate a block list for the Check Point NGTP integration
description: After the Block List has been created in your ServiceNow AI Platform and the URL is available, the Check Point administrator configures the Block List as Custom Intelligence Feed on all the Check Point Next Generation Gateways. Before it can accept Block List entries, the Block List must be configured in Check Point and activated in the ServiceNow AI Platform.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Working with block lists, Check Point Next Generation Threat Prevention integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Activate a block list for the Check Point NGTP integration

After the Block List has been created in your ServiceNow AI Platform and the URL is available, the Check Point administrator configures the Block List as Custom Intelligence Feed on all the Check Point Next Generation Gateways. Before it can accept Block List entries, the Block List must be configured in Check Point and activated in the ServiceNow AI Platform.

## Before you begin

Role required: Security Incident Administrator \(sn\_si.admin\)

## About this task

After the Block List is configured, as the security incident administrator, you can activate the Block List manually, or, the Block List is automatically activated upon completion of a ServiceNow AI Platform Change Request. The Change Request must be approved and moved from the inactive state to the active state before it can accept Block List entries.

## Procedure

1.  Navigate to **All** &gt; **Check Point NGTP Integration** &gt; **Block Request Lists**, and select the **Block Request Lists** module.

2.  In the **Check Point Block Request Lists** list that is displayed, select your new Block List in the **Name** column.

3.  On the record that is displayed, note the **Email Retrieval URL** button, the active Block List Retrieval URL link, and, if configured, the ServiceNow AI Platform change request in the Change Requests section.

    Also note that the Active check box is cleared.

    ![Malware Outboind IP](../image/malware-outbound-ip.png)

    **Note:** With Tabbed forms cleared in your system settings, the Block List Retrieval URL appears in Retrieval URL section.

4.  Click the **Block List Retrieval URL** tab to display the retrieval URL.

    The following figure shows the Block List Retrieval URL displayed as a tab with Tabbed forms selected in your system settings. The link to the change request \(CH0030270\) is also displayed.

    ![Malware Outbound IP showing Change Requests](../image/malware-outbound-ip2.png)

5.  To complete the configuration and move the Block List from inactive to active, you must choose one of the following options to notify the firewall administrator that the retrieval URL is available.

<table id="table_kpf_lrk_ls"><thead><tr><th>

Option

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Click Email Retrieval URL.

</td><td>

Email Block List Retrieval URL directly to the firewall administrator. This option permits the firewall administrator to finish the configuration on the Check Point platform. Choose this option if the firewall administrator is not using the ServiceNow AI Platform.

</td></tr><tr><td>

Complete the ServiceNow AI Platform change request and assign the configuration tasks to the firewall administrator.

</td><td>

This option is available only if the firewall administrator for Check Point is also using the Now Platform, and the ServiceNow AI Platform change management and approval processes are configured.**Note:** Users with the Security Incident Administrator \(sn\_si.admin\) role can approve the ServiceNow AI Platform change request. Once the configuration tasks are completed and the change request has been closed, the Block List is activated automatically.

</td></tr></tbody>
</table>
## What to do next

After you notify the firewall administrator that the retrieval URL is available, and you confirm the Block List has been configured in Check Point, as the security incident administrator, your next step is to activate the Block List. You either activate the Block List manually or, if configured, use the ServiceNow AI Platform change request form to activate the Block List. The Block List is automatically activated when the change request is closed.

