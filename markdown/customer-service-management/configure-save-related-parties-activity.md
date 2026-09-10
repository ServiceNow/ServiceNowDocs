---
title: Save Related Parties Activity
description: Save related party records to the database using the output of an upstream Add related party activity. Supports insert, update, and delete operations when related table permissions are enabled.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/configure-save-related-parties-activity.html
release: australia
topic_type: task
last_updated: "2026-06-08"
reading_time_minutes: 2
breadcrumb: [Activities, Playbooks in Customer Service Management, Agent tools, Organize agent workspaces, Configure, Customer Service Management]
---

# Save Related Parties Activity

Save related party records to the database using the output of an upstream Add related party activity. Supports insert, update, and delete operations when related table permissions are enabled.

## Before you begin

Role required: playbook\_experience.admin

**Note:** The Save related parties activity is available only when Playbooks for Customer Service Management is installed with the demo data flag enabled.

## About this task

The Save Related Parties activity is an automation activity that persists related party records to the database. It’s configured within Workflow Studio, is automation-only, and will not appear to agents during playbook execution.

This activity is only needed when the Add Related Parties activity in your playbook does not have the Save Related Party Data checkbox enabled. Use the Save Related Parties activity instead when you need to control when the save occurs, and when intermediate steps must happen before the data is committed.

This activity is ideal for scenarios such as:

-   Running an approval or validation step before related party data is written to the database
-   Collecting related parties across multiple stages of a playbook and committing all records only when the full application or workflow is complete
-   Verifying a co-applicants identity or eligibility before their record is committed and saved to the database in a loan application playbook

**Note:** The Add Related Parties activity includes a Save related parties check box that, when enabled, writes data to the database automatically when the agent completes the activity. On its own, Add Related Parties only captures data. That data is not saved to the database until the Save related parties activity is added to the playbook flow. It must be placed after an Add related party activity in the playbook flow to receive and process that activity's JSON output.

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

    3.  In the activity picker, search for and select **Save Related Parties**.
    **Note:** The Save Related Parties activity requires an Add related party activity to be configured upstream in the same playbook flow. Without it, the activity has no data to process.

5.  Configure the newly added activity in the playbooks canvas using the **Details and Automation** tabs in the side panel.

    To further customize the side panel tabs, and to tailor the activity to your specific use case, see. [Configure Save Related Parties Activity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/customize-save-related-parties-activity.md)


