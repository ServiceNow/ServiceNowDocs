---
title: Assign a partner contact on the case form
description: Enable Customer Service Management agents to assign partner contacts for an account that is associated to an install base item on the case form. By adding partner contacts, you can provide access to multiple partners to access their accounts.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/assign-a-partner-contact-case-form.html
release: australia
product: Customer Service Management
classification: customer-service-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Case form, Customer Service forms, Reference, Customer Service Management]
---

# Assign a partner contact on the case form

Enable Customer Service Management agents to assign partner contacts for an account that is associated to an install base item on the case form. By adding partner contacts, you can provide access to multiple partners to access their accounts.

## Before you begin

Role required: customer service agent

## Procedure

1.  Navigate to **CSM/FSM Configurable Workspace** &gt; **Cases** &gt; **My Cases**.

2.  Select **New**.

3.  In the **Install Base** field, use the search icon \[Omitted image "search\_icon.png"\] Alt text: Search icon. to add an install base item on the Create Case form.

    The **Account** and **Contact** fields are automatically filled from the install base form. For a description of the field values, see [Case task form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/csm-case-task-form.md).

4.  In the **Partner** field, use the search icon to \[Omitted image "search\_icon.png"\] Alt text: Search icon. search for a partner associated with the selected account.

    The partner in the **Partner** field is the partner account that is associated with the account.

5.  In the **Partner Contact** field, enter an eligible partner contact who has the following criteria:

    -   All partner contacts of the partner account are eligible if the **Restrict Account Access** isn't enabled.
    -   All partner contacts with the partner admin role are eligible if **Restrict Account Access** is enabled.
    -   Partner contacts that are added as an Authorized Representative through the related party list for the install base item.
    -   Partner contacts that are added as an Authorized Account through the related party list for the install base item.
    To add a related party to an install base item, see [Add related parties to an install base item](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/add-related-party-install-base.md).

6.  Select **Submit**.


## Result

A partner contact is assigned to the case.

