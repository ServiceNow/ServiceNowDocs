---
title: Customize metric definitions
description: Customize the base system metric definitions based on your business requirements.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/digital-experience-score/dexscr-customize-dex-score-metric-defs.html
release: australia
product: Digital Experience Score
classification: digital-experience-score
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure DEX Score, Digital Experience Score, Digital End-User Experience, IT Service Management]
---

# Customize metric definitions

Customize the base system metric definitions based on your business requirements.

## Before you begin

Role required: sn\_dex\_score.digital\_workplace\_leader, sn\_dex.admin

## Procedure

1.  Navigate to **All** &gt; **Digital Experience Score​** &gt; **Metric Definition Configuration**.

2.  Open a metric definition configuration to modify its details.

3.  On the form, edit the **Metric visibility** field to determine who can view the metric.

    1.  Select the Unlock metric visibility icon \[Omitted image "icon-unlock-visible-fields.png"\] Alt text: and select the visibility type

    2.  From the drop-down list, select one of the following options:

        -   L1 checklist: Metric details are visible to service desk agents from the Investigation tab page of incident records for DEX monitored devices.
        -   Advanced: Metric details are visible to administrators and IT operators. Service desk agents can view advanced metrics by toggling **Show additional metrics** on the Investigation tab page of incident records.
    3.  To delete a value, select the value and then select the Remove selected item icon \[Omitted image "icon-remove.png"\] Alt text:.

    4.  Select the Lock Metric visibility icon \[Omitted image "icon-lock-visible-fields.png"\] Alt text:.

4.  Edit the **Metric category** field to specify the device health category that the metric is associated with.

    1.  Select the Lookup using list icon \[Omitted image "icon-magnifying-glass-blue.png"\].

    2.  On the Device self-service categories page, select a category from the Title list.

5.  On the form, customize the remaining fields.

    For a description of the field values, see [Metric definition form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/digital-experience-score/dexscr-dex-metric-def-form.md).

6.  Select **Update**.


**Parent Topic:**[Configuring Digital Experience Score​](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/digital-experience-score/dexscr-configuring-dex-score.md)

**Related topics**  


[Define qualitative mapping for a DEX Score metric](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/digital-experience-score/dexscr-define-qlty-metric-score-mapping.md)

[Metric scores in Digital Experience Score​](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/digital-experience-score/dexscr-dex-score-defs.md)

[DEX Score metrics calculation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/digital-experience-score/dexscr-dex-score-metrics-calc.md)

[DEX Score normalization for metric scores](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/digital-experience-score/dexscr-dex-score-normalization.md)

