---
title: Configure a dosage specification for a medication product associated with a program
description: Create a dosage specification associated with a medication product included in a program.
locale: en-US
release: yokohama
product: Healthcare and Life Sciences Service Management Core
classification: healthcare-and-life-sciences-service-management-core
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configure dosage specifications for a medication product, Configure, Healthcare and Life Sciences Service Management Core, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Configure a dosage specification for a medication product associated with a program

Create a dosage specification associated with a medication product included in a program.

## Before you begin

-   [Configure a program](hcls-create-program.md#).

    **Note:** When configuring a program, associate medication products with the program.


Role required: sn\_hcls.admin

## About this task

By default, the application provides a few sample dosage characteristics for the Healthcare and Life Sciences workflows that you can as a reference when creating a dosage characteristic. All the same dosage characteristics are associated with the Dosage Characteristics group.

## Procedure

1.  Navigate to **All** &gt; **HCLS Service Management** &gt; **Administration** &gt; **Dosage specifications**.

    Alternatively, when [configuring a program](hcls-create-program.md#), select the Dosage specifications related list.

2.  In the Dosage specifications list, modify an existing dosage specification or click **New** to create another specification.

3.  On the form, fill in the fields.

<table id="table_jfm_xnv_gtb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name to identify the dosage specification.

</td></tr><tr><td>

Program

</td><td>

Program associated with the medication product,

</td></tr><tr><td>

Medication product

</td><td>

Medication product being prescribed for the patient.

</td></tr><tr><td>

Primary diagnosis

</td><td>

Main condition in a patient submitted by the practitioner as the reason for the healthcare service requested.

</td></tr><tr><td>

Secondary diagnosis

</td><td>

Coexisting condition that might exist in a patient submitted by the practitioner.

</td></tr><tr><td>

Tertiary diagnosis

</td><td>

Highly specialized medical care recommended for the patient by the practitioner.

</td></tr><tr><td>

Dosage definition

</td><td>

This field is automatically set to dosage definition value based on the dosage specification as the template.

</td></tr><tr><td>

State

</td><td>

Status of the dosage specification.

 If you have not published the dosage specification, this field is automatically set to **Draft**. If you have already published the dosage specification, this field is automatically set to **Published**.

</td></tr><tr><td>

Active

</td><td>

Option for enabling the dosage specification.

</td></tr><tr><td>

Description

</td><td>

Additional information about the dosage specification.

</td></tr></tbody>
</table>4.  Save the dosage specification settings.

    -   Save a new specification by clicking **Submit**.
    -   Save the changes to an existing specification by clicking **Update**.
5.  [Configure characteristics for the dosage specification](hcls-create-program.md#).

6.  Publish the dosage specification for use in the medication products added to the associated program.

    1.  In the Dosage specifications list, select the dosage specification.

    2.  On the Dosage specification form, click **Publish**.


