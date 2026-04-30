---
title: Map the processing activity fields to a question response
description: Map some of the processing activity fields with the responses of the assessment questions to update the processing activity details based on the assessment response.
locale: en-US
release: zurich
product: Privacy Workspace
classification: privacy-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Create a privacy assessment, Configure, Privacy Management, Governance, Risk, and Compliance]
---

# Map the processing activity fields to a question response

Map some of the processing activity fields with the responses of the assessment questions to update the processing activity details based on the assessment response.

## Before you begin

Role required: sn\_privacy.admin

## About this task

A processing activity form has multiple fields. You can choose which responses of the assessment questions must be copied to the various fields of the processing activity record. For example, you can configure that if a certain question has Yes as an answer, then the short description of that question must be used in the **Name** field of the processing activity form.

The following table shows mappings between the fields on the processing activity form with the assessment template configurations:

|Field type in assessment configuration|Field labels on the assessment template configurations|Field labels on the processing activity form|
|--------------------------------------|------------------------------------------------------|--------------------------------------------|
|String|Name|Name|
|String|Description|Processing activity purpose|
|String|Data retention period \(in days\)|Data retention period \(in days\)|

## Procedure

1.  Navigate to **All** &gt; **Privacy Management** &gt; **Assessments** &gt; **All Assessment Templates**.

2.  Click and open the required assessment template.

3.  In the Metric Categories related list, click the required metric.

    The metric category expands.

4.  Click the question from which you want to copy the fields to the processing activity.

5.  Click the **Processing Activity Configuration** section.

6.  From the **Processing activity field** field, select the field that must be populated in the processing activity form.

7.  Click **Update**.


**Parent Topic:**[Create a privacy assessment](create-assessment-template.md)

