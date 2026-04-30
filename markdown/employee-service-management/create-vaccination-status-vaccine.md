---
title: Configure vaccine or vaccine booster types for Vaccination Status
description: Create or modify vaccine or vaccine booster types that people can use to report their vaccination status.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Vaccination Status, Safe Workplace, Health and Safety, Employee Service Management]
---

# Configure vaccine or vaccine booster types for Vaccination Status

Create or modify vaccine or vaccine booster types that people can use to report their vaccination status.

## Before you begin

Role required: sn\_imt\_vaccine.admin

## About this task

Vaccine and vaccine booster reporting requires Vaccine response definition records. Each record contains vaccine-specific information so that users can properly report their vaccination status with the correct type of vaccine. For example, you can create a record for single-dose or multi-dose vaccine and set the number of days between doses. These configurations determine the questions users must answer when reporting their vaccination. Vaccination Status contains several generic COVID-19 vaccines that do not require configuration.

## Procedure

1.  Navigate to **All** &gt; **Vaccination status** &gt; **Vaccine response definitions**.

2.  Click **New** or open a record.

3.  On the form, fill in the fields.

<table id="table_mqb_zv5_4qb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Vaccine type

</td><td>

The type of vaccine, such as a COVID-19 mRNA vaccine or a vaccine booster.

</td></tr><tr><td>

Manufacturer

</td><td>

The name of the vaccine manufacturer.

</td></tr><tr><td>

SMS friendly name

</td><td>

A display name for the vaccine that displays in SMS messages.

</td></tr><tr><td>

Number of doses required

</td><td>

Number of doses required for full vaccination.

</td></tr><tr><td>

Booster parent vaccine

</td><td>

The parent vaccine the booster supports, such as a booster for a COVID-19 mRNA vaccine. **Note:** The **Booster parent vaccine** field appears only when you set the **Vaccine type** to **Booster**.

</td></tr><tr><td>

Recommended days until booster required

</td><td>

Number of days since vaccination before a booster is required. This field is visible only if **Vaccine type** is set to **Booster**.

</td></tr></tbody>
</table>4.  Click **Submit**.


**Parent Topic:**[Vaccination Status](../concept/vaccination-status.md)

