---
title: Deploying what you built with Autonomous Engineer
description: When all work items are complete, Autonomous Engineer generates an update set that you export and move through the standard ServiceNow deployment process.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ae-deployment.html
release: brazil
topic_type: concept
last_updated: "2026-09-21"
reading_time_minutes: 1
keywords: [Autonomous Engineer, deployment, update sets, App Repository, App Engine Management Center, ReleaseOps]
breadcrumb: [Use, Autonomous Engineer, Agentic development on the ServiceNow AI Platform, Building applications]
---

# Deploying what you built with Autonomous Engineer

When all work items are complete, Autonomous Engineer generates an update set that you export and move through the standard ServiceNow deployment process.

## Workflow for deployment

Autonomous Engineer generates a single batch update set for the plan when all work items reach a complete state. First, export the update set from the plan dashboard. Then deploy it to a test environment for user acceptance testing, or promote it to production using your standard ServiceNow deployment process.

**Important:** Changes are isolated until you explicitly deploy and install the application. In ServiceNow Studio, changes are tracked in update sets and promoted when you move the update set between instances.

## Deployment methods for Autonomous Engineer

Autonomous Engineer supports update sets and application packaging for moving apps from development to production.

-   Pack update sets into scoped applications for easier transport and installation across instances, for example using Application Repository \(AppRepo\). For more information, see [ServiceNow application repository](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/application-repository-self-hosted/app-repo.md).
-   For information on update sets for Autonomous Engineer, see [Update sets and Autonomous Engineer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ae-update-sets.md).
-   For more information on System Update Sets, see [System update sets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/system-update-sets/system-update-sets.md).

**Parent Topic:**[Using Autonomous Engineer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ae-using-autonomous-engineer.md)

