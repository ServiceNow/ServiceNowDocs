---
title: Configure user criteria for a service definition
description: After creating a service definition, configure user-specific criteria to control which users can access and use that service definition to create a case.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring service definitions, Service definitions, Case management, Organize agent workspaces, Configure, Customer Service Management]
---

# Configure user criteria for a service definition

After creating a service definition, configure user-specific criteria to control which users can access and use that service definition to create a case.

## Before you begin

Role required: admin, sn\_csm\_case\_types.service\_definition\_admin, or sn\_csm\_case\_types.service\_definition\_manager

## About this task

You can associate user-specific criteria such as role, assignment group, or specific user with a service definition to determine which users can access and use that service to create a case.

For example, you can configure user criteria for service definitions like Product Recall or New Product Launch in Store so that only regional managers or operational managers in designated groups can use those services to create cases.

## Procedure

1.  Navigate to **All** &gt; **Customer Service** &gt; **Administration** &gt; **Service Definitions**.

2.  Select a service definition.

3.  In the Service Definition User Criteria related list, select **New**.

    The system displays a new Service Definition User Criteria record. The **Service definition** field is auto-filled with the name of the selected service definition.

4.  In the **User criteria** field, select a user criteria record.

    These records are stored in the User Criteria \[user\_criteria\] table.

    You can also create a user criteria record by selecting **New** on the User Criteria pop-up window and filling in the fields on the User Criteria form.

    For more information about the fields on this form, see [User criteria form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-reservation-management/user-criteria-form.md).

5.  Enable the **Active** check box.

6.  Select **Submit**.


