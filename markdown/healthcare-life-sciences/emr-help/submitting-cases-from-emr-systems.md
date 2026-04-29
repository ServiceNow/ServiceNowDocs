---
title: Creating healthcare cases from within your EMR
description: Use the EMR Help service portal to create healthcare cases from directly within you EMR system.
locale: en-US
release: australia
product: EMR Help
classification: emr-help
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Create requests within your EMR system, EMR Help, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Creating healthcare cases from within your EMR

Use the EMR Help service portal to create healthcare cases from directly within you EMR system.

As a user with the sn\_ind\_rmt\_help.requester role, you can submit healthcare cases from within your EMR system. These cases can then be fulfilled within a ServiceNow instance.

**Note:** The healthcare case request capability can only be fulfilled for custom healthcare case types. In order to fulfill healthcare cases, you must first create your own custom healthcare case type. For more information on this, see [Configure healthcare case types for EMR Help](../task/configure-hcls-case-types-for-emr-help.md).

## Creating a healthcare case

To create a case from within your EMR, select Healthcare Case from the Requests option menu in the upper right. The Healthcare Case form will then appear.

![The Health Case request form in the EMR portal.](../image/hcls-emr-healthcare-case.png)

<table id="table_uxg_b1p_b1c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

EMR session information

</td><td>

EMR session information will displays the values for any configured parameters that have been captured from EMR.

 If you have a parameter configured to display here but it does not generate, it is because there no value passed from the EMR for that parameter.

 These fields populate automatically and are read only.

</td></tr><tr><td>

Healthcare organization

</td><td>

The healthcare organization associated with this healthcare case.

 This field populates automatically based on user's associated organization.

</td></tr><tr><td>

Healthcare practitioner

</td><td>

The healthcare practitioner associated with this healthcare case.

 This field populates automatically based on the practitioner making the request.

</td></tr><tr><td>

I need help with

</td><td>

The reason for your request.

 Select the type of healthcare service you need help with from the drop-down list.

</td></tr><tr><td>

Is this related to a patient record?

</td><td>

Select to indicate this request is associated with a patient record.

 If yes, the patient field becomes visible and available to populate.

</td></tr><tr><td>

Patient

</td><td>

The patient associated with this healthcare case.

 This field populates automatically if the **patient\_id**parameter is passed from the EMR.

</td></tr><tr><td>

Description

</td><td>

Description of your issue.

</td></tr><tr><td>

Protected health information \(PHI\)

</td><td>

Enter details such as patient name, medical record number \(MRN\), and date of birth \(DOB\).

 The value entered into this field is encrypted.

</td></tr></tbody>
</table>Click submit to route your healthcare case request to fulfilment.

## Submitted Healthcare case information

After submitting your Healthcare case, you can review the information you submitted directly from the portal.

![Submitted Healthcare case request displaying the activity tab.](../image/hcls-emr-healthcare-case-submitted.png)

-   The Activity tab displays the status of the request.
-   The Attachments tab displays any attachments associated with the request.
-   The Additional info tab displays a read only version of all information submitted on the request.

![Submitted healthcare case request displaying the Additional info tab.](../image/hcls-emr-healthcare-case-additional-info.png)

