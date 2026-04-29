---
title: Build form and business logic
description: The next step in designing an application is to build logic. Logic includes form logic \(what people can and cannot see/use on a form\) and business logic \(rules that govern what happens to data when it is entered\).
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Build your application, Exploring professional development, Building pro-code applications, Developing your application, Building applications]
---

# Build form and business logic

The next step in designing an application is to build logic. Logic includes form logic \(what people can and cannot see/use on a form\) and business logic \(rules that govern what happens to data when it is entered\).

## Agentic AI

Create applications with help from agentic AI. For more information, see [Vibe coding and AI app development on the ServiceNow AI Platform](../../ai-capabilities/concept/use-ai-capabilities-in-custom-apps.md).

## Scripting and modifications

Before writing any code, be aware of the impact on upgrades and the adoption of new ServiceNow features. Particular care should be taken when modifying baseline artifacts and processes.

Consider the following before scripting:

-   Assess the requirement. Is the logic critical to the functioning of the app?
-   Determine if ServiceNow can be configured to fulfill the requirement without code.
-   Leverage options, such as Flow Designer, Virtual Agent, and UI Policies to take advantage of platform capabilities without writing code.
-   Low and no-code approaches to logic are easier to debug and upgrade.

Examples of when scripting is appropriate:

-   Building Flow Designer actions
-   Creating a Scripted REST API
-   Creating logic for scoped applications in Script Includes
-   Customizing and creating widgets for Service Portal

Evaluate the business requirement and consider a no-code route before using a scripted solution.

Be aware of ServiceNow enhancements. For example, in the orlando release, Virtual Agent conversations have more no-code options than London. Read release notes and other publications. Get certified and stay current with your certifications.

To better understand when to customize, review the [Innovate at Scale Success Playbook](https://www.servicenow.com/success/playbook/innovate-at-scale.html) on the [Customer Success Center](https://www.servicenow.com/success.html).

## Modifying default behavior

In the past, one of the strategies used was to copy the artifact to update and to deactivate the original. The copy/deactivate approach is no longer recommended due to the following issues:

-   Developers cannot tell if a deactivated artifact was upgraded without research.
-   Two files, the original and the copy, need to be maintained. Maintenance doubles each time a customization is made.
-   With each release, the customized record becomes older.
    -   Customers do not receive the enhancements included in a new release.
    -   A new release may rely on the original record being updated.
    -   Developers may make more changes to compensate for the original record being inactive.

A script where only the **Active** flag is changed will be updated, but the script does not appear on the skipped list. With the copy and deactivate strategy, a developer has less visibility into customizations and cannot easily assess or revert to the baseline version.

Rather than copying and deactivating the original artifact, edit the artifact directly. The ServiceNow Upgrade Engine will add the latest version to the version history and report that the artifact was skipped. Developers can see a new version is available with the upgrade.

-   **[Form logic](form-logic.md)**  
Controlling what users see when they visit a form can increase productivity and responsiveness. For example, users should only see fields that are useful to them. Users may only need to see certain fields based on what is configured on the form. Apply form logic to control what is visible, read-only, and mandatory on a form.
-   **[Business rules and script includes](business-rules-and-script-includes.md)**  
Business rules are server-side actions that can be run during CRUD \(Create, Read, Update, Delete\) operations on instance records.
-   **[Flow Designer](flow-designer.md)**  
Flow Designer is a ServiceNow AI Platform feature that enables rich process automation capabilities in a consolidated design environment. Flow Designer enables process owners to use natural language to automate approvals, tasks, notifications, and record operations without having to code.

**Parent Topic:**[Build your application](build-your-application.md)

