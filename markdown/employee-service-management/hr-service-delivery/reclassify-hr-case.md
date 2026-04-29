---
title: Transfer an HR case
description: You can create and use methods to reclassify or transfer an opened HR case from one HR service to another. Oftentimes an HR case opens as a General Benefits Inquiry. After investigating, you can transfer it to the applicable HR service.The base system provides examples of HR transfer case configuration types. You can also create your own.You can reclassify an HR case that you originally create under one HR service but want to move it under a different HR service.
locale: en-US
release: australia
product: HR Service Delivery
classification: hr-service-delivery
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Use HR Case Management, Case and Knowledge Management, HR Service Delivery, Employee Service Management]
---

# Transfer an HR case

You can create and use methods to reclassify or transfer an opened HR case from one HR service to another. Oftentimes an HR case opens as a General Benefits Inquiry. After investigating, you can transfer it to the applicable HR service.

You can configure different transfer case scenarios. There are two \(2\) methods you can use to transfer an HR case created with an HR service to another HR case with a different HR service.

The base system provides:

-   Reclassify:
    -   The HR case number does not change after transferring an HR case from one HR service to another.
    -   Links redirect to the new case for the following users:
        -   Opened for: Person that the HR request was opened for.
        -   Subject person: Person that is the subject of the HR request.
    -   Notification emails are not sent for reclassification cases.
-   Standard:
    -   The HR case number changes when transferring an HR case from one HR service to another. Both HR case numbers appear on the HR case for reference.
    -   Links do not redirect from original case to new case.
    -   The subject person receives a notification email with the closed case and transferred case information.
-   Common to both Reclassify and Standard:
    -   Fields from the current case are copied and moved to the new case.

        **Note:** The sn\_hr\_core.transfer\_case.ignored\_fields sys property can be set with fields that are not copied in an HR case transfer.

    -   Work notes copy from original case to new case.
    -   Attachments are copied and moved from the current case to the new case.
    -   Previous interaction records from the current case are copied and moved to the new case.
-   Sys property:

    The sn\_hr\_core.reclassify\_default\_transfer sys property determines the default method to use after upgrade. For more information, see [HR properties](../task/t_HRProperties.md).


**Parent Topic:**[Use HR Case Management](c_HRCaseManagement.md)

## Configure HR transfer case

The base system provides examples of HR transfer case configuration types. You can also create your own.

### Before you begin

Role required: sn\_hr\_core.admin

### About this task

If you are creating a transfer case configuration, you must also create a script include to implement the sn\_hr\_core HR case transfer extension point. For more information, see [Registering custom script includes against the scripted extension points](https://www.servicenow.com/docs/access?context=impl-scripted-ext-pts-base-code&version=australia&pubname=australia-api-reference&ft:locale=en-US).

Refer to the existing script includes as examples:

-   hr\_TransferCase
-   ReclassifyCaseTransfer
-   StandardCaseTransfer

The hr\_TransferCase script include provides a list of fields ignored in the transfer and acts as a utility for the other two script includes.

**Note:** Refer to [Script includes](https://www.servicenow.com/docs/access?context=c_ScriptIncludes&version=australia&pubname=australia-api-reference&ft:locale=en-US).

### Procedure

1.  Navigate to **All** &gt; **HR Administration** &gt; **Transfer Case Configuration**.

2.  Select **New**.

3.  Fill in the form.

<table id="table_o31_kh1_nhb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

The name of the HR case transfer type.The defaults are:

-   Reclassify
-   Standard


</td></tr><tr><td>

Display text

</td><td>

The HR case transfer type that appears on the Transfer Case menu from the HR case form. The defaults are:-   Transfer with existing case number
-   Transfer to a new case number


</td></tr><tr><td>

HR criteria

</td><td>

Defines what HR agents can view and use this transfer type when performing an HR case transfer from the HR case form.See [HR criteria](hr-criteria.md#).

**Note:** When defining conditions like case sensitivity or null values, see API [GlideFilter - Scoped, Global](https://www.servicenow.com/docs/access?context=c_GlideFilterScopedAPI&version=australia&pubname=australia-api-reference&ft:locale=en-US).

</td></tr><tr><td>

Is default

</td><td>

Indicates that the transfer type is the default and appears first in the Transfer Case menu from the HR case form.**Note:** To mark a transfer type as the default, click the **Set as Default** button at the bottom.

</td></tr><tr><td>

Active

</td><td>

Indicates if the HR case transfer type is active and available for use. Inactive indicates that the transfer type does not appear in the Transfer Case menu from the HR case form.

</td></tr></tbody>
</table>4.  Select **Submit** or **Update**.


## Move an HR case from one HR service to another

You can reclassify an HR case that you originally create under one HR service but want to move it under a different HR service.

### Before you begin

Role required: sn\_hr\_core.case\_writer

### About this task

You can also retain the details of the original case. For example, you can take a General Inquiry case and reclassify it as a Medical Benefits Inquiry case.

### Procedure

1.  Open an existing HR case.

2.  From **Additional actions**, select **Transfer Case**.

3.  From **Transfer type**:

    -   **Transfer with existing case number**: The HR case number does not change, links redirect with new case, and work notes transfer to new case.
    -   **Transfer to a new case number**: The HR case number changes, links do not redirect, and work notes do not transfer. Both HR case numbers appear on the HR case for reference.
4.  From **New HR Service**, select the HR service you want to assign to your original case.

5.  Select **OK**.

    The current case and its child tasks close. When you transfer an HR case from one HR service to another, some field values do not transfer to the new case. The Opened for person receives a notification email with the closed case and transferred case information. Replies to the email appear in the Comments section of the HR case. If the subject person replies to the email associated with the closed case, the reply appears in the comments for both the closed and transferred cases.

    **Note:** If the sn\_hr\_core.restrict\_guest\_email system property is False \(default\), text from an email appears in the Work notes field when the employee is responding from a personal email account.

    See [Email setup](https://www.servicenow.com/docs/access?context=c_EmailConfiguration&version=australia&pubname=australia-platform-administration&ft:locale=en-US).


