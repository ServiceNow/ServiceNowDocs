---
title: Defining and setting for employee documents
description: Use Employee Document Management to configure how employee documents should be handled based on company policy, processes, and regulatory compliance.For each document type, you can determine who can access a document as well as define the retention policies associated with it, or place a legal hold. A document type can manage multiple documents.A retention period defines how long an employee document should be saved before being discarded. Retention periods are combined with conditions or criteria to form a retention policy.Default retention policies ensure that employee documents are not mistakenly purged. When a retention policy has not been assigned to a document type, the default retention policy is used.Set policies determining how long documents should be retained and who is covered. Retention policies combine the retention period and conditions or criteria.Default security policies ensure that employee documents are secure. The HR Service Delivery base system provides default security policies for each document type and determines who can access and has purge authorization.Many employee documents contain confidential and personal information. Use document security policies to define access to employee documents and ensure that they are secure.Add or modify expiration notification policies on a document type. Allow setting an expiration date on a document and sending email notifications to document owners, managers, or HR representatives when the document expires or nearing its expiration.
locale: en-US
release: australia
product: Employee Document Management
classification: employee-document-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 15
breadcrumb: [Configuring Employee Document Management, Employee Document Management, HR Documents, HR Service Delivery, Employee Service Management]
---

# Defining and setting for employee documents

Use Employee Document Management to configure how employee documents should be handled based on company policy, processes, and regulatory compliance.

## Document types

Document types are at the center of the Employee Document Management application. All employee documents are required to have a document type assigned. Categorize your employee documents by assigning document types. Use document types to combine policies that determine handling of an employee document. Use document types to:

-   Associate a security policy. Security policies determine who can access employee documents and determine purge authorization.
-   Associate a retention policy. Retention policies determine how long to keep a document and who the document is applicable to.
-   Place a legal hold. Legal holds temporarily prevent document purging or changes to the document.
-   Allow access to employees.
-   Configure employee documents to be moved automatically when an HR case is closed. See [Configure an HR service](../task/configure-hr-service.md).

![How document types pull together topic detail, security policy, retention policy and expiration policy.](../image/doc-type.png)

**Parent Topic:**[Configuring Employee Document Management](configuring-employee-document-management.md)

**Related topics**  


[Activate Employee Document Management](../task/activate-employee-doc-mgmnt.md#)

## Define policies for a document type

For each document type, you can determine who can access a document as well as define the retention policies associated with it, or place a legal hold. A document type can manage multiple documents.

### Before you begin

Role required: sn\_hr\_ef.manager

### About this task

Document types combine topic detail, retention policies, and legal holds. The default retention period for a document type is defined on the corresponding Center of Excellence \(COE\). For details on COEs, see [HR Centers of Excellence data model](hr-centers-of-excellence-coes.md).

**Note:** The base system provides various document types as examples.

### Procedure

1.  Navigate to **All** &gt; **HR Administration** &gt; **Employee Documents** &gt; **Document Types**.

2.  Click **New** or an existing document type to edit.

3.  Fill in the fields as appropriate.

<table id="table_xpw_rbf_d2b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name that describes the document type.

</td></tr><tr><td>

Topic detail

</td><td>

Topic detail associated with an HR service. The topic detail categorizes the document type.

 The HR service can be used to automatically move employee documents to the employee document repository when an HR case is closed.

</td></tr><tr><td>

Active

</td><td>

Option for activating or deactivating a document type. On deactivating a document type, the document type does not appear for selection when creating a document or moving attachments.

</td></tr><tr><td>

Application type

</td><td>

Application associated with the document type.

</td></tr><tr><td>

Legal hold

</td><td>

Indicates if a legal hold has been placed on the document type. When checked, all employee documents with this document type are placed on legal hold.

</td></tr><tr><td>

Employee access

</td><td>

Enables employees to access their own employee documents.

</td></tr><tr><td>

Expiration date

</td><td>

Option to set expiration date on a document. Email notifications will be sent to document owners, managers, or HR representatives \(as per expiration policies\) when the document expires or nearing its expiration.

</td></tr></tbody>
</table>4.  From the Context Menu, click **Save** to remain on the Document Type form.

    The following tabs appear.

<table id="table_pt3_g5l_dfb"><thead><tr><th>

Tab

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Security Policies

</td><td>

Security policy associated with the document type. Security policies grant authorized users the ability to view, create, move, or authorization to purge employee documents.When you select a topic detail, the default security policy associated with that topic detail \(if any\) is automatically displayed in the **Security Policies** tab.

 In the **Security Policies** tab, you can,

-   Add and associate multiple security policies to a document type.
-   Define an order in which a security policy must be evaluated. Lower numbers are placed ahead of higher numbers. For example, a security policy with an order set to 100 is evaluated before a security policy with an order set to 200.
-   Enable or disable a security policy. When you disable a security policy, it implies that a security policy will be associated with the document type, but will not be considered for evaluation.


</td></tr><tr><td>

Retention Policies

</td><td>

Retention policy associated with the document type.The retention policy combines the retention period \(determines how long a document should be saved\) and HR criteria \(filters who the policy is applicable to\).

 See [Add or modify a retention policy](hr-doc-management-config.md#).

</td></tr><tr><td>

Legal Holds

</td><td>

Shows any legal holds placed on the document type with reason, date, and time stamps.

</td></tr><tr><td>

Expiration Policies

</td><td>

Expiration policies enable an administrator to filter documents of a document type based on HR criteria or on fields of employee document table or as a combination. It also enables an administrator to configure groups or recipients that could receive email notifications when document expires or nears its expiration.

</td></tr></tbody>
</table>5.  After adding or editing the retention policy, click **Save** to remain on the Document Type form or click **Submit** to return to the Document Type list.


## Define how long to retain employee documents

A retention period defines how long an employee document should be saved before being discarded. Retention periods are combined with conditions or criteria to form a retention policy.

### Before you begin

Role required: sn\_hr\_ef.manager

**Note:** Retention periods are unique and cannot be duplicated. Before you can delete a retention period, you must be sure that a document type is not associated with the retention policy.

### Procedure

1.  Navigate to **All** &gt; **HR Administration** &gt; **Employee Documents** &gt; **Retention Periods**.

2.  Fill in the fields as appropriate.

<table id="table_ibk_b4f_d2b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Title

</td><td>

Name that describes the retention period.

</td></tr><tr><td>

Date field

</td><td>

Starting point of the retention period. The fields that are available depend on the Employee Document \[sn\_hr\_ef\_employee\_document\] table. Fields from the Employee Document \[sn\_hr\_ef\_employee\_document\] table used to define the beginning of the retention period.

 Dot-walk and select a field to determine the starting point of the retention period.

</td></tr><tr><td>

Application type

</td><td>

Application associated with the retention period.

</td></tr><tr><td>

Date offset type

</td><td>

Offset that determines if the retention period should start before or after what was selected in the **Date field**.Combined with the **Date field**, **Date offset units**, and **Date offset quantity** determines the length of the retention period.

 For example:

-   Date field = Created
-   Date offset type = After
-   Date offset units = Years
-   Date offset quantity = 1
Using this configuration, the retention period is one year after the created date of the document.

</td></tr><tr><td>

Date offset units

</td><td>

Unit of time that determines if the retention period should be measured in months or years.

</td></tr><tr><td>

Date offset quantity

</td><td>

Number of months or years before or after the **Date field** selection.

</td></tr></tbody>
</table>3.  Click **Submit** or **Update**.


## Add or modify default retention policies

Default retention policies ensure that employee documents are not mistakenly purged. When a retention policy has not been assigned to a document type, the default retention policy is used.

### Before you begin

Role required: sn\_hr\_ef.manager

### About this task

You can edit default retention policies.

The HR Service Delivery base system provides default retention policies for each employee document associated with a Center or Excellence \(COE\) table.

Default retention policies are assigned to all documents that fall under a COE and the retention period is indefinite and never purged.

**Note:** If you change the default retention period, all new documents are assigned the new period, but existing documents still use the original retention period.

Default retention policies cannot be deleted when being used by a document type. Only one default policy for a COE is allowed.

Once a purge date is calculated and a legal hold is placed, the purge date does not change.

### Procedure

1.  Navigate to **All** &gt; **HR Administration** &gt; **Employee Documents** &gt; **Default Retention Policies**.

2.  Click **New** to create a default retention policy or on an existing policy to edit.

3.  Fill in the fields as appropriate.

<table id="table_b3h_dnf_d2b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Table

</td><td>

COE table employee documents are associated with when the HR Service Delivery is licensed and activated.

</td></tr><tr><td>

Retention period

</td><td>

Retention period identifying how long the document is retained.The only field you can edit.

</td></tr><tr><td>

Application type

</td><td>

Application associated with the default retention policy.

</td></tr></tbody>
</table>4.  Click **Submit** or **Update**.


## Add or modify a retention policy

Set policies determining how long documents should be retained and who is covered. Retention policies combine the retention period and conditions or criteria.

### Before you begin

Role required: sn\_hr\_ef.manager

### About this task

Regulations, laws, and your company policies determine how long documents should be retained.

Once a purge date is calculated and a legal hold is placed, the purge date does not change.

To ensure that there are no accidental purging, the base system provides default retention policies. When a retention policy has not been assigned to a document type, the default retention policy is used.

When a document type is covered by multiple retention policies:

-   The policy with the longest retention period applies.
-   When there is a non-default default retention policy and a default retention policy with a retention period of indefinite, the non-default retention policy applies. Assuming the HR criteria matches and the retention period is applicable.

Retention policies have a one-to-one relationship to a document type, you cannot have the same retention policy for multiple document types.

**Note:** You can use the same retention period for multiple retention policies.

When you have multiple retention policies, but there is an overlap in criteria, the retention policy with the longest retention period is used.

For example: Document type = Disciplinary Notice

-   Retention policies:
    -   US employees \(retention period = End Date + 7 years\)
    -   US contract employees \(retention period = End Date + 5 years\)
-   If a user is both a US employee and contract employee, the US employees retention policy is used because it has a longer retention period.

**Note:** You can use the default retention policy for all document types. The default retention policy defines that all employee documents are retained while an employee is a current employee of your company. Once an employee leaves the company, a second retention policy is triggered based on HR criteria. When an employee does not satisfy the HR criteria and leaves the company, the original default retention policy is still in effect. The employee documents are retained indefinitely.

### Procedure

1.  Navigate to **All** &gt; **HR Administration** &gt; **Employee Documents** &gt; **Retention Policies**.

2.  Click **New** or an existing retention policy to edit.

3.  Fill in the fields as appropriate.

<table id="table_zwx_ppf_d2b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Applies to

</td><td>

Employee Document \[sn\_hr\_ef\_employee\_document\] table and document type associated with the retention policy.Select a table and document type the retention policy is based on.

</td></tr><tr><td>

HR criteria

</td><td>

Who the retention policy applies to. For example, you can select HR criteria based on a country. This criteria ensures everyone based in the selected country has the same retention policy.

**Note:** When defining conditions like case sensitivity or null values, see API [GlideFilter - Scoped, Global](https://www.servicenow.com/docs/access?context=c_GlideFilterScopedAPI&version=australia&pubname=australia-api-reference&ft:locale=en-US).

</td></tr><tr><td>

Retention period

</td><td>

How long an employee document should be saved.

</td></tr><tr><td>

Active

</td><td>

Indicates if the retention policy is active and in use.**Note:** Default retention policies cannot be deactivated.

</td></tr></tbody>
</table>4.  Click **Submit** or **Update**.


## Add or modify default security policies

Default security policies ensure that employee documents are secure. The HR Service Delivery base system provides default security policies for each document type and determines who can access and has purge authorization.

### Before you begin

Role required: sn\_hr\_ef.manager

Users are granted access to employee documents by:

-   Groups
-   Roles
-   Both groups and roles

The security policy can require authorization to purge and requires a user to belong to the group that has purge authorization.

See [Manage HR Groups](../task/t_ManageHRGroups.md) and [Manage HR roles](c_ManageRoles.md).

### Procedure

1.  Navigate to **All** &gt; **HR Administration** &gt; **Employee Documents** &gt; **Default Security Policies**.

2.  Click **New** or an existing default security policy to edit.

3.  Fill in the fields as appropriate.

<table id="table_izc_grh_2fb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Description

</td><td>

Phrase that describes the HR employee document security policy.

</td></tr><tr><td>

Application type

</td><td>

Application associated with the security policy.

</td></tr><tr><td>

Active

</td><td>

Option for enabling or disabling the security policy. When you disable a security policy, it implies that the security policy will be associated with the document type, but will not be considered for evaluation.

</td></tr><tr><td>

Applies when

</td><td>

Filters defining additional conditions on a security policy.

</td></tr></tbody>
</table>4.  Click **Submit** or **Update**.


## Add or modify document security policies

Many employee documents contain confidential and personal information. Use document security policies to define access to employee documents and ensure that they are secure.

### Before you begin

Role required: sn\_hr\_ef.admin

### About this task

You can determine who can read, write, or authorize purging of documents by adding or modifying document security policies.

**Note:** You can provide employees visibility into their own employee documents through their HR profile. Check the **Employee access** box on the **Document type** form. See [Define policies for a document type](hr-doc-management-config.md#).

Users are granted access to employee documents by:

-   Groups
-   Roles
-   Both groups and roles

The security policy can require authorization to purge and requires a user to belong to a group that has purge authorization.

See [Manage HR Groups](../task/t_ManageHRGroups.md) and [Manage HR roles](c_ManageRoles.md). Or see [Groups](../task/t_ManageHRGroups.md) and [Roles](c_ManageRoles.md).

### Procedure

1.  Navigate to **All** &gt; **HR Administration** &gt; **Employee Documents** &gt; **Security Policies**.

2.  Click **New** or an existing security policy to edit.

3.  Fill in the fields as appropriate.

<table id="table_cgc_tlf_d2b"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Description

</td><td>

Phrase that describes the HR employee document security policy.

</td></tr><tr><td>

Application type

</td><td>

Application associated with the security policy.

</td></tr><tr><td>

Active

</td><td>

Option for enabling or disabling the security policy. When you disable a security policy, it implies that the security policy will be associated with the document type, but will not be considered for evaluation.

</td></tr><tr><td>

Applies when

</td><td>

Filters defining additional conditions on a security policy.

</td></tr></tbody>
</table>    Use the three tabs to determine what groups or roles are required to search, access, and edit meta data for an employee document by document type. You can also define what groups receive purge notifications or can authorize purging of employee documents.

<table id="table_vgf_nmf_d2b"><thead><tr><th>

Tabs

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Read

</td><td>

Groups: Groups a user must belong to search and read an employee document with the associated document type and security policy.Roles: Roles a user must have to search and read an employee document with the associated document type and security policy.

**Note:** Users with the Employee Document Management Reader \[sn\_hr\_ef.document\_reader\] role must also be added here to search and read documents associated with the document type and security policy.

 Match all: Determines if both the conditions for groups and roles must be met for access.

**Note:** If you leave unchecked, the user only has to meet conditions from either Groups or Roles, not both.

</td></tr><tr><td>

Write

</td><td>

Groups: The groups a user must belong to access.Roles: Roles a user must have to search, read, and create an employee document with the associated document type and security policy.

 **Note:** Users with the Employee Document Management Writer \[sn\_hr\_ef.document\_writer\] role must also be added here to search, read, and create documents associated with the document type and security policy.

 Match all: Determines if both the conditions for groups and roles must be met for write access.

**Note:** If you leave unchecked, the user only has to meet conditions from either Groups or Roles, not both.

</td></tr><tr><td>

Authorize Purge

</td><td>

Authorization is required to purge documents, or send a notification before the purge process runs.Groups: Group a user must belong to authorize or be notified of an upcoming purge.

**Note:** Only one person in the group is required to authorize.

</td></tr></tbody>
</table>4.  Click **Save** and the **Document Types** related list appears.

5.  Click **New** and you can create a document type to be associated with the security policy.

6.  Click **Submit** or **Update**.


## Add or modify expiration policies on a document type

Add or modify expiration notification policies on a document type. Allow setting an expiration date on a document and sending email notifications to document owners, managers, or HR representatives when the document expires or nearing its expiration.

### Before you begin

Role required: admin

### About this task

Certain documents, such as passports or training certificates, have expiration dates. For organizations to adhere to compliance policies, the latest versions of employee documents are to be maintained. With this feature, an administrator can set up expiration notification policies on a document type and a user can set an expiration date for a document while uploading it to Employee Document Management or when moving a case to Employee Document Management.

### Procedure

1.  Navigate to **All** &gt; **HR Administration** &gt; **Employee Documents** &gt; **Expiration Notification Policies**.

2.  Click **New**.

3.  On the form, fill in the fields:

    |Field|Description|
    |-----|-----------|
    |Document type|Document type on which the expiration policy is set. For example, Education Agreements.|
    |Name|Name that you specify for the expiration notification policy.|
    |Order|Order that you specify for an expiration policy. Assume that a document qualifies two expiration notification policies, then the policy with lesser order is given higher priority.|
    |Active|Option to activate the expiration policy for use.|
    |**Add filter criteria**|
    |HR criteria|HR criteria defines the audience on whom you want to apply filter conditions. For example, US employees: Tax forms collection.|
    |Applies when|Filter conditions that you want to apply on fields of employee document.|
    |Match both|When there is more than one filter condition, enable this option. Documents are filtered based on all conditions specified.|

4.  Click **Submit**.


### What to do next

1.  Navigate to **All** &gt; **HR Administration** &gt; **Employee Documents** &gt; **Expiration Notification Policies**.
2.  Open the required expiration notification policy.
3.  In the **Expiration Notification Recipients** related list, add recipients:

<table id="table_hlz_1nx_nvb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name for the expiration notification recipient.

</td></tr><tr><td>

Data offset type

</td><td>

Date offset type relative to the expiration date of the document. For example, do you want to send a notification before or after the expiration date.

</td></tr><tr><td>

Data offset units

</td><td>

Number of days, weeks, or months that defines your offset units.

</td></tr><tr><td>

Data offset quantity

</td><td>

Value specified for data offset. For example, assume you have selected Data offset type as **Before**, Date offset units as **Days**, and Date offset quantity as **3**, then email notifications will be sent three days before the expiration date of the document.

</td></tr><tr><td>

Expiration notification policy

</td><td>

Expiration notification policy for which recipients are being created.

</td></tr><tr><td>

Recipients

</td><td>

Recipients for notifications could be selected from the fields supported on an employee document.**Note:** If you want to notify different recipients on different days, you can configure multiple expiration notification recipients for a single expiration notification policy.

</td></tr><tr><td>

Active

</td><td>

Option to activate the expiration notification recipient.

</td></tr></tbody>
</table>4.  In the Groups section, add groups to which you want to send notifications. Groups receive notifications at the same time as the recipients.
5.  Click **Submit**.

