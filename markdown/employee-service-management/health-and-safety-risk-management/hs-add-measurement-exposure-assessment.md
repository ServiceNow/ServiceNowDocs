---
title: Add a measurement and exposure source for an exposure assessment
description: Add a measurement recorded for the exposure type when performing an exposure assessment.
locale: en-US
release: xanadu
product: Health and Safety Risk Management
classification: health-and-safety-risk-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Perform an exposure assessment for a location, Safety exposure management, Use, Health and Safety Risk Management, Health and Safety, Employee Service Management]
---

# Add a measurement and exposure source for an exposure assessment

Add a measurement recorded for the exposure type when performing an exposure assessment.

## Before you begin

Role required: sn\_hs\_rm.industrial\_hygienist or sn\_hs\_rm.exposure\_writer

## Procedure

1.  Navigate to **All** &gt; **Health and Safety** &gt; **Health and Safety Workspace**.

2.  Select the risk management icon \(![Risk management icon](../image/icon-risk-assessment.png)\).

3.  Select the **Exposure types** list, open the exposure type, and select the exposure assessment record that you want to add the measurement to.

4.  In the **Measurements** tab, select **New**.

5.  On the form, fill in the fields.

<table id="table_sm4_tg4_zdc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Date and time of measurement

</td><td>

Date and time when this measurement is recorded.

</td></tr><tr><td>

Measurement unit

</td><td>

Unit of measurement for this exposure type.The list shows units based on the exposure category selected in the exposure type.

The unit choices for an exposure category are defined in the `Measurement unit` column of the Measurement \[sn\_hs\_rm\_measurement\] table. For more information, see [Define a category and measurement unit for an exposure type](hs-define-category-measurement-unit-exposure-type.md).

</td></tr><tr><td>

Measurement

</td><td>

Measurement value recorded for the exposure.

</td></tr><tr><td>

TWA \(Time-weighted average\)

</td><td>

Time-weighted average for the exposure.

</td></tr><tr><td>

Description

</td><td>

Detailed information about this measurement.

</td></tr></tbody>
</table>6.  Select **Save**.

    The **Exposure sources** tab appears.

7.  In the **Exposure sources** tab, select **New** to add the source of this exposure.

    You can add multiple exposure sources, if relevant.

8.  Select **Save**.


## Result

-   The measurement value is listed in the **Measurements** tab of the exposure assessment.
-   The source of the exposure type is listed in the **Exposure sources** tab of the measurement record.
-   Based on the measurement limit defined in the exposure creation condition, the measurement can trigger an exposure record in the **Exposures** tab in these ways:
    -   If the measurement value exceeds the limit, an exposure record is created in the **Exposures** tab. The people affected by this exposure are added in the **Affected people** tab of the generated exposure.

        However, if an active exposure exists for this measurement, no new exposure record is created.

    -   If the measurement is below the limit and an active exposure exists for this assessment, the exposure end date is automatically set to the measurement date. It's because the exposure no longer meets the criteria, making it irrelevant. Additionally, the exposure's state is updated to obsolete and the associated action schedule for the exposure is marked as inactive.

**Parent Topic:**[Perform an exposure assessment for a location](hs-perform-exposure-assessment.md)

