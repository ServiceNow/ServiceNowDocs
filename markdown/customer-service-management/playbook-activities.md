---
title: Activities
description: Activities are the individual steps that make up playbooks in Customer Service Management.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/playbook-activities.html
release: australia
topic_type: concept
last_updated: "2026-07-16"
reading_time_minutes: 5
keywords: [playbook activities, csm playbook activities, add related party activity, save related parties activity, add activity]
breadcrumb: [Playbooks in Customer Service Management, Agent tools, Organize agent workspaces, Configure, Customer Service Management]
---

# Activities

Activities are the individual steps that make up playbooks in Customer Service Management.

Activities show up as cards in the workspace and appear in order within each stage. They are the building blocks of every playbook. Some activities need input from an agent, such as filling out a form or selecting a related record. Others run on their own, without any agent action.

A CSM playbook can include several kinds of activities — most of which are built into the playbook and run in a set order to guide the agent through the case. An agent can also add an optional activity when a case needs it, such as scheduling an appointment or sending an approval request. Other activities run on their own to save or update information, such as writing records to the database after an agent finishes a step.

Activities are set up in Workflow Studio and shown in the workspace through UI Builder. CSM playbooks also come with a set of existing activities that an administrator can use as they are or customize to fit a specific case.

## Navigating playbook stages and activities

Agents can use the stage picker and activity picker to navigate between stages and activities as assigned roles or activity security configurations permit. For example, activities such as case tasks can be assigned to different users. A user with the case task agent role can only see the case tasks that are assigned to them.

When an agent opens a record that uses a playbook, it opens to the current stage and highlights the current activity. For stages with multiple activities, the current activity is the first available activity. An available activity is an activity that has a state other than Complete.

When an agent selects an available activity, it becomes the current activity. An agent can navigate stages and activities in any order as long as there is at least one available activity to select.

**Note:** The playbook configuration determines the visibility and accessibility of pending stages and activities. For more information, see [Configure playbook stage and activity visibility](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/playbook-config-activity-visibility.md).

## Activities in a playbook

A playbook is organized into stages, and each stage contains one or more activities. Activities are the individual tasks an agent completes to work through a stage and resolve the case. The current stage is highlighted, and its activities appear in the activity picker. Selecting an activity opens it in the activity viewer, where the agent does the work to complete it.

A few things shape how an agent works with activities:

-   **Activity state**: Each activity shows its current state in the activity picker, so an agent can see what is done and what is left. For the list of states, see .
-   **How activities are displayed**: The page layout and activity view control how stages and activities appear, such as a focused or stacked view. For more information, see [Select a playbook activity view](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/playbook-select-activity-view.md).
-   **Navigating activities**: An agent can move between stages and activities, including by using keyboard navigation, in the order that their role and the playbook configuration allow.
-   **Filtering activities**: An agent can filter the activity list by state to focus on certain activities. For more information, see [Filter playbook activities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/csm-playbook-filter-activities.md).
-   **Visibility**: An administrator can control which stages and activities are visible, such as hiding activities that are pending or that an agent cannot access. For more information, see [Configure playbook stage and activity visibility](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/playbook-config-activity-visibility.md).

## Types of activities

Activities in a CSM playbook fall into two broad groups based on how they run:

-   Activities that need input from an agent, such as filling out a form, reviewing a document checklist, or adding related parties to a record.
-   Activities that run automatically, without any agent action, such as sending a notification, triggering an approval, or creating a record in the database.

## Optional activities

Each activity has a start rule that controls when it runs. An activity with an automatic start rule runs on its own when the playbook reaches it. An activity with a Manual start rule waits for an agent to start it — this is what makes an activity optional, so an agent can add it to a running playbook only when it's needed.

Optional activities can be global, so an agent can add them at any point, or tied to a specific stage, so they can be added only while that stage is active. This gives agents room to respond to what each case needs, rather than following the exact same steps every time.

When an optional activity involves the customer, such as requesting a document upload or asking the customer to confirm account details before the case moves forward, it becomes part of the customer's own experience, not just the agent's workflow.

For configuration steps to set up optional activities in Workflow Studio, see [Configure an optional activity for a playbook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/configure-optional-activity-for-a-case-type-playbook.md)

## Configuring stage and activity visibility

Users with the admin role can configure the visibility of playbook stages and activities, including:

-   Showing or hiding stages and activities that are pending.
-   Showing or hiding stages and activities where a user does not have access.

The administrator configures these settings in the Playbook Experience record. For more information, see [Configure playbook stage and activity visibility](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/playbook-config-activity-visibility.md).

## CSM playbook activities

The following existing activities are available to customize and use in CSM playbooks.

|Activity|Description|
|--------|-----------|
||Enables agents to add, edit, or delete related party records directly within a playbook. Set up by an admin in Workflow Studio. Returns JSON output for downstream use.|
||Automation activity that saves related party records captured by the Add Related Parties activity to the database. Accepts JSON input and writes records to the specified target table.|

