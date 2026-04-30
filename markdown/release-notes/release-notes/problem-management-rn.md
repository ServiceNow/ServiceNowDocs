---
title: Problem Management release notes
description: The ServiceNow Problem Management application helps you identify the cause of errors in the IT infrastructure that are reported as occurrences of related incidents. Problem Management was enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
---

# Problem Management release notes

The ServiceNow® Problem Management application helps you identify the cause of errors in the IT infrastructure that are reported as occurrences of related incidents. Problem Management was enhanced and updated in the Yokohama release.

## Problem Management highlights for the Yokohama release

-   Increase operational efficiency of tier 1 service desk agents with the dedicated sn\_service\_desk\_agent role.
-   Simplify the management of problems and problem tasks using Problem Management models.

See [Problem Management](https://www.servicenow.com/docs/access?context=c_ProblemManagement&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US) for more information.

## New in the Yokohama release

-   **[User role for service desk agents](https://www.servicenow.com/docs/access?context=prob-roles-instld-itsm-roles&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

    With the sn\_service\_desk\_agent user role, increase operational efficiency by streamlining the process of asking about, gathering, and verifying information, as well as delivering quick resolutions. This role is designed for tier 1 service desk agents and is accessible when the ITSM Roles plugin \(com.snc.itsm.roles\) installed.

    The sn\_service\_desk\_agent role includes the following roles:

    -   sn\_incident\_write
    -   sn\_problem\_write
    -   sn\_change\_write
    -   sn\_request\_write
    -   tracked\_file\_reader
    Additionally, with the installation of the **ITSM Gen AI** \(**com.sn.itsm.gen.ai**\) plugin, the knowledge\_user and now\_assist\_panel\_user roles are integrated within the sn\_service\_desk\_agent role.

    The sn\_service\_desk\_agent user role can be used starting with Service Operations Workspace version 6.1.

-   **[Problem Models for Streamlined Problem Management](https://www.servicenow.com/docs/access?context=problem-mgmt-models&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

    Problem Management models are used to simplify management of problems and problem tasks. These models provide an efficient way to configure state transitions and define conditions to move from one state to another.

    This functionality is enabled out of the base system for new or zBoot customers.


## Activation information

Problem Management is a ServiceNow AI Platform feature that is active by default.

**Parent Topic:**[IT Service Management release notes](it-service-management-rn-landing.md)

