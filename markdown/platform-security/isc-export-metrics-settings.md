---
title: Export metrics settings
description: Use the configuration options in the Settings tab to narrow down reporting results.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Export metrics, Monitor instance metrics, Instance Security Center, Platform Security]
---

# Export metrics settings

Use the configuration options in the Settings tab to narrow down reporting results.

Access the settings for your export metrics by selecting the **Settings** tab.

## Settings configuration fields

<table id="table_pqt_ljl_hpb"><thead><tr><th>

Configuration

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Classifications for Metrics

</td><td>

Add or remove classifications to this field to determine which exports are included in the **Classified Exports by User** and **Classified Exports by Table** reports. These reports support the following classifications:-   Personally identifiable information
-   Confidential
-   Restricted
-   Internal
-   Public

For more detail on data classifications, see [Data classifications](data-classification.md)

</td></tr><tr><td>

Classifications for Alerts

</td><td>

Add or remove classifications to this field to determine which exports trigger instance security notifications. The classifications supported in the **Classifications for Metrics** field are supported here. For more detail on these alerts, see the security notifications section on the [Instance Security Center](instance-security-center.md) page. The **Record Threshold** field defines the number of records exported before your instance triggers and alert.

</td></tr><tr><td>

Record Threshold

</td><td>

Number of record a user must export to trigger an alert. To trigger an alert, these records must also match the classifications listed in the **Classifications for Alerts** field.

</td></tr></tbody>
</table>Save your settings by entering **Control + s** \(Windows\) or **⌘ + s** \(macOS\).

**Parent Topic:**[Export metrics](instance-sec-center-export-metrics.md)

