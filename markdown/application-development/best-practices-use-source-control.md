---
title: Guidelines for using source control
description: Source control \(Git\) combined with the Application Repository is the preferred deployment method for custom scoped applications. Using System Update Sets is also an approved deployment mechanism for application development.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Deployment, Getting Started guide for developers, Building applications]
---

# Guidelines for using source control

Source control \(Git\) combined with the Application Repository is the preferred deployment method for custom scoped applications. Using System Update Sets is also an approved deployment mechanism for application development.

## Why use source control?

-   **Full change history**

    Git provides a complete, auditable record of every change, such as who made it, when, and why, with the ability to use diff, review, and revert functions at the individual file level.

-   **Branching and parallel development**

    Multiple developers can work on different features simultaneously without conflicting update sets.

-   **Code review workflows**

    Pull requests and merge reviews enforce peer review before any change is published, reducing errors and security oversights.

-   **Versioned releases**

    Tags and branches map directly to Application Repository versions, enabling reliable rollbacks and hotfix workflows.

-   **CI/CD integration**

    External CI/CD tools such as Jenkins, GitHub Actions, and Azure DevOps can trigger builds, tests, and deployments using the ServiceNow SDK and CLI.


## When are System Update Sets appropriate?

System Update Sets retain value for quick operational changes to the following:

-   Global-scope configurations.
-   Emergency hotfixes when the full source control pipeline would introduce unacceptable delay.
-   Organizations still transitioning from legacy development practices.
-   Changes to ServiceNow® Store or plugin applications where the Application Repository workflow doesn’t apply natively.

Even in these scenarios, consider using Instance Scan checks on your System Update Sets before committing them, and batch related update sets to reduce deployment complexity.

## Security guidelines

-   **Enforce least privilege through access control lists \(ACLs\)**

    Define custom application-specific roles rather than relying on broad system roles. Configure ACLs to use the evaluation order of roles first, then conditions, then scripts for optimal performance and security.

-   **Use deny-by-default**

    The glide.sm.default\_mode property should remain in **Deny** mode so that wildcard ACLs restrict access to admin-only by default.

-   **Run Instance Scan automatically**

    Configure Instance Scan to run against System Update Sets and application deployments. This catches empty ACLs, overly permissive access, and coding standard violations before they reach production.

-   **Protect cross-scope access**

    Configure application cross-scope access privileges deliberately. Do not default to open access for all scopes.

-   **Implement multi-factor authentication and IP restrictions**

    All interactive accounts performing deployments should use multi-factor authentication. Service accounts for automated deployments should be restricted by IP range and have tightly scoped roles.

-   **Audit everything**

    Use Access Analyzer to regularly review user, group, and role permissions. Forward deployment logs and Access Control activity to your SIEM platform for monitoring.

-   **Separate data from code**

    Application data records are not included in Application Repository deployments. Manage reference data and seed data through separate, controlled processes with appropriate data classification.


## Deployment method decision matrix

The following table shows the scenario and recommended deployment approach:

|Scenario|Recommended approach|
|--------|--------------------|
|New custom scoped application|Use source control + Application Repository + App Engine Management Center Pipelines and Deployments, or ReleaseOps.|
|Global scope configuration changes|Use System Update Sets with Instance Scan or global application using the Application Repository.|
|Emergency production hotfix|Use System Update Sets for speed and back port into source control \(Git\) immediately after.|
|Citizen developer app from App Engine Studio|Use App Engine Management Center Pipelines and Deployments with a guided approval workflow.|
|Multi-team release coordination:|Use ReleaseOps with release trains and playbook validation.|

**Parent Topic:**[Deployment](get-started-deployment.md)

