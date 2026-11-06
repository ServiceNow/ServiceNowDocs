---
title: Decision tables release notes
description: The ServiceNow decision tables application enable you to separate decision logic from your code by creating and managing decision rules in a structured, readable format in Workflow Studio. See the following sections for release notes by version.Decision tables in Workflow Studio were updated in Brazil patch X to address issues and defects.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/release-notes/decision-tables-rn.html
release: australia
topic_type: topic
last_updated: "2026-10-21"
reading_time_minutes: 1
breadcrumb: [Workflow Studio release notes, App development and low-code release notes, Features and changes by product, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# Decision tables release notes

The ServiceNow® decision tables application enable you to separate decision logic from your code by creating and managing decision rules in a structured, readable format in Workflow Studio. See the following sections for release notes by version.

## About decision tables

-   Create decision tables that evaluate data from existing ServiceNow® records, external data sources, or data provided at runtime.
-   Build rules with condition columns and multiple result columns.
-   Reference decision tables in code snippets, flows, subflows, and playbooks.

See  for more information.

## Activation and other requirements

-   **Activation information**

    Workflow Studio is a ServiceNow AI Platform feature that is active by default.


## Accessibility and localization

-   **Localization information**

    Decision tables in Workflow Studio support the Localization Framework. However, editing decision tables in Excel isn’t supported for localized content, so the Excel editing feature is available only on instances that use English.


**Parent Topic:**[Workflow Studio release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/release-notes/workflow-studio-rn-landing.md)

## Brazil patch X

Decision tables in Workflow Studio were updated in Brazil patch X to address issues and defects.

### What's changed

-   ****

    Decision table exports now apply the access control lists \(ACLs\) to the data that's exported. Access is determined by the ACLs on the referenced table. This issue is related to PRB2067404.

-   ****

    Delegated developers can now create, read, edit, and delete decision tables that belong to an application they have delegated developer access to. This issue is related to PRB2065210.


