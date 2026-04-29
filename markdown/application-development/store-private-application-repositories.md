---
title: The ServiceNow Store and private application repositories
description: The ServiceNow Store provides two main repository mechanisms for application distribution: the ServiceNow Store and private \(company\) application repositories.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Deployment, Getting Started guide for developers, Building applications]
---

# The ServiceNow Store and private application repositories

The ServiceNow Store provides two main repository mechanisms for application distribution: the ServiceNow® Store and private \(company\) application repositories.

-   **ServiceNow® Store**

    The ServiceNow® Store is the public marketplace where ServiceNow and certified partners publish applications. Store applications are installed through the Application Manager and receive updates through the same channel. You do not publish your custom applications unless you're a certified ISV partner.

-   **Private Application Repository**

    A private application repository is your company’s internal repository, shared across all connected instances. When you publish a scoped application from ServiceNow Studio, it is stored in the application repository. Connected non-production and production instances can then install or upgrade to specific versions. The application repository tracks version history, handles dependency resolution, and protects instance-specific settings \(like private system properties\) from being overwritten during installation.


## How does the Application Repository work?

-   Develop your scoped application in development using ServiceNow Studio or App Engine Studio.
-   Publish a versioned release to the application repository, such as v1.0.0, v1.1.0.
-   On the target instance \(test or production\), navigate to Application Manager and install the desired version.
-   Review the skip logs for any records that were protected from overwrite due to local modifications.

**Important:** Do not mix Application Repository and System Update Sets deployment methods for the same application. Combining these approaches may cause skipped changes, commit errors, and version tracking failures.

## Security considerations for repositories

The Application Repository respects cross-scope access privileges, which means an installed application on production cannot be edited in the ServiceNow Studio. It can only be updated through a new published version.

This is a critical security control that helps prevent unauthorized modifications in production. Confirm that only authorized developers have the admin or application\_creator roles needed to publish to the Application Repository in development.

**Parent Topic:**[Deployment](get-started-deployment.md)

