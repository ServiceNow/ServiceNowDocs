---
title: Configure a practice area table
description: Configure a practice area table so you can use fields from legal request and legal matter tables to include in the Lists section of Legal Counsel Center.
locale: en-US
release: australia
product: Legal Request Management
classification: legal-request-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Legal Request Management, Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# Configure a practice area table

Configure a practice area table so you can use fields from legal request and legal matter tables to include in the Lists section of Legal Counsel Center.

## Before you begin

Role required: admin

## About this task

The record producer uses variables to store field information submitted via intake forms for a legal request or legal matter. If you have to use any of these variables as columns in the list view in Legal Counsel Center, you must add them as columns in the respective practice area tables. These practice area tables extend the Legal Request \[sn\_lgs\_ops\_request\] table for legal requests and the Legal Matter \[sn\_lg\_matter\_matter\] table for legal matters. For more information, see [Practice area tables for legal requests](../reference/legal-request-pa-tables.md) and [Practice area tables for legal matters](../../legal-matter-management/reference/legal-matter-pa-tables.md).

**Note:** For using practice area tables for legal matters, you must have the Legal Matter Management installed.

## Procedure

1.  Add new columns in a practice area table that you want to use to create reports for legal requests or legal matters submitted for the practice area.

    For more information, see [Add and customize a field in a table](https://www.servicenow.com/docs/access?context=t_CreatingNewFields&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

2.  Create or modify a record producer for a legal request or legal matter for the associated practice area.

    For more information, see [Create or modify a record producer for legal services through Classic environment](create-record-producer-legal-request.md).

3.  Update the business rule to synchronize variables with the mapped table columns when users modify the intake form data after they've submitted a legal request or matter.

    1.  Navigate to **System Definition** &gt; **Business Rules**.

    2.  Open the **Sync variable with mapped columns** business rule.

    3.  In the **When to run** tab, add a new OR condition for the category.

        For example, to synchronize the variables of a Compliance intake form with the mapped columns of the Compliance \[sn\_lg\_ops\_compliance\] table, you would enter the following OR condition:

        **\[Category\] \[is\] \[Compliance \[sn\_lg\_ops\_compliance\]\]**

    For more information, see [Create a business rule](https://www.servicenow.com/docs/access?context=c_BusinessRules&version=australia&pubname=australia-build-workflows&section=t_CreatingABusinessRule&ft:locale=en-US).


**Parent Topic:**[Configuring Legal Request Management](../concept/legal-ops-administration.md)

