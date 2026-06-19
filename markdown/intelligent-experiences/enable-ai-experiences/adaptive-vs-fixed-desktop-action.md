---
title: When to use adaptive vs. defined path desktop actions
description: Use this guide to determine which type of desktop action best fits your automation scenario before you begin configuration.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/enable-ai-experiences/adaptive-vs-fixed-desktop-action.html
release: australia
product: Enable AI Experiences
classification: enable-ai-experiences
topic_type: concept
last_updated: "2026-04-27"
reading_time_minutes: 3
breadcrumb: [Explore, AI Desktop Actions, Enable AI experiences]
---

# When to use adaptive vs. defined path desktop actions

Use this guide to determine which type of desktop action best fits your automation scenario before you begin configuration.

There are two types of desktop actions: defined path and adaptive path. Both enable AI agents to automate tasks on behalf of users, but they differ in how steps are executed, what applications they support, and how they handle variation in the user interface.

## Key differences

<table><thead><tr><th>

Area

</th><th>

Defined path

</th><th>

Adaptive path

</th></tr></thead><tbody><tr><td>

How steps are determined

</td><td>

You record a fixed sequence of steps in the AI Desktop Actions Windows application

</td><td>

The AI agent generates and adjusts steps dynamically based on a high-level goal you describe

</td></tr><tr><td>

Supported applications

</td><td>

Desktop applications, thick client applications, and web-based applications

</td><td>

Web-based applications and websites only

</td></tr><tr><td>

Environment

</td><td>

Runs on the Windows desktop

</td><td>

Requires Google Chrome and the ServiceNow Web Automation browser extension

</td></tr><tr><td>

Handles UI changes

</td><td>

Steps may fail if the application UI changes

</td><td>

Adjusts to changes in UI state at runtime

</td></tr><tr><td>

Handles conditional logic

</td><td>

Requires a separate desktop action for each conditional path

</td><td>

Evaluates conditions at runtime and determines the appropriate path

</td></tr><tr><td>

Result consistency

</td><td>

Consistent and repeatable — steps execute in the same order every time

</td><td>

Results may vary between runs due to the non-deterministic nature of AI

</td></tr><tr><td>

Configuration location

</td><td>

AI Desktop Actions Windows application and AI Agent Studio**Note:** Background task desktop actions can't be configured in AI Desktop Actions, but you can add them in AI Agent Studio as tools.

</td><td>

AI Agent Studio

</td></tr></tbody>
</table>## Choose defined path when

Use defined path desktop actions for scenarios where the steps are known, fixed, and don't change between executions:

-   The task involves a legacy desktop application or thick client that does not have an API or web interface. For example, automatically processing badge-related requests in a facilities management desktop application.
-   The task follows the same sequence of steps every time, regardless of the data involved. For example, entering shipping data into a shipping management application using a fixed form structure.
-   Your organization requires predictable, auditable automation where every execution follows an identical sequence.
-   The application runs on Windows and does not require a browser.

## Choose adaptive path when

Use adaptive path desktop actions for scenarios where the steps can't be fully predicted in advance, or where the application UI may change between executions:

-   The task is web-based and involves conditional logic. For example, the next steps depend on the outcome of a previous action, such as reviewing an incident record and routing it differently based on its current state.
-   The web application updates its UI frequently.
-   You want the AI agent to determine the most efficient path to complete a goal, rather than following a prescribed sequence.
-   The task requires navigating multiple web pages or making decisions based on page content. For example, finding the latest invoice from a vendor portal and returning a summary.

## When you aren't sure which to use

If your task is web-based and you're uncertain whether the steps always be the same, start with adaptive path. Adaptive path actions require less upfront design work and can handle variation that would cause a defined path action to fail. If you find that results are inconsistent and the task is always performed the same way, consider switching to defined path.

If your task involves a non-browser desktop application, defined path is your only option. Adaptive path requires Google Chrome and can't interact with applications outside the browser.

**Note:**

Defined path desktop actions can automate both desktop applications and web-based tasks. Adaptive path desktop actions support web-based tasks only and require Google Chrome with the ServiceNow Web Automation browser extension installed.

