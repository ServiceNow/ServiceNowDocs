---
title: Create and manage cases for a business organization
description: As a staff member, create and manage cases for your business organizations \(formerly business locations\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/manage-business-location-cases.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Business Organizations, Configure Service Model Foundation, Data models, Set up your environment, Configure, Customer Service Management]
---

# Create and manage cases for a business organization

As a staff member, create and manage cases for your business organizations \(formerly business locations\).

## Before you begin

Role required: Any one of the following roles:

-   admin
-   sn\_customerservice.svc\_location\_agent
-   sn\_customerservice.svc\_location\_consumer\_agent
-   sn\_customerservice.svc\_location\_manager

## About this task

Staff members with the location agent or location consumer agent role can do the following:

-   View information for the customers at their location.
-   Create cases for:
    -   the accounts, and contacts at their location \(location agent\).
    -   the households, and consumers at their location \(or location consumer agent\).
-   Create consumers.
-   Update cases created at their location.

A case belongs to one business organization \(formerly business location\). When a case is created by a location agent, location consumer or manager, the **Requestor Organization** field on the Case form is automatically updated with the business organization that the agent or manager belongs to. If the case is reassigned, this field is updated to show the new agent or manager.

If the location agent, location consumer agent or manager belongs to multiple locations, the **Requestor Organization** field may be kept empty. When you fill in this field, make your selection carefully because the service organization controls a location agent's access to cases.

The **Requestor Organization** and **Provider Organization** can be set manually for a new case or changed for an existing case. Changing the organization doesn’t change the assigned agent.

Location agents, location consumer agents and managers can create cases for business organizations without adding an account, contact, or consumer. The location agent, location consumer agent or manager who creates the case is added to the **Opened by** field.

**Important:** Some table and field labels have been changed across recent releases. For a mapping of former labels to current labels, see [Service Model Foundation renamed Entities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/renamed-entities.md).

## Procedure

1.  Navigate to **All** &gt; **Customer Service** &gt; **Cases** and select **Create New**.

2.  Select the type of case that you want to create.

3.  On the form, fill in the fields.

    For a description of the field values, see [Case form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/r_CustomerServiceCaseForm.md).

4.  Select **Submit**.

5.  Perform the following tasks on a case:

    -   Assign a case to yourself by selecting the **Assign to me** button on the Case form and resolve cases assigned to your organization.
    -   Add comments and work notes, and follow the standard case resolution flow, including:
        -   Propose a solution by selecting the **Propose solution** button.
        -   Close cases by selecting the **Close Case** button.
    -   Create and update case tasks by selecting the **New** button from the Tasks related tabs.
    -   View task SLAs, Appointments, Email, Attached Knowledge, Knowledge Gaps Escalations, and Affected install base items on accessible cases.
    -   Read published knowledge articles and raise knowledge feedback from the Attached Knowledge related tab.
    -   Related cases can be accessed from the related search results on the case.

**Related topics**  


[Service Model Foundation cases](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/industry-data-model-cases.md)

[Assign responsibilities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/csm-assign-responsibilities.md)

[Assign roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/configure-data-model-roles.md)

[Create a customer service case](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/t_CreateACaseFromCustServApp.md)

