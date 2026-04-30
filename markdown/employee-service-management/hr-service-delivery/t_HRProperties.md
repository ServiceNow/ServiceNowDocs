---
title: HR properties
description: HR properties control the behavior of HR Service Delivery.
locale: en-US
release: yokohama
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [HR Administration, Case and Knowledge Management, HR Service Delivery, Employee Service Management]
---

# HR properties

HR properties control the behavior of HR Service Delivery.

## Before you begin

Role required: sn\_hr\_core.admin

## Procedure

1.  Navigate to **All** &gt; **HR Administration** &gt; **Properties**.

    Some HR properties are found under **sys\_properties.list**.

2.  Configure the HR properties, as appropriate.

<table id="table_h44_tnx_5r"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr id="tablerow_assign_method_requests"><td>

sn\_hr\_core.hr\_profile\_default\_fields

</td><td>

Fields that appear on the Generate HR Profiles page. You can add fields from the sn\_hr\_core\_profile column, but use commas to separate the fields.

</td></tr><tr><td>

sn\_hr\_core.hr\_email

</td><td>

Enter the default email address for general HR inquiries.

</td></tr><tr><td>

sn\_hr\_core.hr\_phone

</td><td>

Enter the default phone number for general HR inquiries.

</td></tr><tr><td>

sn\_hr\_core.hr\_profile\_editable\_fields

</td><td>

Fields that users can edit themselves about their employee profile.

</td></tr><tr><td>

sn\_hr\_core.profile.max.tries

</td><td>

The maximum number of attempts allowed before the application exits when creating a user.

</td></tr><tr><td>

sn\_hr\_core.hr\_vip\_default\_priority

</td><td>

The default priority on cases that the **Opened for** and/or **Subject person** is tagged as a VIP.

</td></tr><tr><td>

sn\_hr\_core.impersonateCheck

</td><td>

Check **Yes** \(true\) to prevent any user impersonating another user from viewing HR information.**Note:** Even if the logged in user has HR access and impersonates another HR user with the same access, HR information is not visible.

</td></tr><tr><td>

com.snc.signaturepad.retrieveSignature

</td><td>

Check **Yes** to enable signature retrieval and allowing users to save their digital signatures for reuse. If true, retrieves the latest signature image for a user and show it by default when the user navigates to the signature pad.

</td></tr><tr><td>

sn\_hr\_core.log

</td><td>

The level of detail for system logs. The valid values are:-   Info: Least amount of detail
-   Warn: Default
-   Debug: Most amount of detail


</td></tr><tr><td>

sn\_hr\_core.rollup\_work\_notes

</td><td>

Check **Yes** to have work notes from a task also appear on the case.

</td></tr><tr><td>

sn\_hr\_core.duplicate\_hr\_case\_time\_out

</td><td>

The number of days that must pass before a duplicate case warning appears when an HR case is created for the same HR service and subject person in HR Agent Workspace.The base system value is three \(3\) days.

 For example, if an agent creates an HR case for a General Benefits Inquiry \(HR service\) for Abel Tuter and another General Benefits case is created in HR Agent Workspace within three days, a message appears notifying the user of a potential duplicate case. A list of similar cases also appears. The agent can continue to create a new case or cancel.

**Note:** This property only affects possible duplicate HR cases for the same HR service and subject person in HR Agent Workspace. For more information, see [Receiving a duplicate case warning with HR Service Delivery Agent Workspace](../concept/agent-ws-hr-dup-case.md).

</td></tr><tr><td>

sn\_hr\_core.inbound\_email

</td><td>

This parameter determines if an email to HR is converted into an HR case.-   Yes: Create an HR case from email.
-   No: Do not create an HR case from email.


</td></tr><tr><td>

sn\_hr\_core.sync.exclusion\_fields.profile

</td><td>

Specifies which fields on the HR profile \(sn\_hr\_core\_profile\) table you don't want to synchronize with the User \(sys\_user\) table.For example, specify fields that should not be overwritten as they are already synchronized with an external application.

</td></tr><tr><td>

sn\_hr\_core.sync.exclusion\_fields.sys\_user

</td><td>

Specifies which fields on the User \(sys\_user\) table you don't want to synchronize with the HR profile \(sn\_hr\_core\_profile\) table \(as a comma separated list\).For example, specify fields that should not be overwritten as they are already synchronized with an external application.

</td></tr><tr><td>

sn\_hr\_core.itext7.pdf\_conversion

</td><td>

Activate this property to use the iText7 for your document templates for PDF conversion, pre-fill values, and merge signatures into your documents.

</td></tr><tr><td>

sn\_hr\_core.reclassify\_default\_transfer

</td><td>

Determines how you want your instance to behave when you transfer an HR case to another case after an upgrade.Valid entries:

-   true: Use the default transfer case to use the standard method. The HR case number changes when transferring an HR case from one HR service to another. Both HR case numbers appear on the HR case for reference.
-   false: Use the reclassify method to transfer an HR case. The HR case number does not change after transferring an HR case from one HR service to another.
**Note:** For more information, see [Transfer an HR case](../concept/reclassify-hr-case.md).

</td></tr><tr><td>

sn\_hr\_core.include\_elevated\_roles

</td><td>

Checks for logged in users that have roles with elevated privilege before granting access. Valid entries:-   true: Check if logged in user has role with elevated privilege before granting access.
-   false: Do not check if logged in user has role with elevated privilege before granting access.


</td></tr><tr><td>

sn\_hr\_core.restrict\_query.limit\_inactive

</td><td>

Limits access to cases, through inactive tasks, based on a time limit in months. If the property is left empty, there will be no limit on the cases that are displayed. The default value to **12**. Depending on your business requirements, you can set this property to a value lesser than 12 months. This might improve the performance experience of your instance.

**Note:** You might not get a benefit out of this property in one of the following cases:

-   Property is unavailable in the system.
-   Property is left empty.
-   Property is set to a positive value, but the number of inactive case tasks within the time limit is large.


</td></tr></tbody>
</table>3.  Click **Save**.


**Parent Topic:**[HR Administration](../concept/c_AdministerHRServiceManagement.md)

