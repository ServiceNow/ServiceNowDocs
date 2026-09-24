---
title: CRM Workspace base experience
description: The CRM Workspace base experience provides a ready-to-use workspace to help you begin optimizing your service operations. The workspace includes key components that are immediately accessible and that support both customer service agents and managers in their daily activities.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/csm-config-ws-base-experience.html
release: brazil
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [CRM Workspace, Organize agent workspaces, Configure, Customer Service Management]
---

# CRM Workspace base experience

The CRM Workspace base experience provides a ready-to-use workspace to help you begin optimizing your service operations. The workspace includes key components that are immediately accessible and that support both customer service agents and managers in their daily activities.

## Landing page

The landing page serves as an initial view of the workspace. The CSM workspace landing page provides customer service agents and managers with lists of assigned cases and case tasks as well as agent, group, and organization metrics.

Agents use landing pages as a starting point to get into their work. From the landing page, they can quickly scan and prioritize cases and case tasks, access records, and track their performance.

## Lists

CRM Workspace uses list pages to display record information such as cases and case tasks. These pages help agents navigate, filter, and manage records.

Several default lists are available for use, including Cases, Interactions, Knowledge, and Tasks. Each list is structured to display key columns that provide agents with essential information at a glance.

## Record pages

CRM Workspace record pages provide the base structure for how a record is displayed in the workspace. These pages present the essential fields and related information agents need to resolve customer issues, including customer information, customer history, interactions, SLAs, and much more. Review the record pages available with the CRM Workspace here.

## Responsive interface

CRM Workspace offers agents the ability to personalize their workspace interface for optimal productivity. Display, theme, and notification preferences enable agents to control information density \(comfortable or compact modes\), choose color schemes \(light or dark mode\), and manage alerts. Workspace pages automatically adapt their layout for desktop, tablet, and mobile devices.

## Workspace naming

By default, the name of the workspace included with the Customer Service Management application is CRM Workspace.

**Note:** Starting with the Brazil release, the name of the CSM/FSM Configurable Workspace has changed. The workspace name is dependent on the installed products.

-   CRM Workspace: For customers using the Customer Service Management application or working in the Customer Relationship Management \(CRM\) environment.
-   Industry-specific names: For customers using any of the industry products, such as Financial Services or Public Sector.

You can change this name by setting the **experienceTitleAlias** field on the UX Page Properties record \(sys\_ux\_page\_property.list\).

If multiple aliases are found within the same workspace, the number in the **Order** field on the UX Page Properties record determines which alias is used. The alias with the lowest order number is used for the workspace name display.

