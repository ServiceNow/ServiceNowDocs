---
title: Configure the submission flow of the enrollment request form
description: Use scripted extension points to decide what records are created or updated after an enrollment request form is submitted.
locale: en-US
release: australia
product: Patient Support Services
classification: patient-support-services
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure, Patient Support Services, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Configure the submission flow of the enrollment request form

Use scripted extension points to decide what records are created or updated after an enrollment request form is submitted.

## Before you begin

**Important:**

Starting with the Yokohama release, Patient Support Services is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported.

For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support knowledge base.

Set the application scope to Patient Support Services using the application picker. For more information, see [Application picker](https://www.servicenow.com/docs/access?context=c_ApplicationPicker&version=australia&pubname=australia-application-development&ft:locale=en-US).

Role required: admin

## About this task

The Patient Support Services application installs the `sn_patientservice.EnrollmentCaseUtilService` script, the `EnrollmentCaseUtilService` script include, and the `EnrollmentCaseServiceExtPoint` extension point.

The sn\_patientservice.EnrollmentCaseUtilService script is preconfigured for the enrollment request form available by default within the application. Before creating an enrollment case, the application runs the sn\_patientservice.EnrollmentCaseUtilService script and uses the following submission workflow logic to create records and avoid duplication of records:

1.  Create a patient record if one doesn't exist.
2.  Create a consumer record if one doesn't exist.
3.  Create a practitioner record if one doesn't exist.
4.  Create a member plan if one doesn't exist.

Using extension points makes it easier to integrate customizations without actually altering the base code. You can extend standard base functionality using customized scripts. For more information, see [Using extension points to extend application functionality](https://www.servicenow.com/docs/access?context=extension-points&version=australia&pubname=australia-api-reference&ft:locale=en-US).

An implementation is available in the base system for scripted extension points. You can modify the data and add additional fields.

## Procedure

1.  Navigate to **All** &gt; **System Extension Points** &gt; **Scripted Extension Points**.

2.  In the **API Name** column, search for and click **sn\_patientservice.EnrollmentCaseServiceExtPoint**.

3.  On the Extension Point form, select a script include to use the `EnrollmentCaseServiceExtPoint` extension point.

    -   Modify the existing script by going to the Implementations related list and clicking **sn\_patientservice.EnrollmentCaseServiceExtPoint**.
    -   Create and register a custom script include.
4.  Customize the submission workflow logic of your enrollment form by adding the `createPatient`, `createMemberPlan`, and `createPractitioner` methods to your script include that implements the `EnrollmentCaseServiceExtPoint` extension point.

    You can create multiple implementations for an extension point and provide an order number for each implementation. The implementation that has the lowest order number is executed first.

<table id="table_fkq_ww3_jtb"><thead><tr><th>

Customization

</th><th>

Implementation

</th></tr></thead><tbody><tr><td>

Create a patient record if none exist.

</td><td>

Include the `createPatient` method of the `EnrollmentCaseServiceExtPoint` extension point in the implementation.

</td></tr><tr><td>

Create a member plan if none exist.

</td><td>

Include the `createPatient` method of the `EnrollmentCaseServiceExtPoint` extension point in the implementation.

</td></tr><tr><td>

Create a practitioner record if none exist.

</td><td>

Include the `createPatient` method of the `EnrollmentCaseServiceExtPoint` extension point in the implementation.

</td></tr></tbody>
</table>5.  On the Extension Point form, click **Update**.


