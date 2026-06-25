---
title: Deleting threat intelligence library records
description: Delete threat intelligence library records such as observables, indicators, and objects.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/threat-intelligence-security-center/tisc-delete-lib-records.html
release: australia
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2026-03-12"
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

    \[Omitted image "tisc-delete-library-record.png"\] Alt text: Delete library records

4.  Select **Delete**.

    The record will be deleted from threat intelligence library.


## What to do next

Refer to the section [Define an Observable](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/threat-intelligence-security-center/define-an-observable.md) to create a record.

**Parent Topic:**[Threat Intelligence Security Center Library](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/threat-intelligence-security-center/threat-intelligence-security-center-library.md)

**Related topics**  


[TISC Data Model]()

[TISC Library Objects form view]()

[TISC Library Repository]()

[Access Vulnerability Downstream actions]()

[Export intelligence data]()

[Confirm Potential Relationships from Related Records]()

[Automated Correlation]()

