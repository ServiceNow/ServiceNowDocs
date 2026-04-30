---
title: Onboard an external manager
description: Onboard a manager from a contractor company to manage, review, and assign the outsourcing and assignments of work order tasks to their field agents.
locale: en-US
release: yokohama
product: Workforce Optimization for Field Service
classification: workforce-optimization-for-field-service
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring Contractor Management, Configuring contractor capabilities, Setting up your workforce, Configuring Field Service Management, Field Service Management]
---

# Onboard an external manager

Onboard a manager from a contractor company to manage, review, and assign the outsourcing and assignments of work order tasks to their field agents.

## Before you begin

Role required: wm\_admin and wm\_contractor\_manager\_int

## About this task

The work order tasks of the contractor company are automatically assigned to the manager for reassigning it to the field agents. The users can update the work order tasks company only if a manager is assigned.

**Note:** The users will not be able to edit or assign the work order tasks of this contractor company if a manger is not assigned to the company.

You can also do the initial configuration of onboarding an external manager through the **Field Service** &gt; **Administration** &gt; **Contractor Management** guided setup. For more information about using the guided setup interface, see [Using guided setup](https://www.servicenow.com/docs/access?context=guided-setup&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US).

## Procedure

1.  Navigate to **Outsourced Field Service** &gt; **Outsourced Service Providers**.

2.  Click the contractor company from which you want to onboard a manager.

3.  Click **Onboard Manager**.

4.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |First name|Manager's first name.|
    |Last name|Manager's last name.|
    |Active|Option for making this manager the selected external manager.|
    |Email|Manager's official email address.|
    |Time zone|Time zone of the manager’s location.|
    |Business phone|Manager’s business phone number.|
    |Mobile phone|Manager’s mobile number.|
    |Photo|\(Optional\) Photograph of the manager.|
    |Date format|String format as specified in the field.|

5.  Click **Submit**.


## Result

The system sends an email to the newly onboarded manager that includes a URL to use to log in to Field Service Contractor Portal.

