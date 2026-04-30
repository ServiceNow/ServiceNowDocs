---
title: Configure the system property to enable migration to ReleaseOps
description: Update the sn\_deploy\_pipeline.migrate\_releaseops system property to enable deployments using ReleaseOps.
locale: en-US
release: zurich
product: App Engine Management Center
classification: app-engine-management-center
topic_type: task
last_updated: "2025-10-22"
reading_time_minutes: 1
breadcrumb: [Migration tasks, Configure Pipelines and Deployments, Configure, App Engine Management Center, Governing app development, Building applications]
---

# Configure the system property to enable migration to ReleaseOps

Update the **sn\_deploy\_pipeline.migrate\_releaseops** system property to enable deployments using ReleaseOps.

## Before you begin

Role required: admin or app\_engine\_admin

You must have ReleaseOps installed and set up on your production and other pipeline environments to complete the following procedure. See [Migrating App Engine pipelines to ReleaseOps](../concept/migrating-ae-pipelines-to-releaseops-aemc.md) for more information.

## Procedure

1.  On your production instance, navigate to **All** &gt; **System Properties** &gt; **All Properties**.

2.  In the search bar, enter `sn_deploy_pipeline.migrate_releaseops` and select the Enter key.

3.  Select the **sn\_deploy\_pipeline.migrate\_releaseops** property from the list.

    **Note:** By default, the **sn\_deploy\_pipeline.migrate\_releaseops** property value is set to false.

4.  If you aren’t in the correct application scope, select the link to open the record in the correct scope.

5.  In the **Value** field, enter `true`.

    ![Set the system property to enable migration to ReleaseOps.](../image/aemc-system-property-enable-migration.png)

6.  Select **Update** or select and hold \(or right-click\) in the header and select **Save** to update the record.


## Result

You have set the **sn\_deploy\_pipeline.migrate\_releaseops** system property to enable migration to ReleaseOps.

## What to do next

If you customized your ReleaseOps deployment request states, you must map the deployment request states onto the corresponding App Engine deployment request states. See [Map deployment request states](map-deployment-request-states-aemc.md) for more information.

