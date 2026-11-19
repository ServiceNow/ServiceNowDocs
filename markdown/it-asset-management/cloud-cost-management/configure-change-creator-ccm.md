---
title: Configure a change creator user for Cloud Cost Management
description: Create and configure a change creator user so that the Cloud Cost Management application can create change requests on behalf of the insights\_admin or insights\_owner.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-asset-management/cloud-cost-management/configure-change-creator-ccm.html
release: zurich
product: Cloud Cost Management
classification: cloud-cost-management
topic_type: task
last_updated: "2026-08-14"
reading_time_minutes: 1
breadcrumb: [Configure, Cloud Cost Management, IT Asset Management]
---

# Configure a change creator user for Cloud Cost Management

Create and configure a change creator user so that the Cloud Cost Management application can create change requests on behalf of the insights\_admin or insights\_owner.

## Before you begin

Role required: admin

## About this task

A change creator user is configured as an internal integration user and should be assigned the sn\_change\_write role. With this role assignment, this change creator user can create change requests while scheduling recommendations for unused resources, business hours, and rightsizing.

## Procedure

1.  Create a ServiceNow user for internal use by navigating to **All** &gt; **System Security** &gt; **Users**.

2.  Select **New**.

3.  On the User form, fill in the required details for the user such as user ID, first name, last name, email, and password.

    \[Omitted image "create-internal-user-ccm.png"\] Alt text: User form to create an internal user in ServiceNow

4.  Select the **Internal Integration User** and **Web service access only** options.

    If you don't see the **Web service access only** option on the form, you can personalize and add it from the list view.

5.  Select **Submit**.

    The user record is created.

6.  Open the record and select the **Roles** tab.

7.  Assign these roles to the internal user.

    -   **catalog**
    -   **rest\_service**
    -   **sn\_change\_write**
8.  Create a credential record for this user by navigating to **All** &gt; **Http Basic Auth Credentials**.

9.  On the Basic Auth Credentials page, select **New**.

10. On the Basic Auth Credentials form, provide the name, user name, and password in the respective fields.

    You must enter the same user name and password that you entered while creating the user.

11. In the **Credential alias** field, search for and select `sn_clin_core.clin_change_creator`.

    sn\_clin\_core.clin\_change\_creator is the default credential alias shipped with Cloud Cost Management.

12. Select **Submit**.

    The internal user is mapped to the default credential alias.


