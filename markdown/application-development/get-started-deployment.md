---
title: Deployment
description: Deploying custom applications from development to non-production and production instances is one of the most critical processes in ServiceNow platform management. Knowing the ServiceNow application deployment life cycle, including migration methods, security considerations, and organizational best practices ensures stability, security, and traceability.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Getting Started guide for developers, Building applications]
---

# Deployment

Deploying custom applications from development to non-production and production instances is one of the most critical processes in ServiceNow platform management. Knowing the ServiceNow application deployment life cycle, including migration methods, security considerations, and organizational best practices ensures stability, security, and traceability.

## Key ideas for your deployment

-   Use application-scoped deployments and source control over update sets whenever possible.
-   Leverage ReleaseOps, App Engine Management Center/Pipelines and Deployments, or System Update Sets depending on your organization's chosen management method.
-   Always test in non-production before deploying to production.
-   Implement access control lists \(ACLs\), role-based access control, and Instance Scan checks as part of every deployment.
-   Find out what your platform owner has standardized and follow that protocol.

-   **[Moving applications between instances](moving-applications-between-instances.md)**  
ServiceNow applications are built in Development instances, then promoted through Test and Production environments using update sets or the Application Repository to package and migrate changes. This multi-instance workflow ensures applications are thoroughly tested before reaching end users in Production.
-   **[The ServiceNow Store and private application repositories](store-private-application-repositories.md)**  
The ServiceNow Store provides two main repository mechanisms for application distribution: the ServiceNow® Store and private \(company\) application repositories.
-   **[Managing application versions](managing-application-versions.md)**  
Semantic versioning \(Major.Minor.Patch\) is the standard approach for ServiceNow applications. Each time you publish from ServiceNow Studio, you assign a version number, which gives your team a clear audit trail of all changes.
-   **[Deployment management options](management-options.md)**  
ServiceNow offers multiple management options for orchestrating deployments. Your choice depends on your organization’s maturity, licensing, and operational preferences. You can choose between ReleaseOps, App Engine Management Center Pipelines and Deployments, or System Update Sets.
-   **[Standard operating procedure for deployment](standard-operating-procedure-for-deployment.md)**  
Every ServiceNow organization should have a documented deployment standard operating procedure. The procedure should specify the approved method for orchestrating deployments, the pipeline stages and approval gates, and the roles authorized to perform deployments.
-   **[Guidelines for using source control](best-practices-use-source-control.md)**  
Source control \(Git\) combined with the Application Repository is the preferred deployment method for custom scoped applications. Using System Update Sets is also an approved deployment mechanism for application development.

**Parent Topic:**[Getting Started guide for developers](getting-started-landing-page.md)

