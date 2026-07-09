---
title: Configure intelligent approvals
description: Configure your instance to support intelligent approvals.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2026-07-01"
reading_time_minutes: 1
keywords: [configure, intelligent approvals, AI approvals, AI platform]
---

# Configure intelligent approvals

Configure your instance to support intelligent approvals.

## Configuration overview

Before you can use intelligent approvals, verify that your instance meets the following requirements and complete the configuration tasks.

1.  Verify AI entitlement

    Check your entitlements to determine whether you have access to publish and run intelligent approvals.

2.  Activate the Intelligent Approvals plugin

    Activate the Intelligent Approvals plugin \(`com.glide.intelligent_approvals`\) to turn on the AI agent that processes approval requests and generates approval decisions.

3.  Configure user roles and permissions

    Assign the appropriate role to users who create and manage intelligent approvals. Access to build-time features is restricted by role.

4.  Verify AI Platform Core dependencies

    Confirm that the following AI Platform Core components are activated:

    -   NextWave framework
    -   AIX framework for the homepage experience
    -   Document Intelligence \(DocIntel\) capabilities

## Prerequisites and dependencies

Intelligent approvals require the following components and entitlements:

-   **AI entitlement**

    Check your entitlements to determine whether you have access to create, publish, and run intelligent approvals.

-   **AI Platform Core suite**

    The following AI Platform Core components must be activated:

    -   NextWave framework
    -   AIX framework for the homepage experience
    -   Document Intelligence \(DocIntel\) capabilities \(`com.glide.intelligent_approvals`\)
-   **Approver Agent**

    The Approver Agent that evaluates approval requests and generates approval decisions must be activated. This agent processes requests at runtime and returns one of three outcomes: auto-approve, auto-reject, or can't decide.

-   **User role**

    Users must have the appropriate role to create and manage intelligent approvals. For role requirements, see [Intelligent approvals reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/build-workflows/reference-intelligent-approvals.md).


