---
title: Field descriptions for a complaint case
description: Complaint cases help the complaint agents resolve complaint service requests that they receive from the customers.
locale: en-US
release: australia
product: Financial Services Complaint Management
classification: financial-services-complaint-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Work on a complaint case, Use, Complaint Management, Common applications, Financial Services Operations \(FSO\)]
---

# Field descriptions for a complaint case

Complaint cases help the complaint agents resolve complaint service requests that they receive from the customers.

When a complaint service request is submitted, it creates a complaint case. Some of the fields on the case form are populated from the request from which it is created.

After the case is assigned, a complaint agent fills out the fields on the case when working on the playbook activities in the case.

## Complaint case fields

The playbook activities in the **Playbook** tab of the complaint case provide case-related information.

<table id="table_xw5_vpd_pkb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Complaint details

</td></tr><tr><td>

Number

</td><td>

System-generated unique number for the case.

</td></tr><tr><td>

Customer

</td><td>

Consumer who submitted the complaint. The field doesn't appear when a business customer is selected in the **Account** field.

</td></tr><tr><td>

Account

</td><td>

Business customer who submitted the complaint. The field doesn't appear when a consumer is selected in the **Customer** field.

</td></tr><tr><td>

Contact

</td><td>

Contact of the business customer who submitted the complaint. The field doesn't appear when a consumer is selected in the **Customer** field.

</td></tr><tr><td>

Channel

</td><td>

Channel through which the complaint was received.

</td></tr><tr><td>

Financial account

</td><td>

Financial account of the customer.

</td></tr><tr><td>

Type

</td><td>

Type of complaint such as product related or other.

</td></tr><tr><td>

Category

</td><td>

Category for the complaint. This list contains the industry-standard categories that are based on the selected complaint type.

</td></tr><tr><td>

Subcategory

</td><td>

Subcategory for the complaint. This list contains the industry-standard subcategories that are based on the selected complaint category.

</td></tr><tr><td>

Short description

</td><td>

Brief description of the complaint.

</td></tr><tr><td>

Complaint summary

</td><td>

Detailed summary of the complaint.

</td></tr><tr><td class="sub-head" colspan="2">

Review and Response

</td></tr><tr><td>

Legal impact

</td><td>

Option to indicate if the complaint has a legal implication.If you select **Yes** in this field, the workflow automatically generates a complaint legal fulfillment task for a legal review. For more information, see [Work on a complaint task](../task/work-fso-complaint-task.md).

</td></tr><tr><td>

Regulatory impact

</td><td>

Option to indicate if the complaint has a potential regulatory impact.If you select **Yes** in this field, the workflow generates a quality control task. For more information, see [Work on a quality control task for a complaint case](../task/work-fso-quality-control-task.md).

</td></tr><tr><td>

Regulatory category

</td><td>

Regulation category for the complaint. The list shows the regulation categories configured by your complaint admin. For more information, see [Configure regulation categories and subcategories](../task/configure-regulation-categories-fso-complaint-mgmt.md).

 This field appears only when you select **Yes** in the **Regulatory impact** field.

</td></tr><tr><td>

Regulatory subcategory

</td><td>

Regulation subcategory for the complaint.The list shows the regulation subcategories configured by your complaint admin. For more information, see [Configure regulation categories and subcategories](../task/configure-regulation-categories-fso-complaint-mgmt.md).

 This field appears only when you select **Yes** in the **Regulatory impact** field.

</td></tr><tr><td>

Response template

</td><td>

Type of response template to use in the case.

</td></tr><tr><td>

Expected outcome

</td><td>

Resolution expected by the customer.

</td></tr><tr><td>

Response

</td><td>

Response drafted by the agent to resolve the case. To copy content from a response template and add to this field, select the response template icon \(![response template icon](../image/response-template-icon.png)\). For more information on how to use a response template, see [Use response templates to add information to cases](https://www.servicenow.com/docs/access?context=csm-aw-agent-use-response-template&version=australia&pubname=australia-customer-service-management&ft:locale=en-US).

**Note:** Response templates are available only if they're configured by your complaint admin. For more information, see [Define response templates](../task/configure-response-templates-fso-complaints.md).

</td></tr><tr><td class="sub-head" colspan="2">

Quality control

</td></tr><tr><td>

Quality control tasks

</td><td>

List of quality control tasks, if any, for the case.**Note:** A quality control task is generated if there's a potential regulatory impact identified for the case.

</td></tr><tr><td class="sub-head" colspan="2">

Customer outcome

</td></tr><tr><td>

Customer approval

</td><td>

Field to indicate the state changes for customer approval.

</td></tr><tr><td class="sub-head" colspan="2">

Findings and learnings

</td></tr><tr><td>

Findings and learnings

</td><td>

Findings and learnings from the case resolution.

</td></tr></tbody>
</table>