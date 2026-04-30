---
title: Create a record using a playbook
description: Create a record using a playbook activity instead of a record form.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Using playbooks, Automate and optimize, Use, Customer Service Management]
---

# Create a record using a playbook

Create a record using a playbook activity instead of a record form.

## Before you begin

Role required: sn\_customerservice\_agent

## About this task

If a playbook is configured to use the record generator feature, customer service agents can create a record using a playbook activity. Creating a record from a list or form, or from an activity in another playbook, opens the playbook and initiates the first activity. This activity guides an agent through the record creation process.

With additional configuration, you can also create a case from any of the following records that opens a playbook and initiates the first activity:

-   Interaction
-   Case
-   Account
-   Consumer

To create cases in this way, the following configuration is required:

-   Enable the **Create Case** button from the Customer Service Case Types application for each of these records. This enables agents to create a specific type of case.

    See [Configure customer service case types](configure-csm-case-types.md) for more information about using the Customer Service guided setup and the Case Types category to configure case type UI actions.

-   Configure the playbook to use the playbook record generator.

    For more information about configuring this feature, see [Playbook record generator](https://www.servicenow.com/docs/access?context=playbook-record-generator-overview&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US).


## Procedure

1.  Navigate to a list or form in CSM Configurable Workspace.

    For example, navigate to the All Onboarding Cases list.

2.  Select **New**.

    If you selected **New** from the All Onboarding Cases list, the Onboarding playbook opens and initiates the first activity for collecting customer information.

3.  Fill in the fields on the first activity card.

4.  Select **Continue**.

    The system uses the customer information to create a case. The case number is added to the tab and the first activity in the first playbook stage is marked as complete. The second activity is highlighted as the current activity.

5.  Collect additional customer information, if needed, and select **Save**.

6.  Continue using the playbook stages and activities to resolve the customer's issue and complete the case.


