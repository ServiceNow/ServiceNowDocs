---
title: Migrating App Engine pipelines to ReleaseOps
description: Starting with version 28.2.1 of AEMC, you can migrate your existing App Engine pipelines to ReleaseOps. Learn more about the migration process and benefits of migrating to ReleaseOps.
locale: en-US
release: australia
product: App Engine Management Center
classification: app-engine-management-center
topic_type: concept
last_updated: "2025-10-15"
reading_time_minutes: 2
breadcrumb: [Explore, App Engine Management Center, Governing app development, Building applications]
---

# Migrating App Engine pipelines to ReleaseOps

Starting with version 28.2.1 of AEMC, you can migrate your existing App Engine pipelines to ReleaseOps. Learn more about the migration process and benefits of migrating to ReleaseOps.

When you migrate to ReleaseOps, you enable ReleaseOps to handle the deployment process in the background without disrupting your existing App Engine pipeline. Developers submit applications in their development environments as before. But with migration enabled, a corresponding ReleaseOps deployment request is created at the time of application submission, which enables ReleaseOps to orchestrate the deployment process. To learn more about the deployment process, see [Deployment process in AEMC](deployment-process-aemc.md).

## Benefits of migration

Migrating an App Engine pipeline to ReleaseOps enables you to take advantage of ReleaseOps features without disrupting your existing App Engine pipeline or deployment process. This approach is helpful if you want to:

-   Evaluate ReleaseOps before fully adopting it.
-   Continue using the Application Repository for deployments.
-   Deploy with ReleaseOps in environments where full support isn’t available yet, such as App Engine Studio and Creator Studio.

## Migration process overview

To migrate to ReleaseOps, you must have ReleaseOps installed and configured on each instance in your App Engine pipeline. Once you have configured ReleaseOps and the system property to enable migration, developers initiate deployment as usual. However, with migration enabled, deployment is handled by ReleaseOps in the background. The following list outlines the entire process for migrating to ReleaseOps:

1.  [Install ReleaseOps](../../release-ops/task/install-releaseops.md) on each environment \(instance\) in your App Engine pipeline.
2.  Complete ReleaseOps setup by [configuring a new ReleaseOps ecosystem](../../release-ops/task/configure-new-releaseops-ecosystem.md) and [configuring multi-instance management](../../release-ops/task/configure-mif.md).
3.  [Configure the system property to enable migration to ReleaseOps](../task/configure-sys-property-for-migration-to-releaseops-aemc.md).
4.  [Map deployment request states](../task/map-deployment-request-states-aemc.md) if you’re using custom deployment request states in your ReleaseOps pipeline. Base system ReleaseOps deployment request states will automatically map onto the corresponding App Engine deployment request states.
5.  If you want to add additional conditions to enable ReleaseOps migration, you can set up [custom conditions in Workflow Studio](../task/add-custom-conditions-to-enable-releaseops-deployment.md). For example, you might want only deployments for certain applications to migrate to ReleaseOps. So you can set up a condition that checks if the deployment request is from that specific application.

Once you have migrated to ReleaseOps, ReleaseOps handles the deployment process in the background. To learn more about the deployment process after migrating to ReleaseOps, see [Deployment process in AEMC](deployment-process-aemc.md).

