---
title: Using agent connector and contributor roles in Financial Services Operations
description: Financial Services Operations \(FSO\) applications install agent connector and contributor roles to manage and monitor user privileges effectively. To provide the right level of access, these roles must be paired with roles in the CSM Industry data model and contributor user roles.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [User management, Explore, Financial Services Operations \(FSO\)]
---

# Using agent connector and contributor roles in Financial Services Operations

Financial Services Operations \(FSO\) applications install agent connector and contributor roles to manage and monitor user privileges effectively. To provide the right level of access, these roles must be paired with roles in the CSM Industry data model and contributor user roles.

## Core roles in FSO

-   **Agent Connector**

    Users with this role can create, update, and close cases and tasks.

-   **Contributor**

    Users with this role can create and read cases and make limited updates during the initial stages.


To enable these roles effectively:

-   Combine Agent Connector with a suitable CSM role, such as Relationship Agent or Location Agent.
-   Pair Contributor with a CSM contributor role for accurate access.

## Assigning access based on business needs

Based on your business needs, you can assign CSM industry data model roles or contributor user roles to your users with FSO roles to get the desired level of access for a given user, such as to control access to cases, case tasks, and other case-related information.

For more information, see [Industry data model roles](https://www.servicenow.com/docs/access?context=csm-data-model-roles&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US) and [Contributor user roles](https://www.servicenow.com/docs/access?context=csm-contributor-user-roles&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US).

## Visual overview

The following diagram shows examples how you can combine various FSO roles with the CSM roles and assign them to appropriate FSO user groups.

![Infographic shows FSO fulfiller and contributor roles combining with CSM fulfiller and requestor roles into common example roles groups such as loan agent and card contributor.](../image/fso-csm-contributor-industry-data-model.png "Example of FSO roles combined with roles in CSM industry data model and Contributor users")

## Example role combinations in Financial Services Loan Operations

The following are a few examples of how you can assign roles to users in Loan Operations:

-   A loan relationship manager must be assigned one of the following:
    -   Loan Contributor \[sn\_bom\_loan\_b2b.contributor\] and CSM Relationship Contributor \[sn\_customerservice.relationship\_contributor\] roles
    -   Financial services relationship contributor \[sn\_bom.relationship\_contributor\], which contains both the Loan Contributor \[sn\_bom\_loan.contributor\] and CSM Relationship Contributor \[sn\_customerservice.relationship\_contributor\] roles
-   A branch worker for a business location must be assigned Loan Contributor \[sn\_bom\_loan\_b2b.contributor\] and CSM Service Organization Contributor \[sn\_customerservice.service\_organization\_contributor\] roles.
-   A loan relationship agent must be assigned Loan Agent Connector \[sn\_bom\_loan\_b2b.agent\_connector\] and CSM Relationship Agent \[sn\_customerservice.relationship\_agent\] roles.
-   A loan location agent for a business location must be assigned Loan Agent Connector \[sn\_bom\_loan\_b2b.agent\_connector\] and CSM Location Agent \[sn\_customerservice.svc\_location\_agent\] roles.

![Infographic displaying the titles of the various Loan operations role employees combined with various CSM agent and contributor roles.](../image/example-fso-csm-combine-roles.png "Examples of loan operations roles combined with CSM roles")

