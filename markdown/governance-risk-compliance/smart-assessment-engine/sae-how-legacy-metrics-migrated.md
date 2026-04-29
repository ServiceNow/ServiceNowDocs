---
title: How legacy metric types are migrated to sections in templates
description: Legacy metric types are migrated to specific sections in the assessment templates in the Smart Assessment Engine application.
locale: en-US
release: australia
product: Smart Assessment Engine
classification: smart-assessment-engine
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Reference, Smart Assessment Engine, Governance, Risk, and Compliance]
---

# How legacy metric types are migrated to sections in templates

Legacy metric types are migrated to specific sections in the assessment templates in the Smart Assessment Engine application.

## How metric types are mapped

This tables shows the mapping used to move the existing metric types to the section in the assessment templates.

|Existing metric type|Mapped to|
|--------------------|---------|
|Name \(Translated text\) \(Max length 255\)|**Name** \(Translated text\) field in the Assessment Template table.|
|Description \(Translated text\) \(Max length 1000\)|**Description** \(Translated html\) field in the Assessment Template table.|
|Table \(Table Name\)|**Table** \(Table Name\) field in the Context Item table.|

## How metric categories are mapped

This tables shows the mapping used to move the existing metric categories to the section table in the assessment templates.

|Existing metric type|Mapped to the Section table|
|--------------------|---------------------------|
|Name \(Translated text\) \(Max length 255\)|**Name** \(Translated text\) field.|
|Description \(Translated text\) \(Max length 1000\)|**Description** \(Translated text\) field.|
|Order \(Integer\)|**Order** \(Order Index\) field.|

## How metrics are mapped

This tables shows the mapping used to move the existing metrics to the question table in the assessment templates.

|Existing metric type|Mapped to the Question table|
|--------------------|----------------------------|
|Allow additional information \(True/False\)|**Enable justification** \(True/False\) field.|
|Data type \(String\) \(Max length 40\)|Based on the **Data type** field value, the appropriate question type reference is added to the Question table. Data type is string.|
|Details \(Translated html\) \(Max length 8000\)|**Guidance statement** \(Translated html\) field.|
|Question \(Translated text\) \(Max length 512\)|**Label** \(Translated text\) field.|
|Mandatory \(True/False\)|**Is mandatory** \(True/False\) field|
|Max \(Integer\)|**Max number** \(Decimal\) field|
|Min \(Integer\)|**Minimum number** \(Decimal\) field|
|Order \(Integer\)|**Order** \(Order index\)|

## How metric types are migrated to question types

After migration, all Question records are set as data type **Text**.

After migration, all Question records whose source metric is template/Numeric-scale are set with a response layout of **Horizontal**.

This tables shows the mapping used to move the existing metric types to the question types in the assessment templates.

|Existing metric type|Mapped to|
|--------------------|---------|
|Attachment|Attachment|
|Choice|Drop-down list|
|Date|Date|
|Date/Time|Date/Time|
|Likert scale|Radio button|
|Multiple selection|Check box|
|Numeric scale|Radio button|
|Reference|Reference|
|Yes/No|Radio button|

## How fields are mapped

This tables shows the mapping used to move the existing fields to the question table in the assessment templates.

|Field in the existing table|Mapped to the Question table|
|---------------------------|----------------------------|
|Reference table|**Table** field.|
|Condition|**Filter condition** field.|

## How metric definitions are mapped

This tables shows the mapping used to move the existing metric definitions to the choice table in the assessment templates.

|Metric definition in the existing table|Mapped to the Choice table|
|---------------------------------------|--------------------------|
|Display|**Text label** field in the Choice table|
|Order|**Integer** data type is mapped to the **Order** field in the Choice table that is based on the same ascending sequence of the template-definition records in the **Value** field that is associated with a particular template.|

## How assessment metric templates are mapped

Only templates where the **Allow image** field is set to false are migrated. No field mapping is done for this table.

Metrics whose data type is template are migrated as questions of the type Radio button if the **Allow image** field is set to false at the template level.

## How assessment template definitions are mapped

This tables shows the mapping used to move the existing template definitions to the choice table in the assessment templates.

|Assessment template definition in the existing table|Mapped to the Choice table|
|----------------------------------------------------|--------------------------|
|Display|**Text label** field.|
|Value|Integer data type is mapped to the **Order** field in the Choice table, based on the same ascending sequence of the template-definition records in the **Value** field that is associated with a particular template.|

