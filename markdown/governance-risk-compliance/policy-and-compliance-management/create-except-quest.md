---
title: Create an exception questionnaire
description: When you are setting up the Policy Exception Integration Registry, you can define configurable questions that can be included in risk assessments created from templates. The Policy Exception Integration Registry can be associated with one template at a time.
locale: en-US
release: yokohama
product: Policy and Compliance Management
classification: policy-and-compliance-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Allow policy exception requests from other applications, Policy and Compliance Management enhancement steps, Implement, Policy and Compliance Management, Governance, Risk, and Compliance]
---

# Create an exception questionnaire

When you are setting up the Policy Exception Integration Registry, you can define configurable questions that can be included in risk assessments created from templates. The Policy Exception Integration Registry can be associated with one template at a time.

## Before you begin

Role required: sn\_compliance.attestation\_creator

## Procedure

1.  Navigate to **All** &gt; **Policy and Compliance** &gt; **Policy Exceptions** &gt; **Exception Questionnaire**.

2.  Click **New**.

    ![New exception questionnaire](../image/exception-quest-new.png)

    **Note:** Notice that the Assessment Metric Type screen opened. In the terminology of GRC applications, a question in a questionnaire is considered a metric. A group of questions is a category. A group of categories is a metric type.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|The name of the questionnaire.|
    |Assessment duration|The amount of time allowed from the creation of the assessment to its completion.|
    |Table|The table containing the records to be assessed.|
    |Scale factor|The scale factor to be used for all questionnaire results.|
    |State|The publish state of the assessment: **Draft** or **Published**.|
    |Enforce condition|When selected, all records that do not meet the conditions defined are deleted.|
    |Roles|Roles that have Read access to the information in the assessment.|
    |Condition|Conditions for selecting records from the selected table to be assessed. For more information, see [Condition builder](https://www.servicenow.com/docs/access?context=c_ConditionBuilder&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US).|
    |Description|A description for this exception questionnaire.|

4.  Save the questionnaire record.

5.  Click **Attestation Designer** to create the questionnaire.

    For more information, see [Attestation Designer](../concept/c_Attestations.md#).


**Parent Topic:**[Allow policy exception requests from other applications](../concept/allow-other-app-policy-except.md)

