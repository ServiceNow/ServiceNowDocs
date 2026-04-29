---
title: Vibe-coded app refinement in ServiceNow Studio
description: ServiceNow Studio connects AI-generated, vibe-coded apps to enterprise-grade solutions, where you can review, edit, and enhance your application in a dedicated development environment.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [ServiceNow Studio, vibe coding, Build Agent, AI-assisted development, application development, developer tools, code refinement, metadata editing, Automated Test Framework, ATF, application files, access control lists, ACL, record producers, update sets]
audience: developer
breadcrumb: [Build Agent overview, Develop, Vibe coding and AI-assisted development, Vibe coding and AI app development on the ServiceNow AI Platform, Building applications]
---

# Vibe-coded app refinement in ServiceNow Studio

ServiceNow Studio connects AI-generated, vibe-coded apps to enterprise-grade solutions, where you can review, edit, and enhance your application in a dedicated development environment.

After vibe coding or developing an application with Build Agent or Now Assist for Creator, ServiceNow Studio provides a powerful, developer-friendly environment for reviewing, customizing, and perfecting your app.

If you're a developer who's new to vibe coding and AI-assisted development, ServiceNow Studio provides a more abstracted approach to code refinement compared to ServiceNow IDE.

For documentation on using Build Agent in ServiceNow Studio, see [Build Agent in ServiceNow Studio](../../servicenow-studio/concept/build-agent-in-servicenow-studio.md).

## ServiceNow Studio workflow

To review and refine your vibe-coded app from Build Agent in ServiceNow Studio, follow these steps:

1.  Open your app in ServiceNow Studio.

2.  Use Build Agent to create or edit metadata for your application.
3.  Review and edit application files.

    -   Use the **Application Files** tab to see all generated elements and metadata—tables, access controls, roles, record producers, and more.
    -   Open any file \(such as a table or ACL\) in a new tab for detailed inspection and editing.
    -   Confirm that generated tables capture the correct data and adjust field properties as needed.
    -   Edit access control lists \(ACLs\) to confirm that the correct roles and permissions are applied.
    -   Review and modify roles, record producers, and other artifacts for accuracy.
4.  Use developer tools in ServiceNow Studio.

    -   ServiceNow Studio provides a tabbed, IDE-like interface for navigation and editing.
    -   You can refine code, add business logic, and manage metadata across your app's scope.
    -   Use Build Agent for update set management, cross-scope editing, and safe deployment.
5.  Iterate with Build Agent.

    -   Use the Build Agent panel to edit metadata for your application.
    -   Toggle the panel as needed to avoid covering important information.
    -   Use Build Agent to create Automated Test Framework \(ATF\) tests.
6.  Test and validate the app.

    -   Use the ServiceNow Studio integration with the ATF to run the tests.
    -   Verify that your refined app functions correctly.

## When to choose the ServiceNow IDE or ServiceNow Studio

1.  ServiceNow IDE: Best for file‑centric, code‑heavy edits, rapid iteration, and pairing with the ServiceNow SDK for local dev/CI. Suitable for developers familiar with the ServiceNow AI Platform.
2.  ServiceNow Studio: Best for metadata‑centric review \(tables, ACLs, roles\) and cross‑scope editing with a visual overview of app artifacts; keeps Now Assist in‑context for conversational adjustments. Suitable for developers with various levels of experience on the ServiceNow AI Platform.

**Parent Topic:**[AI-assisted ServiceNow AI Platform development with Build Agent](vc-build-agent-landing.md)

