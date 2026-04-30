---
title: Edit the HR case template for an HR catalog item
description: Edit the HR case template for an HR catalog item to automatically populate fields on an HR case form when a request for that item is made.
locale: en-US
release: xanadu
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [HR catalog item configuration, HR service catalog management, HR services, HR Administration, Case and Knowledge Management, HR Service Delivery, Employee Service Management]
---

# Edit the HR case template for an HR catalog item

Edit the HR case template for an HR catalog item to automatically populate fields on an HR case form when a request for that item is made.

## Before you begin

Role required: sn\_hr\_core.admin

## Procedure

1.  Navigate to **All** &gt; **HR Administration** &gt; **HR Services** &gt; **Manage HR Catalog**.

2.  Hover over the HR catalog item and click **Edit Case Template**.

    ![Edit the HR case template for an HR catalog item](../image/edit-hr-case-template-for-hr-catalog-item.png)

3.  Fill in the fields on the form, as appropriate.

    **Note:** This is the new UI form view. To switch to the classic environment, click **Switch to Classic UI** in the form header.

<table id="table_tcl_wtg_3fb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the HR case template.

</td></tr><tr><td>

Active

</td><td>

Option to activate the HR case template for use.

</td></tr><tr><td>

COE

</td><td>

HR case table \(COE\) that the HR case is categorized under when a request for that HR service is made.**Note:** Make sure that the COE for the HR case template matches that of the associated HR service.

</td></tr><tr><td>

Owning group

</td><td>

Group that is responsible for the HR case template.

</td></tr><tr><td>

Short Description

</td><td>

Short description that appears on the HR case form when a request for that HR service is made.

</td></tr><tr><td>

Priority

</td><td>

Priority assigned to the HR case when a request for that HR service is made.

</td></tr><tr><td>

Assignment type

</td><td>

Assignment of the HR case when a request for that HR service is made. You can assign the HR case to a user, skill, or group. Select one of the following:-   Named user: In the **Assigned to** field, select a user.
-   Skills/Assignment group: In the **Skills** or **Assignment Group** field, select a skill or group.


</td></tr><tr><td>

Use global descriptions for translations

</td><td>

Option to enable the use of global descriptions for translations. If selected, you can provide the short description and description for the HR case template in one or more languages. See [Translations for HR cases and tasks](../concept/translation-of-hr-cases-and-tasks.md#) for more information.You can use dynamic variables to personalize your short and global descriptions.

 Using dynamic variables in an HR task template works in:

-   HR tasks related to HR cases in the legacy UI or HR Service Delivery Agent Workspace
-   Employee Center Pro To-dos form
-   Lifecycle Events ticket form
**Note:** Because some dynamic variables might provide personal information, use the sn\_hr\_core.task\_template\_variable\_ignore system property to ensure privacy. For example, social security number \(ssn\) is excluded by default. You can add other variables to this system property to disable them but ensure they are comma separated with no spaces between each variable.

</td></tr><tr><td>

Add field

</td><td>

Fields to automatically populate on the HR case form when a request for that HR service is made. Select one or more fields from the **Add field** list and provide the desired values. For example, you can add the **State** field to set a default case state or add the **PDF Template** field to select a document for cases that require a document acknowledgement or signature.Any changes that you make to the template fields or values will take precedence over the original template values in the fields.

 **Note:** Select the Document Template option to associate a document template \(of Document Templates \[com.snc.document\_templates\] plugin\) with an HR service.

</td></tr></tbody>
</table>4.  Click **Update**.


**Parent Topic:**[HR catalog item configuration](../concept/hr-catalog-item-configuration.md)

**Previous topic:**[Edit the record producer for an HR catalog item](edit-hr-record-producer-for-hr-catalog-item.md)

**Next topic:**[Link knowledge articles or managed documents to an HR catalog item](link-knowledge-article-to-hr-catalog-item.md)

