---
title: Transform maps for IBM License Metric Tool \(ILMT\) and BigFix Inventory integration v2 APIs
description: When you import data from the IBM License Metric Tool \(ILMT\) or BigFix Inventory using version 2 of the ILMT and BigFix Inventory integration APIs, your ServiceNow instance uses a default transform map to process this data into ServiceNow tables.
locale: en-US
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Integrating using v2 APIs, ILMT and BigFix Inventory integrations, Software Asset Management publisher pack for IBM, Supported software publisher licenses, Software Asset Management, IT Asset Management]
---

# Transform maps for IBM License Metric Tool \(ILMT\) and BigFix Inventory integration v2 APIs

When you import data from the IBM License Metric Tool \(ILMT\) or BigFix Inventory using version 2 of the ILMT and BigFix Inventory integration APIs, your ServiceNow instance uses a default transform map to process this data into ServiceNow tables.

## Default ILMT and BigFix Inventory transform map

By default, the ServiceNow AI Platform provides the ILMT Software License Usage transform map to process the IBM license usage data that you import using version 2 of the ILMT and BigFix Inventory integration APIs. When you import this data into your ServiceNow instance, it is added to the source ILMT Product Usage Staging \[ilmt\_v2\_product\_usage\_staging\] and ILMT Device Usage Staging \[ilmt\_v2\_device\_usage\_staging\] tables. The ILMT Software License Usage transform map then uses the following table mappings to map the data from these source tables to the corresponding target tables:

<table id="table_u3v_wjr_yxb"><thead><tr><th>

Source Table

</th><th>

Target Table

</th></tr></thead><tbody><tr><td>

ILMT Product Usage Staging \[ilmt\_v2\_product\_usage\_staging\]**Note:** Data that is imported into this table is reported against your discovered IBM software products.

</td><td>

ILMT Product Usage \[ilmt\_v2\_product\_usage\]

</td></tr><tr><td rowspan="2">

ILMT Device Usage Staging \[ilmt\_v2\_device\_usage\_staging\]**Note:** Data that is imported into this table is reported against the hosts that are running your IBM software products.

**Note:** You can import data into this table only if you are using ILMT version 9.2.24 or later. You cannot import data into this table if you are using ILMT version 9.2.23 or earlier or if you are using BigFix Inventory.

</td><td>

ILMT Product Usage Per Server \[ilmt\_v2\_usage\_per\_server\]

</td></tr><tr><td>

ILMT Discovered Computer \[ilmt\_discovered\_computer\]

</td></tr></tbody>
</table>After the data is successfully mapped, it is updated in the corresponding target table records. You can then use the updated target table data to reconcile your IBM software products and verify compliance.

## ILMT and BigFix Inventory data processing

The ILMT Software License Usage transform map processes data by using the onStart transform map script. The onStart transform map script is an event script that processes at the beginning of an import. For more information on this transform map script, see [Map with transformation event scripts](https://www.servicenow.com/docs/access?context=r_MapWithTransformationEventScripts&version=australia&pubname=australia-integrate-applications&ft:locale=en-US).

**Parent Topic:**[Integrating with the IBM License Metric Tool \(ILMT\) or BigFix Inventory using v2 APIs](integrating-ilmt-bigfix-v2-apis.md)

