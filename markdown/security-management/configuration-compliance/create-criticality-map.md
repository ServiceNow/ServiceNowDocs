---
title: Create a Configuration Compliance criticality map
description: Configuration Compliance criticality mapping provides a transform map for third-party source criticality fields to recognizable fields in Configuration Compliance severity.
locale: en-US
release: australia
product: Configuration Compliance
classification: configuration-compliance
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Configuration Compliance, Unified Security Exposure Management, Security Operations]
---

# Create a Configuration Compliance criticality map

Configuration Compliance criticality mapping provides a transform map for third-party source criticality fields to recognizable fields in Configuration Compliance severity.

## Before you begin

Role required: sn\_vulc.admin

## Procedure

1.  Navigate to **All** &gt; **Configuration Compliance** &gt; **Administration** &gt; **Criticality Mapping**.

2.  Click **New**.

3.  Fill in the fields on the form, as appropriate.

<table id="table_vks_thr_ns"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Source

</td><td>

The name of the source for the criticality mapping.

</td></tr><tr><td>

Source value

</td><td>

The source criticality value.

</td></tr><tr><td>

Target value

</td><td>

The target value. Choices are: -   **Critical**

The configuration issue associated with the control is causing a disruption to one or more business-critical CIs.

-   **High**

The configuration issue associated with the control is a threat, but is not causing a shutdown of critical network resources.

-   **Moderate**

The configuration issue associated with the control is a risk, but is not an immediate threat.

-   **Low**

The configuration issue associated with the control is a low-level threat and can be ignored in favor of CIs that are at greater risk.

-   **Minor**

The configuration issue associated with the control is a minor risk and can be ignored if necessary.

</td></tr></tbody>
</table>4.  Click **Submit**.


