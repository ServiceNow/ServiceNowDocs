---
title: Confidence score calculation for hardware vulnerability assessment
description: Confidence Score is displayed for partially matched assessments, vulnerable items \(VITs\), and ignored assessments.
locale: en-US
release: zurich
product: Industrial Workspace
classification: industrial-workspace
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Operational Technology Hardware Vulnerability Assessment, Explore, Industrial Workspace, Operational Technology]
---

# Confidence score calculation for hardware vulnerability assessment

Confidence Score is displayed for partially matched assessments, vulnerable items \(VITs\), and ignored assessments.

## About Confidence Score Calculation

HVA uses a scoring mechanism called Confidence Score to indicate the accuracy of the CVE data matching the CPE-mapped normalized content of an OT device. Confidence Score is an aggregated calculation of the matching scores created by the matching algorithm in HVA.

The Confidence Score varies for the following assessments:

-   Fully matched assessments: The Confidence Score is 1 for full assessments as all the parameters in the CVE information matches the device discovery model values available for the OT device.
-   Partially matched assessments: The Confidence Score is less than 1 for partial assessments as all the parameters in the CPE information doesn’t match the device discovery model values available for the OT device.

Following is an example of calculating the confidence score from the Common Platform Enumeration \(CPE\) information available for an OT device.

The following is a sample of a vulnerability assessment record, **CVE-2019-13946**: ![Screenshot displaying a CVE vulnerability for the OT device, named OT_device_demo_internal_963.](../image/hva-confidence-score-example.png)

The following is a sample of information available in CPE Firmware mapped to the OT device, **OT\_device\_demo\_internal\_963**:![Screenshot displaying the CPE Firmware information available in the OT device, named OT_device_demo_internal_963.](../image/hva-cpe-firmware-info-example.png)

The following is a sample of the information available in discovery model for the OT device, **OT\_device\_demo\_internal\_963**:![Screenshot displaying the device discovery model information available in the OT device, named OT_device_demo_internal_963.](../image/hva-discovered-model-cpe-example.png)

## How to calculate the confidence score

If you compare the samples of the CPE Firmware mapped to the OT device and the discovery model for the OT device, you can see that:

-   There is only a partial match for the **Model** information. Due to a partial match, the model score is assigned a value of 20.
-   The **Version** information doesn't match so the version score is assigned a value of 0.

The confidence score range is 0–1. Based on the CPE information, the confidence score is calculated using the following formula:

```
((BASE SCORE) + (publisher score) + (model score) + (version score)) / 100
```

=

```
((25) + (25) + (20) + (0)) / 100
```

=

```
70 / 100
```

=

```
.70
```

**Note:** To refer to the values used to calculate the confidence score, see [Confidence score reference tables for hardware vulnerability assessment](otvr-hva-confidence-score-ref.md).

**Parent Topic:**[Operational Technology Hardware Vulnerability Assessment](../concept/understanding-hwd-vuln-assessment.md)

