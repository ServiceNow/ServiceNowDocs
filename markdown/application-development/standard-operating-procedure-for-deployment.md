---
title: Standard operating procedure for deployment
description: Every ServiceNow organization should have a documented deployment standard operating procedure. The procedure should specify the approved method for orchestrating deployments, the pipeline stages and approval gates, and the roles authorized to perform deployments.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Deployment, Getting Started guide for developers, Building applications]
---

# Standard operating procedure for deployment

Every ServiceNow organization should have a documented deployment standard operating procedure. The procedure should specify the approved method for orchestrating deployments, the pipeline stages and approval gates, and the roles authorized to perform deployments.

## Pre-deployment checklist

-   Confirm your organization’s approved deployment method with your platform owner or release manager. The approved methods include ReleaseOps, App Engine Management Center Pipelines and Deployments, and System Update Sets. For more information, see [Deployment management options](management-options.md).
-   Run Instance Scan against your application to check for security violations, coding standard issues, and guideline deviations.
-   Execute all Automated Test Framework suites and verify they pass.
-   Review access control lists \(ACLs\) to confirm they follow least-privilege principles with no empty or overly permissive rules.
-   Verify that credentials, API keys, and environment-specific properties are isolated using private system properties.
-   Submit and obtain required change request approvals according to your organization’s change management process.
-   Deploy to non-production first, validate thoroughly, then promote to production only after all quality gates pass.

## Deployment pipeline security

Your deployment standard operating procedure should explicitly address the following security requirements:

-   **Multifactor authentication \(MFA\)**

    Use multifactor authentication for all interactive accounts that perform deployments.

-   **IP allow listing**

    Use IP allow listing for service accounts used in automated pipelines.

-   **Credential rotation schedules**

    Use credential rotation schedules for integration accounts.

-   **Audit logging**

    Use audit logging of all deployment actions.

-   **Rollback procedures**

    Use rollback procedures in case a deployment introduces a security regression.


**Parent Topic:**[Deployment](get-started-deployment.md)

