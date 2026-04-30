---
title: Migration tasks
description: You must complete several tasks to migrate your App Engine pipelines to ReleaseOps.
locale: en-US
release: zurich
product: App Engine Management Center
classification: app-engine-management-center
topic_type: concept
last_updated: "2025-10-16"
reading_time_minutes: 1
breadcrumb: [Configure Pipelines and Deployments, Configure, App Engine Management Center, Governing app development, Building applications]
---

# Migration tasks

You must complete several tasks to migrate your App Engine pipelines to ReleaseOps.

Starting with version 28.2.1 of AEMC, you can migrate your existing pipelines to ReleaseOps. To learn more about the migration process and the advantages of migrating to ReleaseOps, see [Migrating App Engine pipelines to ReleaseOps](migrating-ae-pipelines-to-releaseops-aemc.md). To start migrating your existing pipelines, complete each of the following procedures.

1.  [Install ReleaseOps](../../release-ops/task/install-releaseops.md) on each environment \(instance\) in your App Engine pipeline.
2.  Complete ReleaseOps setup by [configuring a new ReleaseOps ecosystem](../../release-ops/task/configure-new-releaseops-ecosystem.md) and [configuring multi-instance management](../../release-ops/task/configure-mif.md).
3.  [Configure the system property to enable migration to ReleaseOps](../task/configure-sys-property-for-migration-to-releaseops-aemc.md).
4.  [Map deployment request states](../task/map-deployment-request-states-aemc.md) to match ReleaseOps deployment request states to the corresponding App Engine deployment request states.
5.  [Add custom conditions to enable ReleaseOps deployments](../task/add-custom-conditions-to-enable-releaseops-deployment.md) in Workflow Studio.

