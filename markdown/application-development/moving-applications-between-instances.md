---
title: Moving applications between instances
description: ServiceNow applications are built in Development instances, then promoted through Test and Production environments using update sets or the Application Repository to package and migrate changes. This multi-instance workflow ensures applications are thoroughly tested before reaching end users in Production.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Deployment, Getting Started guide for developers, Building applications]
---

# Moving applications between instances

ServiceNow applications are built in Development instances, then promoted through Test and Production environments using update sets or the Application Repository to package and migrate changes. This multi-instance workflow ensures applications are thoroughly tested before reaching end users in Production.

## Instance types

Development environments typically follow a multi-instance architecture. Each instance serves a distinct purpose in the application life cycle.

-   Development \(DEV\): Build and iterate apps.
-   Testing/QA \(TEST\): Validate and test changes.
-   Staging/UAT \(STAGE\): Validate and test changes.
-   Production \(PROD\): Live environment that powers daily business operations.

## Core principle

The core principle is straightforward: never develop directly in production. All configuration and code changes originate in DEV, flow through one or more non-production validation stages, and arrive in PROD only after passing quality checks including automated testing, Instance Scan checks, and stakeholder approvals.

When moving an application, every artifact associated with that application scope—business rules, script includes, UI pages, ACLs, tables, flows, and so on must travel together as a coherent unit. Partial deployments create version mismatches and are a leading source of production incidents.

## Security considerations for instance movement

-   **Credential isolation**

    Integration credentials, API keys, and OAuth tokens must never be promoted from development to production. Use system properties marked as private or environment-specific credential stores.

-   **ACL validation**

    Run Instance Scan on every deployment to verify that ACLs follow least-privilege principles. Empty or overly permissive ACLs are a common security gap.

-   **Role separation**

    Developers should not have admin access in production. Use dedicated deployment service accounts with only the roles necessary to install applications.

-   **Data protection**

    Confirm that test data in non-production does not contain unmasked production PII. Use data masking or anonymization during clone operations.


**Parent Topic:**[Deployment](get-started-deployment.md)

