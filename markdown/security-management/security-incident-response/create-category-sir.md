---
title: Create a security incident category
description: Create a security incident category to use to classify security incidents in Security Incident Response Workspace.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Category management in Security Incident Response, Configure, Security Incident Response Workspace, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Create a security incident category

Create a security incident category to use to classify security incidents in Security Incident Response Workspace.

## Before you begin

Role required: sn\_si.admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Security Incident Response Workspaces** &gt; **Administration**.

2.  Navigate to **Category Management** &gt; **Category**.

3.  On the Category page, select **New**.

4.  On the form, fill in the fields.

    **Note:** The **Table**, **Element**, and **Language** fields are automatically set to the values for the current user.

    |Field|Description|
    |-----|-----------|
    |Sequence|Controls the display order of this category within the **Category** field of the security incident's **Details** tab. Lower sequence numbers appear first.|
    |Inactive|Option for making the category inactive.|
    |Label|Name for the category to display in the **Category** field of the security incident's **Details** tab. For example, Confidential personal identity data exposure.|
    |Value|A integer or string value corresponding to the label field. When you select a label, this value is stored in the database.|
    |Dependent value|Any fields on which the category is dependent \(Optional\)|
    |Hint|An optional brief description for this category to identify its usage. For example, `This category is for an security incident with confidential personal identity data exposure.`|

5.  Select **Save**.

6.  Create a subcategory.

    1.  Navigate to **Category Management** &gt; **SubCategory**.

    2.  Repeat the steps for creating a category.

    3.  Select **Save**.


## Result

The newly created category is saved and appears on the Category page.

**Parent Topic:**[Category management in Security Incident Response](../concept/category-management-sir.md)

**Related topics**  


[Create a security incident subcategory](create-subcategory-sir.md)

