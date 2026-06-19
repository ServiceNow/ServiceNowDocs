---
title: Example Build Agent use cases
description: Use Build Agent for a wide range of development scenarios beyond application creation, including app analysis, modernization, documentation, governance, and learning assistance. Reference these scenarios to identify ways to apply Build Agent across your development workflow.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/building-applications/additional-build-agent-use-cases.html
release: australia
product: Building Applications
classification: building-applications
topic_type: reference
last_updated: "2026-05-06"
reading_time_minutes: 4
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Explore, Build Agent, Agentic development on the ServiceNow AI Platform, Building applications]
---

# Example Build Agent use cases

Use Build Agent for a wide range of development scenarios beyond application creation, including app analysis, modernization, documentation, governance, and learning assistance. Reference these scenarios to identify ways to apply Build Agent across your development workflow.

## Documentation creation

Use Build Agent to create customized knowledge base articles and knowledge articles, so users can access information and learn the application more easily.

Build Agent can automate the creation of readme files for source code repositories. Generated readme files provide clear, structured documentation that outlines installation procedures, usage guidelines, and example snippets, which streamlines the onboarding process for new developers.

## Learning assistance

Use Build Agent as a resource for learning ServiceNow application development practices. You can ask about a wide range of topics, including development techniques, available APIs, and the overall functionality of the ServiceNow AI Platform.

Build Agent supports continuous learning by summarizing relevant documentation, highlighting key points, and providing concrete examples that illustrate complex concepts, which helps developers grasp and apply general guidelines in their work.

## Brainstorming sessions

Use Build Agent to refine application development ideas and capture structured requirements for later build steps during brainstorming sessions. Requirements are captured in detail during these sessions, supporting a structured process for developing application features. All ideas are documented so your team can reference previous discussions and integrate feedback during the development lifecycle.

## Additional use cases

Use the following scenarios to identify specific ways to apply Build Agent in your development workflow.

-   **App gap analysis**

    Summarize an existing app, identify gaps in coverage, and propose targeted enhancements. For example, Build Agent flags tables without ACLs, business rules with no test coverage, and manual steps that could be automated with flows.

-   **Security posture review**

    Open an existing app and audit its ACLs, roles, and data filters. Build Agent identifies gaps such as tables with no ACLs, overly permissive rules, and missing role hierarchy, then generates fixes.

-   **Test coverage bootstrapping**

    Analyze an app's metadata, identify what has zero test coverage, generate Automated Test Framework \(ATF\) tests for the gaps, run them, and triage failures.

-   **Architecture diagrams**

    Generate Mermaid.js diagrams by querying and collating data from the platform.

-   **Common workflow patterns**

    Describe a common business process — such as intake and approval, escalation routing, or SLA monitoring with dashboards — and Build Agent scaffolds the full workflow, including tables, flows, catalog items, notifications, and reporting.

-   **Migration acceleration**

    Provide your source system's table definitions, business logic, or data model — pasted as SQL, text, CSV, or screenshots — and Build Agent recreates the equivalent tables, fields, relationships, and automation on the ServiceNow AI Platform.

-   **App modernization**

    Analyze legacy customizations such as classic workflows, Jelly UI, and script-heavy logic, then rebuild them using modern patterns: flows instead of workflows, React UI pages instead of Jelly, and structured security instead of script-based checks.

-   **Data-model scaffolding**

    Paste a CSV file, drop a spreadsheet screenshot into the chat, or describe your data model in plain text. Build Agent generates the matching ServiceNow tables, columns, and relationships. For Excel or PDF input, convert to CSV or paste a screenshot first.

-   **Cross-scope workflows**

    Build custom apps that write to global tables such as Incident. For example, auto-generate incidents when assets become overdue.

-   **Build from user stories**

    Point Build Agent at a user story from the `rm_story` table or paste one from another tool. The acceptance criteria drive development, creating the tables, logic, and tests that satisfy each criterion.

    **Note:** Querying `rm_story` directly requires the Agile Development 2.0 plugin.

-   **SQL to table**

    Paste a SQL `CREATE TABLE` definition into the chat and Build Agent translates it into a ServiceNow table with matching column types and relationships.

-   **Post-build summaries**

    Generate release notes and summary documents after the build foundation is complete.

-   **Instance governance setup**

    Create instance scan checks that enforce your organization's standards, including naming conventions, security requirements, and code quality. Checks run as part of your existing instance scan infrastructure.


## Use cases by development goal

Use the following table to identify Build Agent use cases based on your development stage and goal.

<table id="table_use-case-matrix"><thead><tr><th>

Use case

</th><th>

Immediate productivity

</th><th>

Process and quality improvement

</th><th>

Strategic transformation

</th></tr></thead><tbody><tr><td>

Explore \(zero risk, read-only\)

</td><td>

-   Explain any concept, API, or metadata type in plain language
-   Look up how a specific business rule, flow, or ACL works

</td><td>

-   Document an existing app end-to-end: architecture, security model, and data flows
-   Generate Mermaid diagrams of table relationships and integration points

</td><td>

-   Run existing Automated Test Framework \(ATF\) tests and triage failures to assess application health before a release
-   Audit security posture: review ACLs, identify missing role controls, and surface compliance gaps

</td></tr><tr><td>

Enhance \(modifications, reviewable before promotion\)

</td><td>

-   Add a field, client script, or UI policy to a form
-   Add a catalog variable or update a record producer

</td><td>

-   Add email notifications, scheduled jobs, and flows to automate a manual process
-   Build a scripted REST API for an external integration

</td><td>

-   Generate ATF test suites for untested apps, then run and triage them to establish a quality baseline
-   Add instance scan checks to enforce governance standards across the platform

</td></tr><tr><td>

Build \(new development on non-production\)

</td><td>

-   Prototype an app from a one-line description
-   Create a catalog item with variables and a fulfillment flow

</td><td>

-   Build a full app with tables, roles, ACLs, business rules, flows, catalog items, and a UI page
-   Build a Service Portal or workspace for self-service

</td><td>

-   Build AI agents and Now Assist skills to bring intelligent automation into your processes
-   Build from design mockups or a detailed PRD, complete with automated test coverage from day one

</td></tr></tbody>
</table>**Parent Topic:**[Exploring Build Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/building-applications/exploring-build-agent.md)

