---
title: When to use adaptive vs. defined path desktop actions
description: Use this guide to determine which type of desktop action best fits your automation scenario before you begin configuration.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-04-27"
reading_time_minutes: 2
breadcrumb: [Explore, AI Desktop Actions, Enable AI experiences]
---

# When to use adaptive vs. defined path desktop actions

Use this guide to determine which type of desktop action best fits your automation scenario before you begin configuration.

There are two types of desktop actions: defined path and adaptive path. Both enable AI agents to automate tasks on behalf of users, but they differ in how steps are executed, what applications they support, and how they handle variation in the user interface.

## Key differences

|Area|Defined path|Adaptive path|
|----|------------|-------------|
|How steps are determined|You design a fixed sequence of steps in the AI Desktop Actions Windows application|The AI agent generates and adjusts steps dynamically based on a high-level goal you describe|
|Supported applications|Desktop applications, thick client applications, and web-based applications|Web-based applications and websites only|
|Browser requirement|No browser requirement — runs on the Windows desktop|Requires Google Chrome and the ServiceNow Web Automation browser extension|
|Handles UI changes|Steps may fail if the application UI changes|Adjusts to changes in UI state at runtime|
|Handles conditional logic|Requires a separate desktop action for each conditional path|Evaluates conditions at runtime and determines the appropriate path|
|Result consistency|Consistent and repeatable — steps execute in the same order every time|Results may vary between runs due to the non-deterministic nature of AI|
|Configuration location|AI Desktop Actions Windows application|AI Agent Studio|

## Choose defined path when

Use defined path desktop actions for scenarios where the steps are known, fixed, and do not change between executions:

-   The task involves a legacy desktop application or thick client that does not have an API or web interface — for example, automatically processing badge-related requests in a facilities management desktop application.
-   The task follows the same sequence of steps every time, regardless of the data involved — for example, entering shipping data into a shipping management application using a fixed form structure.
-   Your organization requires predictable, auditable automation where every execution follows an identical sequence.
-   The application runs on Windows and does not require a browser.

## Choose adaptive path when

Use adaptive path desktop actions for scenarios where the steps cannot be fully predicted in advance, or where the application UI may change between executions:

-   The task is web-based and involves conditional logic — for example, the next steps depend on the outcome of a previous action, such as reviewing an incident record and routing it differently based on its current state.
-   The web application updates its UI frequently and a fixed sequence of steps would require constant maintenance.
-   You want the AI agent to determine the most efficient path to complete a goal, rather than following a prescribed sequence.
-   The task requires navigating multiple web pages or making decisions based on page content — for example, finding the latest invoice from a vendor portal and returning a summary.

## When you are not sure which to use

If your task is web-based and you're uncertain whether the steps always be the same, start with adaptive path. Adaptive path actions require less upfront design work and can handle variation that would cause a defined path action to fail. If you find that results are inconsistent and the task is always performed the same way, consider switching to defined path.

If your task involves a non-browser desktop application, defined path is your only option. Adaptive path requires Google Chrome and cannot interact with applications outside the browser.

**Note:**

Defined path desktop actions can automate both desktop applications and web-based tasks. Adaptive path desktop actions support web-based tasks only and require Google Chrome with the ServiceNow Web Automation browser extension installed.

