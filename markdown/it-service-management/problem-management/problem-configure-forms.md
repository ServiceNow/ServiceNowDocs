---
title: Configure the problem form
description: Configure the problem form layout to conform to the workflow and the process of your organization. Add, remove, and customize fields and related lists, create problem categories, and modify links as needed.
locale: en-US
release: yokohama
product: Problem Management
classification: problem-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Configuring Problem Management, Problem Management, IT Service Management]
---

# Configure the problem form

Configure the problem form layout to conform to the workflow and the process of your organization. Add, remove, and customize fields and related lists, create problem categories, and modify links as needed.

## Before you begin

Role required: admin

## About this task

The Problem form in the base system is configured to follow recommended ITIL practices. Evaluate the form layout and design with your existing business processes, and plan the changes to make.

For additional form customization not described in this page, such as adding company-specific annotations or configuring related lists, see [Form administration](https://www.servicenow.com/docs/access?context=form-administration&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US) and [Configuring the form layout](https://www.servicenow.com/docs/access?context=configure-form-layout&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

By default, auditing is enabled for the problem table. The administrator can configure the form layout to add the Audit Records and Audit History related lists. For more information about options for auditing a table, see [Enable auditing for a table](https://www.servicenow.com/docs/access?context=t_EnableAuditingForATable&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).

## Procedure

-   Navigate to **Problem** &gt; **Create New**.

    Some of the following configuration activities are not accessed from within the problem form. These activities are noted in the procedure.


-   **[Configure the problem form layout](configure-problem-form-layout.md)**  
Configure the problem form so the information it collects is relevant to your organization's processes. You can easily modify the form to show only the fields, related lists, and other elements that you need.
-   **[Add a field in the assess mandatory field dialog](add-field-in-assess-dialog-form.md)**  
Add the mandatory fields necessary to move a problem or a problem task record from the **New** state to the **Assess** state in the assess dialog form. If you miss filling any of the fields, you can always fill those in the assess dialog form.
-   **[Redesign the problem form](design-problem-form.md)**  
The form designer allows you to customize elements in the problem form to create different form views, display a field navigator, or provide field properties.
-   **[Configure problem categories](configure-problem-categories.md)**  
Configure problem categories to provide a refined way of monitoring and reporting problems. Add to or remove category and subcategory choices from the list of problem categories or subcategories.

**Parent Topic:**[Configuring Problem Management](../concept/configuring-problem-mgmt.md)

**Previous topic:**[Activate Problem Management — ATF Tests](activate-problem-mgmt-atf-tests.md)

**Next topic:**[Configure the problem form layout](configure-problem-form-layout.md)

