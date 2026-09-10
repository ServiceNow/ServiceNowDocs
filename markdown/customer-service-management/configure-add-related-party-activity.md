---
title: Add Related Parties Activity
description: Configure the Add Related Parties activity to manage related party records within a playbook, helping agents collect structured data more efficiently during playbook execution.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/configure-add-related-party-activity.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Activities, Playbooks in Customer Service Management, Agent tools, Organize agent workspaces, Configure, Customer Service Management]
---

# Add Related Parties Activity

Configure the Add Related Parties activity to manage related party records within a playbook, helping agents collect structured data more efficiently during playbook execution.

## Before you begin

Role required: playbook\_experience.admin

## About this task

The Add Related Parties activity is a customizable, interactive playbook activity that enables users to manage related parties — such as co-applicants, consumers, contacts, partners, or other entities — directly within the context of a parent record, such as a case, sold product, or custom record. The activity generates a dynamic form based on the selected table data, letting users add, edit, or delete related party records during playbook execution. User-entered data is returned as JSON for validation or use in later playbook activities.

This activity is ideal for scenarios such as:

-   Adding co-applicants or authorized representatives to loan applications
-   Listing household members or family contacts on case records
-   Linking business partners or vendors to contracts
-   Associating multiple contacts or consumers with sold products
-   Preloading existing related parties already linked to a record for further verification before proceeding within the active playbook

Understanding Building Playbook Stages and Activities:

In Workflow Studio, playbooks are organized into stages that group related activities. Stages represent phases of your workflow and appear as columns in the playbook canvas. Within each stage, activities are the individual steps that agents complete, displayed as cards that render sequentially.

Within a stage, you can configure activities to guide users through steps such as creating records, uploading documents, reviewing information, and completing assignments. You can incorporate the Add Related Parties activity into an existing stage within your workflow, or create a dedicated stage for related party management. The following procedure outlines how to add and configure the Add Related Parties activity within a playbook.

## Procedure

1.  Navigate to the **Now Assist Admin Console**.

2.  Select **All** &gt; **Playbook Designer**.

3.  Select a playbook to configure.

    -   To create a new playbook, select **New** and complete the prompted details.
    -   To modify an existing playbook, open it and select **Duplicate** in the top-right. Update the name and description before continuing.
4.  Add an activity to your playbook.

    1.  In the playbook canvas, select the plus icon on the connector line \(between the start and end nodes\).
    2.  Select the square icon to add an activity.

        **Note:** Selecting the diamond icon adds a stage to the canvas, rather than an activity.

    3.  In the activity picker, search for and select **Add Related Parties**.
5.  Configure the newly added activity in the playbooks canvas using the **Details, Automation, and UI Layout** tabs in the side panel.

    To further customize the side panel tabs, and to tailor the activity to your specific use case, see [Configure Add Related Party Activity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/customize-add-related-party-activity.md).


