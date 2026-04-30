---
title: View sensitive information for DLP alerts
description: View the detected sensitive information for DLP alerts.
locale: en-US
release: zurich
product: Data Loss Prevention
classification: data-loss-prevention
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Internet Content Adaption Protocol \(ICAP\) integration for DLP IR, Integrate, Data Loss Prevention Incident Response, Security Operations]
---

# View sensitive information for DLP alerts

View the detected sensitive information for DLP alerts.

## Before you begin

There are certain rules and policies configured in the respective integration and if anytime you are violating the defined policies then a DLP incident gets created and the match content displays that violated information under the Sensitive Information section of that DLP incident record.

Role required: sn\_dlir.analyst

**Note:** End users can also view the sensitive information by logging into DLP User Workspace.

## Procedure

1.  Navigate to **All** &gt; **DLP Incident Management** &gt; **DLP Analyst Workspace**.

    The DLP Workspace - My Incidents page displays on the DLP Analyst Workspace for the analysts.

2.  Open any DLP incident.

3.  Navigate to **Sensitive Information** tab.

    ![DLP incident sensitive information](../image/dlp-icap-match-content.png)

4.  Click on the violated record.

5.  View the match content information and take respective action as necessary.

    ![DLP incident sensitive information violated record.](../image/dlp-icap-match-content-details.png)


**Parent Topic:**[Internet Content Adaption Protocol \(ICAP\) integration for DLP IR](../concept/icap-dlp-integration.md)

