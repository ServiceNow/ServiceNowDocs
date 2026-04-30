---
title: Deleting threat intelligence library records
description: Delete threat intelligence library records such as observables, indicators, and objects.
locale: en-US
release: xanadu
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2025-12-04"
reading_time_minutes: 1
breadcrumb: [Threat Intelligence Security Center Library, Use, Threat Intelligence Security Center, Security Operations]
---

# Deleting threat intelligence library records

Delete threat intelligence library records such as observables, indicators, and objects.

## Before you begin

Role required: sn\_sec\_tisc.analyst

The following example procedure explains how to delete an observable record. You can use the same procedure to delete indicators or objects as well.

## Procedure

1.  Navigate to **Workspaces** &gt; **Threat Intelligence Security Center** &gt; **Threat Intel Library** &gt; **Observables** &gt; **All Observables**.

2.  Open any observable record.

3.  Select **Delete** to delete the aggregated record.

    When you select this action, then it will remove all the related records, except the original source data, and trigger reaggregation.

    A confirmation message will appear to verify that you want to delete the aggregated record. If you also want to delete the source records and prevent re aggregation, select the **Delete Source Records** check box. This action will remove all the associated source records.

    ![Delete library records](../image/tisc-delete-library-record.png)

4.  Select **Delete**.

    The record will be deleted from threat intelligence library.


## What to do next

Refer to the section [Define an Observable](define-an-observable.md) to create a record.

**Parent Topic:**[Threat Intelligence Security Center Library](../concept/threat-intelligence-security-center-library.md)

**Related topics**  


[Understanding the Data Model](../reference/understanding-the-data-model.md)

[TISC Library Objects form view](../concept/tisc-library-home-page-view.md)

[TISC Library Repository](../concept/tisc-ioc.md)

[Access Vulnerability Downstream actions](../concept/downstream-actions-from-the-vulnerability-form-view.md)

[Export intelligence data](tisc-export-observables.md)

[Confirm Potential Relationships from Related Records](confirm-potential-relationships.md)

[Automated Correlation](../concept/automated-correlation-rules.md)

