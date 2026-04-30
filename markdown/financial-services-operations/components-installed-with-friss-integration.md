---
title: Components installed with the Financial Services Operations Integration with FRISS
description: Several types of components are installed with activation of the Financial Services Operations Integration with FRISS \(com.sn\_fso\_intg\_friss\) plugin, including tables.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Integrating with FRISS, Integrating with third-party applications, Integrating applications, Financial Services Operations \(FSO\)]
---

# Components installed with the Financial Services Operations Integration with FRISS

Several types of components are installed with activation of the Financial Services Operations Integration with FRISS \(com.sn\_fso\_intg\_friss\) plugin, including tables.

## Roles installed

<table id="table_vl4_mlf_xwb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

FRISS integration admin\[sn\_fso\_intg\_friss.admin\]

</td><td>

Administrator role for managing the flows for FRISS integration.

</td></tr><tr><td>

FRISS integration viewer\[sn\_fso\_intg\_friss.viewer\]

</td><td>

Viewer role that provides read access to the Claim Fraud Indicator table.

</td></tr></tbody>
</table>## Plugins installed

The ServiceNow Integration Hub Starter Pack Installer \[com.glide.hub.integrations\] plugin is required to support Financial Services Operations Integration with FRISS.

|Plugin|Description|
|------|-----------|
|FRISS Spoke \(com.sn\_friss\_spoke\)|Provides a list of the actions to solve the fraudulent activity in the insurance industry. The actions include reducing the number of false reporting of claims, increasing the number of avoided claims, and processing the genuine claims immediately.|
|Financial Services Operations Core \(sn\_bom\)|Stores the customer data that is needed to make claim requests. For more information, see [Financial Services Operations Core](../../fso-common/reference/financial-services-operations-core-data-model.md).|

## Tables installed

Financial Services Operations Integration with FRISS references information from the following tables to store data:

-   Financial Services Operations tables that are installed when Commercial Lines Claims and Personal Lines Claims applications are installed.
-   Tables from Customer Service Management \(CSM\) application.
-   The ServiceNow AI Platform tables.

<table id="table_dfq_4yy_wwb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Claim Fraud Indicator\[sn\_fso\_intg\_friss\_indicator\]

</td><td>

Stores details on the indicators that contribute to the fraud score.

</td></tr></tbody>
</table>**Parent Topic:**[Financial Services Operations Integration with FRISS](../concept/fso-integration-with-friss-overview.md)

