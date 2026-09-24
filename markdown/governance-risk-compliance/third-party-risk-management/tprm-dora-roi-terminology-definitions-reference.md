---
title: Terminology and definitions fields
description: Field descriptions and the full set of closed-set options for the Terminology and definitions list, used to populate the DORA B\_99.01 Register of Information export.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/third-party-risk-management/tprm-dora-roi-terminology-definitions-reference.html
release: brazil
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 2
keywords: [DORA, Register of Information, B\_99.01, terminology definitions, TPRM]
breadcrumb: [RoI export terminology, Register of information regulatory packages, Use digital resilience third-party registers, Third-party Risk Management, Governance, Risk, and Compliance]
---

# Terminology and definitions fields

Field descriptions and the full set of closed-set options for the **Terminology and definitions** list, used to populate the DORA B\_99.01 Register of Information export.

## Field descriptions

|Field|Description|
|-----|-----------|
|Row ID|Unique identifier for one of the 19 fixed rows, for example `R0010`.|
|Column Code|The Register of Information field that the option applies to, using EBA template and field numbering, for example `B_02.01.0020` refers to field 0020 on template B\_02.01.|
|Column Name|The name of the field on the referenced RoI template, for example `Type of contractual arrangement`.|
|Option|The specific closed-set value from the referenced field that this row defines, for example `1.Standalone arrangement`.|
|Description|Your organization's internal definition of the option. This is the only editable field. If left blank, the B\_99.01 export still succeeds with an empty value for that option.|
|Order|The row's position in the B\_99.01 CSV export.|

## Full field mapping

The rows are pre-seeded by the system and can't be created or deleted.

|Row ID|Column Code|Column Name|Option|Order|
|------|-----------|-----------|------|-----|
|R0010|B\_02.01.0020|Type of contractual arrangement|1. Standalone arrangement|10|
|R0020|B\_02.01.0020|Type of contractual arrangement|2. Overarching arrangement|20|
|R0030|B\_02.01.0020|Type of contractual arrangement|3. Subsequent or associated arrangement|30|
|R0040|B\_02.02.0170|Sensitiveness of the data stored by the ICT third-party service provider|1. Low|40|
|R0050|B\_02.02.0170|Sensitiveness of the data stored by the ICT third-party service provider|2. Medium|50|
|R0060|B\_02.02.0170|Sensitiveness of the data stored by the ICT third-party service provider|3. High|60|
|R0070|B\_06.01.0110|Impact of discontinuing the function|1. Low|70|
|R0080|B\_06.01.0110|Impact of discontinuing the function|2. Medium|80|
|R0090|B\_06.01.0110|Impact of discontinuing the function|3. High|90|
|R0100|B\_07.01.0050|Substitutability of the ICT third-party service provider|1. Not substitutable|100|
|R0110|B\_07.01.0050|Substitutability of the ICT third-party service provider|2. Highly complex substitutability|110|
|R0120|B\_07.01.0050|Substitutability of the ICT third-party service provider|3. Medium complexity in terms of substitutability|120|
|R0130|B\_07.01.0050|Substitutability of the ICT third-party service provider|4. Easily substitutable|130|
|R0140|B\_07.01.0090|Possibility of reintegration of the contracted ICT service|1. Easy|140|
|R0150|B\_07.01.0090|Possibility of reintegration of the contracted ICT service|2. Difficult|150|
|R0160|B\_07.01.0090|Possibility of reintegration of the contracted ICT service|3. Highly complex|160|
|R0170|B\_07.01.0100|Impact of discontinuing the ICT services|1. Low|170|
|R0180|B\_07.01.0100|Impact of discontinuing the ICT services|2. Medium|180|
|R0190|B\_07.01.0100|Impact of discontinuing the ICT services|3. High|190|

