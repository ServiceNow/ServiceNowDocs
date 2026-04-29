---
title: Create an EcoVadis connection and configuration
description: Create a connection to fetch and update scores from EcoVadis to help ensure that your risk and theme scores remain current when using Third-party Risk Management.
locale: en-US
release: australia
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [TPRM with EcoVadis, Integrate, Third-party Risk Management, Governance, Risk, and Compliance]
---

# Create an EcoVadis connection and configuration

Create a connection to fetch and update scores from EcoVadis to help ensure that your risk and theme scores remain current when using Third-party Risk Management.

## Before you begin

Activate the Vendor Risk Management integration with EcoVadis application \[com.sn\_app\_grc\_ecovadis\]. To see the instructions for downloading a GRC application from the ServiceNow® Store, see [Download a GRC application from the ServiceNow Store for the first time](../../grc-common/task/download-grc-first-time.md).

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **EcoVadis for third-party Risk Management** &gt; **Connections &amp; Credential Aliases** and select **EcoVadis Connection Alias**.

2.  Select the Create new connection &amp; credential related link.

3.  Fill out the form.

    |Field|Description|
    |-----|-----------|
    |Connection Name|Name of the connection.|
    |Connection URL|EcoVadis API base address.|
    |Credential Name|Name of the EcoVadis credential.|
    |User Name|Username of the user in EcoVadis.|
    |Password|Password of the user in EcoVadis.|

4.  Select **Create**.

5.  After creating a connection, set up a configuration by navigating to **All** &gt; **EcoVadis for third-party Risk Management** &gt; **Configuration**.

6.  Select **New**.

7.  Enter a name and select the EcoVadis Config connection that you created.

    **Note:** You can only create one configuration.


**Parent Topic:**[Integrating EcoVadis with Third-party Risk Management](../concept/tprm-integrating-ecovadis.md)

