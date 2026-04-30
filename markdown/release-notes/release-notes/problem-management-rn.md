---
title: Problem Management release notes
description: The ServiceNow Problem Management application helps you identify the cause of errors in the IT infrastructure that are reported as occurrences of related incidents. Problem Management was enhanced and updated in the Xanadu release.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
---

# Problem Management release notes

The ServiceNow® Problem Management application helps you identify the cause of errors in the IT infrastructure that are reported as occurrences of related incidents. Problem Management was enhanced and updated in the Xanadu release.

## Problem Management highlights for the Xanadu release

-   Introduction of Problem Management models to provide support for additional problem and problem task scenarios
-   Known error articles are enabled by default for new customers
-   Configure email notifications to redirect to Service Operations Workspace instead of the classic UI16 experience
-   Re-assess a problem task from Work In Progress

See [Problem Management](https://www.servicenow.com/docs/access?context=c_ProblemManagement&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US) for more information.

## New in the Xanadu release

-   **[Initial support for Problem Management models](https://www.servicenow.com/docs/access?context=problem-mgmt-models&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

    Introduction of Problem Management models, beginning with one default problem model \(General\) and two default problem task models \(Root cause analysis and General\).

    The default models are equivalent to the base life cycle in the Washington DC release. This initial support allows for the creation of custom models to tailor additional scenarios for specific use cases.

    **Note:**

    If you are using Service Operations Workspace 5.x and you enable Problem Management models, you will manage problems and problem tasks in the classic UI16 experience, rather than in Service Operations Workspace.

    Service Operations Workspace 6.x is based on the Xanadu release and it supports Problem Management models.


## UI changes

-   **[Problem form](https://www.servicenow.com/docs/access?context=problem-form&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

    The **First reported by** field has been renamed **Origin task** for new customers.

-   **[Prompt when using the Add All button in the Multi-Record Associator](https://www.servicenow.com/docs/access?context=add-multiple-incidents-to-problem&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

    Verify the number of incidents that will be associated with the current problem, helping to prevent associating multiple unintended records.


## Changed in this release

-   **[Re-assess a Problem Task from the Work in Progress state](https://www.servicenow.com/docs/access?context=assess-a-problem-task&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

    Additional flexibility for the workflow of a problem task analyst.

-   **[Email notification redirection behavior](https://www.servicenow.com/docs/access?context=configure-notifcations-sow-itsm&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

    When users select the problem record link in their email notifications, they can be redirected to the problem record in Service Operations Workspace instead of the classic UI16 experience. The ITSM Notifications Redirection \(com.snc.itsm.notifications\_redirection\) plugin is installed and activated automatically to support this behavior.

-   **[Known error articles available by default](https://www.servicenow.com/docs/access?context=create-known-error-from-problem&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

    Problem Knowledge Integration is activated by default for new customers.

-   **[Problem Management Migration Utility](https://www.servicenow.com/docs/access?context=migration-utility&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

    The Xanadu base problem files list is updated so the Problem Management Migration Utility can detect customizations.


## Activation information

[Problem Management](https://www.servicenow.com/docs/access?context=c_ProblemManagement&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US) is a ServiceNow AI Platform feature that is active by default.

**Parent Topic:**[IT Service Management release notes](it-service-management-rn-landing.md)

