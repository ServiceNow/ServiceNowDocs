---
title: Dosage concepts
description: You can increase the efficiency of healthcare representatives and reduce manual errors by configuring dosage specifications for a medication product associated with a program
locale: en-US
release: xanadu
product: Healthcare and Life Sciences Service Management Core
classification: healthcare-and-life-sciences-service-management-core
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Configuring dosage specifications for a medication product, Configuring Healthcare and Life Sciences Service Management Core, Healthcare and Life Sciences Service Management Core, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Dosage concepts

You can increase the efficiency of healthcare representatives and reduce manual errors by configuring dosage specifications for a medication product associated with a program

A dosage comprises the following key components:

-   [Dosage specifications](hcls-dosage-concept.md#section_xwz_z3x_htb)
-   [Dosage characteristics](hcls-dosage-concept.md#section_ur1_bjx_htb)
-   [Dosage characteristic groups](hcls-dosage-concept.md#section_cl5_qjx_htb)

To learn about how dosage components are linked to each other, see [Dosage characteristics mapping](hcls-dosage-concept.md#section_fwn_cjx_htb).

## Dosage specifications

A dosage specification consists of diagnosis details and dosage characteristics of a medication product associated with a program. For more information, see [Dosage specification table](../reference/hcls-dosage-spec-table.md).

**Note:** When you add a dosage specification for a medication product, an equivalent dosage definition entry is added in the application. A dosage definition models a dosage specification for use as a request definition parameter. For more information, see [Dosage definition table](../reference/hcls-dosage-defn-table.md).

## Dosage characteristics

A dosage characteristic defines the attributes of a dosage specification.

A dosage characteristic has the following features:

-   Is included in the **Dosage characteristics** characteristic group and a characteristic group mapped to a field in the Dosage details section of a medication prescription form.
-   Can include a characteristic option to restrict the characteristic value. For example, to restrict the quantity of dosage. Else, when a characteristic option isn't specified for a dosage characteristic, a healthcare representative can later fill the corresponding field value in the Dosage details section of the Medication Prescription form.
-   Is unique for a characteristic group when multiple entries for a characteristic are created. For example, when a dosage specification includes quantity characteristic as quantity per month supply, you can't add another characteristic for the quantity per week supply.
-   Similar dosage characteristics are stored in the Characteristic Group \[sn\_prd\_pm\_configuration\] table.

**Note:** For each dosage characteristic added to a dosage specification, a dosage variable is automatically created. A dosage variable is displayed as a dynamic field in the Dosage characteristics section of the Medication Prescription form. For more information, see [Dosage variable table](../reference/hcls-dosage-var-table.md).

## Characteristic groups for a dosage

A dosage characteristic group comprises the similar characteristics of a dosage specification. Each dosage characteristic maps to a field in the Dosage details section of the Medication Prescription form. For a dosage characteristic to appear with a dosage specification, you must include it in the following characteristic groups:

-   A characteristic group mapped to a field in the Dosage details section of a medication prescription form.
-   The **Dosage characteristics** characteristic group available by default.

## Dosage characteristics mapping

You map a dosage characteristic group with a field in the Dosage details section of the Medication Prescription form. You can use the `DosageCharacteristicsMapper` extension point to configure the mapping between a characteristic group and a field in the Dosage details section of the Medication Prescription form. For more information, see [Configure the mapping between a dosage characteristic and a dosage details field](../task/hcls-ext-point-dosage-char-map.md).

By default, the application provides a few sample characteristics and characteristic groups for the Healthcare and Life Sciences workflows that you can as a reference when creating a dosage specification.

The following figure illustrates the default mapping between characteristics and characteristic groups of a dosage specification, and the mapping between characteristic group of a dosage specification and dosage details fields of a medication prescription.

![Infographic displaying default mapping of characteristics, characteristic groups, and the dosage details of a medication prescription.](../image/hcls-characteristics.png "Default mapping of characteristics, characteristic groups, and the dosage details")

