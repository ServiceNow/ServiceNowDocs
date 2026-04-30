---
title: Add locations to an emission factor
description: Add locations to an emission factor after you create the factor. The reason you must add locations to a factor is that an organization may have different locations and each location may have a different factor value for different periods.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Create an emission factor, Set up the emission factor library, Configure, Operational Sustainability Management \(formerly Environmental, Social, and Governance\)]
---

# Add locations to an emission factor

Add locations to an emission factor after you create the factor. The reason you must add locations to a factor is that an organization may have different locations and each location may have a different factor value for different periods.

## Before you begin

Role required: sn\_esg.program\_manager, sn\_esg.admin

## About this task

Usually, the factors are obtained from standard sources such as the Greenhouse Gas \(GHG\) protocol. Each factor for a location is effective for a specified time period. When you add locations to an emission factor, you specify the factor value for that particular location.

## Procedure

1.  Navigate to **All** &gt; **Operational Sustainability Management** &gt; **Operational Sustainability Workspace** &gt; **Lists** &gt; **Emission Factor Library** &gt; **Factor**.

2.  Open the emission factor for which you want to add locations.

3.  In the Emission factor locations related list, select **New**.

4.  On the form, fill in the fields.

<table id="table_nyn_sz5_d5b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Emission factor

</td><td>

Name of the emission factor for which you are adding the location. This field is automatically set.

</td></tr><tr><td>

Effective from

</td><td>

Date the emission is effective from.

</td></tr><tr><td>

Effective to

</td><td>

Date until which the emission would last.**Note:** If you do not specify the end date, then the factor value is applied indefinitely.

</td></tr><tr><td>

Location

</td><td>

Location of your emissions.**Note:** If you do not specify a location, then the factor value applies to all the locations of your organization.

</td></tr><tr><td>

Value

</td><td>

Value for the factor. For example, if natural gas emits 0.375 kg CO2eq/kWh ICV, then you can provide 0.375 as the value.

</td></tr></tbody>
</table>5.  Select **Submit**.


## Calculation logic for a location

Each location may have a parent location. For example, if your location is **Tokyo**, the parent location of Tokyo is Japan. Similarly, the parent location of Japan is Asia Pacific. If you select a parent location such as **Japan** in the **Location** field and specify the value as **1.5**, then the metrics are calculated using the value of 1.5 for any location that does not have a record but has the parent location as Japan. Similarly, if you select **Asia Pacific** in the **Location** field and specify the value as **2.5**, then the metrics are calculated using the value of 2.5 for any location that does not have a record but has the parent location as Asia Pacific.

**Parent Topic:**[Create an emission factor](create-an-emission-factor.md)

