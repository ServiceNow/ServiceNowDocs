---
title: Service Model Foundation modules
description: The Service Model Foundation plugins add several modules to the application navigator.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Overview, Configure Service Model Foundation, Data models, Set up your environment, Configure, Customer Service Management]
---

# Service Model Foundation modules

The Service Model Foundation plugins add several modules to the application navigator.

## Business Location modules

**Service Organizations &gt; Internal/External Business Locations**: This module lists the internal and external business locations that have been created.

**Note:** This module is available in Agent Workspace and in the platform interface.

Users with the following roles have access to these modules.

-   sn\_customerservice\_manager
-   sn\_customerservice\_agent
-   sn\_customerservice.consumer\_agent
-   sn\_customerservice.svc\_location\_agent
-   sn\_customerservice.svc\_location\_consumer\_agent

## Service Organization External Staffs module

**Service Organizations &gt; Service Organization External Staffs**: This module lists the external staff members created and added to the external business location.

**Note:** This module is available in Agent Workspace and in the platform interface.

Users with the following roles have access to these modules.

-   sn\_customerservice\_manager
-   sn\_customerservice\_agent
-   sn\_customerservice.consumer\_agent
-   sn\_customerservice.svc\_location\_agent
-   sn\_customerservice.svc\_location\_consumer\_agent

## Household modules

-   Customer &gt; Households: Lists the households that a user has access to.
-   Customer &gt; Household Members: Lists the consumers that have been added to households.

**Note:** These modules are available in Agent Workspace and in the platform interface.

Users with the following roles have access to these modules.

-   sn\_customerservice\_manager
-   sn\_customerservice.consumer\_agent
-   sn\_customerservice.svc\_location\_consumer\_agent
-   sn\_customerservice.relationship\_agent
-   sn\_crm\_household\_data\_manager
-   sn\_crm\_household\_relationship\_data\_manager
-   sn\_crm\_consumer\_relationship\_data\_manager
-   sn\_crm\_foundation\_data\_manager
-   sn\_crm\_foundation\_admin

## Customer Relationship modules

-   Customer Relationships &gt; Consumer Team Members: Lists the relationships that have been created between an internal user and a consumer.
-   Customer Relationships &gt; Household Team Members: Lists the relationships that have been created between an internal user and a household.
-   Customer Relationships &gt; Consumer Relationships: Lists the relationships that have been created between two consumers, regardless of household.
-   Customer Relationships &gt; Household Relationships: Lists the relationships that have been created between two consumers who are members of the same household.

**Note:** These modules are only available in the platform interface. You can view relationships in Agent Workspace in related lists. Customer service managers and location managers can also modify account, consumer, and household team member relationships in Agent Workspace.

Users with the following roles have access to these modules.

-   sn\_customerservice\_manager
-   sn\_customerservice.consumer\_agent
-   sn\_customerservice.svc\_location\_manager
-   sn\_customerservice.svc\_location\_consumer\_agent

In addition to the preceding roles,

-   the sn\_crm\_consumer\_relationship\_viewer, sn\_crm\_consumer\_relationship\_data\_manager, sn\_crm\_household\_relationship\_data\_manager, sn\_crm\_foundation\_data\_manager, and sn\_crm\_foundation\_admin roles also have access to the Consumer Team Members module.
-   the sn\_crm\_household\_relationship\_viewer, sn\_crm\_consumer\_relationship\_data\_manager, sn\_crm\_household\_relationship\_data\_manager, sn\_crm\_foundation\_data\_manager, and sn\_crm\_foundation\_admin roles have the access to the Household Team Members and Householder Relatationships modules.

