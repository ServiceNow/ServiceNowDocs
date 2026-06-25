---
title: Configuring Task Mining
description: Plan and configure your Task Mining implementation so that Task Mining analysts and power users can access the Task Mining Workspace and create and manage projects.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/now-intelligence/task-mining/configuring-task-mining.html
release: australia
product: Task Mining
classification: task-mining
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Task Mining, Platform Analytics]
---

# Configuring Task Mining

Plan and configure your Task Mining implementation so that Task Mining analysts and power users can access the Task Mining Workspace and create and manage projects.

## Configuration overview

These configuration tasks must be performed on each instance being used. After installation, these activities don't have to be performed in any specific order.

**Warning:** Do not modify default excluding filters.

-   **[Install Task Mining](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/task-mining/install-task-mining.md)**

    Install the Task Mining application \(sn\_tm\_core\) if you have the admin role.

-   **[Adjust Task Mining agent parameters](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/task-mining/set-system-parameters.md)**

    Modify system-level Task Mining agent and system records.

-   **[Define Task Mining anonymization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/task-mining/define-anonymization.md)**

    Replace personally identifiable information with alias data to protect sensitive user information.

-   **[Customize Task Mining notifications for workstation users](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/task-mining/define-workstation-user-notifications.md)**

    Use Task Mining notifications to notify workstation users that their work is being monitored, request consent, and inform them if they have any actions to take.

-   **[Modify the Task Mining data retention period](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/task-mining/define-data-retention.md)**

    Modify the default retention configuration rules to delete data automatically.

-   **[Avoid capturing and displaying application details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/task-mining/replace-application-details.md)**

    Prevent the Task Mining agent from collecting application details but still collect timestamps by replacing application details that match event filters.

-   **[Assign roles for Task Mining users](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/task-mining/assign-users.md)**

    Assign roles to control access to features, capabilities, and data in the Task Mining application.


## Task Mining agent installation

The Task Mining agent is a service installed on workstations that logs certain events from desktop applications after a data request is submitted by a Task Mining analyst or power user and approved by a manager. For more information, see [Install the Task Mining agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/task-mining/install-agent.md).

