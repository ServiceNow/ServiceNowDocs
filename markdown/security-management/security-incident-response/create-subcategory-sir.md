---
title: Create a security incident subcategory
description: Create subcategories for a category for a deeper classification of a security incident in Security Incident Response Workspace.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Category management in Security Incident Response, Configure, Security Incident Response Workspace, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Create a security incident subcategory

Create subcategories for a category for a deeper classification of a security incident in Security Incident Response Workspace.

## Before you begin

Role required: sn\_si.admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Security Incident Response Workspaces** &gt; **Administration**.

2.  Navigate to **Category Management** &gt; **Subcategory**.

3.  On the Subcategory page, select **New**.

4.  On the form, fill in the fields.

    **Note:** The **Table**, **Element**, and **Language** fields are automatically set to the values for the current user.

    |Field|Description|
    |-----|-----------|
    |Sequence|Controls the display order of this subcategory within the **Subcategory** field of the security incident's **Details** tab. Lower sequence numbers appear first.|
    |Inactive|Option for making the subcategory inactive.|
    |Label|Name for the subcategory to display in the **Subcategory** field of the security incident's **Details** tab. For example, `Worm, virus, Trojan`.|
    |Value|The value written to the database record when a user selects this subcategory.|
    |Dependent value|The category value to which this subcategory belongs.|
    |Hint|An optional brief description for this subcategory to identify its usage.|

5.  Select **Save**.


## Result

The newly created subcategory is saved and appears on the Subcategory page.

**Parent Topic:**[Category management in Security Incident Response](../concept/category-management-sir.md)

**Related topics**  


[Create a security incident category](create-category-sir.md)

