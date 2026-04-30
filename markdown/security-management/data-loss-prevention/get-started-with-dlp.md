---
title: Get started with DLP Incident Response
description: Review the following information before you start setting up your Data Loss Prevention Incident Response \(DLP IR\) application.
locale: en-US
release: zurich
product: Data Loss Prevention
classification: data-loss-prevention
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Explore, Data Loss Prevention Incident Response, Security Operations]
---

# Get started with DLP Incident Response

Review the following information before you start setting up your Data Loss Prevention Incident Response \(DLP IR\) application.

<table id="table_k2d_1bk_ynb"><thead><tr><th>

Setup task

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Verify that you have assigned the required ServiceNow AI Platform and DLP roles.

</td><td>

DLP Incident Response supports the following roles:-   The administrator \(admin\) installs the applications from the ServiceNow Store and assigns the DLP administrator \(sn\_dlir.admin\).
-   sn\_dlir.admin
-   sn\_dlir.analyst

</td></tr><tr><td>

Verify that the ServiceNow core applications that are required to support the Data Loss Prevention Incident Response application are installed and activated.

</td><td>

The Data Loss Prevention Incident Response plugin \(com.snc.data\_loss\_incident\) is required to support the Data Loss Prevention Incident Response product.Verify that the following Security Operations applications are installed and activated from the ServiceNow Store. If not installed, install and activate one application at a time in the following order to ensure a smooth installation:

-   Data Loss Prevention Incident Response \(com.snc.data\_loss\_incident\)
-   Security Support Common

 For more information on setting up your ServiceNow AI Platform instance for the integration, see [Get entitlement for a Security Operations product or application](../../security-incident-response/task/entitle-secops-product.md) or [Activate a ServiceNow Store application](../../security-incident-response/task/activate-entitled-store-app.md).

</td></tr><tr><td>

Domain separation

</td><td>

Verify the [Domain separation and DLP Incident Response](domain-separation-and-dlp.md) topic if you intend to separate data, processes, and administrative tasks.

</td></tr></tbody>
</table>**Parent Topic:**[Exploring Data Loss Prevention Incident Response](../concept/exploring-dlp.md)

**Related topics**  


[DLP Incident Response overview](../concept/understanding-data-loss-prevention.md)

