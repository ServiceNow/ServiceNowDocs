---
title: Case Type form
description: Use the Case Type form in the Compliance Case Management application to categorize the compliance cases by their type.
locale: en-US
release: yokohama
product: Compliance Case Management
classification: compliance-case-management
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Create a case type, Configuring Compliance Case Management, Compliance Case Management, Governance, Risk, and Compliance]
---

# Case Type form

Use the Case Type form in the Compliance Case Management application to categorize the compliance cases by their type.

See the following table for a description of the field values.

|Field|Description|
|-----|-----------|
|Label|Label to be displayed for the case type.|
|Name|Name of the case type. For example, Code of conduct.|
|Case category|Category of the case type. This field is automatically set to **Compliance case \[sn\_comp\_case\_compliance\_case\]**.|
|Active|Option to select the case type as active or inactive.|
|Description|Description about this case type. This description is for the administrator to understand the case subtype.|
|State Model|
|State Model|Workflow states for the case type. For more information, see [Create a state model to define the workflow states and transitions](../task/create-state-model.md).|
|Assessment Configuration|
|Assessment templates|Assessment template for the case type. If the **sn\_grc\_case\_mgmt.enable\_smart\_assessments** system property is set to **true**, then you can specify the Smart assessment templates that you want to use for performing smart assessment on action tasks. For more information, see [Create an assessment template](../task/ccm-create-assessment-template.md). For information on|
|Template Configuration|
|Document templates|Template to generate Portable Document Format \(PDF\) reports for compliance cases associated with this case type.|

**Parent Topic:**[Create a case type](../task/create-case-type.md)

