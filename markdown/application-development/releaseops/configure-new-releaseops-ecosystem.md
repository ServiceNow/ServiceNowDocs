---
title: Complete ReleaseOps manual setup
description: Complete ReleaseOps manual setup to configure a new ReleaseOps ecosystem using the sample pipelines and playbooks.
locale: en-US
release: australia
product: ReleaseOps
classification: releaseops
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [ReleaseOps, deploy changes, update sets, pipeline, ATF, schedule a release, deployment request, deployment analyzer, configure ReleaseOps]
breadcrumb: [Configure, ReleaseOps, Deploying applications, Building applications]
---

# Complete ReleaseOps manual setup

Complete ReleaseOps manual setup to configure a new ReleaseOps ecosystem using the sample pipelines and playbooks.

## About this task

Starting with version 1.2.1 of ReleaseOps, you can use guided setup for a quicker initial configuration experience. For more information, see [Complete ReleaseOps guided setup](complete-guided-setup.md).

The manual setup procedure outlined in this task can also be used to complete ReleaseOps initial configuration. Manual setup can be useful in more complex setup scenarios and when making changes to your existing ReleaseOps ecosystem.

## Before you begin

Role required: admin or sn\_releaseops.releaseops\_pipeline\_admin

Confirm that all instances \(production, development, and test\) have ReleaseOps installed. Your test instance must also have ATF Test Generator and Cloud Runner installed. For more information, see [Install ReleaseOps](install-releaseops.md).

Confirm that multi-instance management has been configured to enable all non-production instances \(development and test\) to be managed by the production instance. For more information, see [Configure multi-instance management for instances using ReleaseOps](configure-mif.md).

## Procedure

1.  On your production instance, create a deployment instance record for each instance that you want to participate in your ReleaseOps ecosystem.

    **Note:** For the ReleaseOps sample release pipelines, the three instances are:

    -   Development
    -   Test
    -   Production
    1.  Navigate to **All** &gt; **ReleaseOps** &gt; **Deployment Instances**.

    2.  Add a new record for each instance that participates in your ReleaseOps ecosystem by selecting **New**.

    3.  Select the **Instance** field, then select the instance that you want to add to your ReleaseOps ecosystem.

    4.  Select the **Instance type** field, then select the correct instance type from the list.

    5.  Select **Submit**.

    6.  Repeat steps b-e for each instance that participates in your ReleaseOps ecosystem.

2.  On your production instance, configure the test instance for both the sample On Demand Pipeline and sample Release Pipeline.

    For sample ReleaseOps pipelines, you must only configure a new pipeline instance for your test instance. You don’t need to configure pipeline instances for your development and production instances, because these environments are defined within deployment requests and releases.

    For custom ReleaseOps pipelines, you can configure additional pipeline instances for the non-production instances that participate in your ReleaseOps ecosystem, excluding your development instance. For more information about custom pipelines, see [Create a custom pipeline](create-release-ops-pipeline.md#).

    1.  Navigate to **All** &gt; **ReleaseOps** &gt; **Pipelines**.

    2.  Select one of the sample pipeline records from the list.

    3.  On the pipeline record, select the **Pipeline instances** tab in the Related Links section.

        ![You can configure your pipeline instances by selecting the Pipeline instances tab on the pipeline record.](../image/releaseops-pipeline-instances-list.png)

    4.  On the **Pipeline instances** tab, select **New**.

    5.  On the new pipeline instance form, select the Lookup using list icon \(![](../../../administer/ui-builder/image/lookup-using-list-icon.png)\) for the **Deployment instance** field, then select the test instance from the list.

    6.  In the **Label** field, select **Test**.

    7.  Select **Submit**.

    8.  Repeat the process in steps b-g to configure test instances for each of your sample pipelines.

3.  On your production instance, navigate to **All** &gt; **System Update Sets** &gt; **Update Sources** and verify that there are valid update sources defined for both your development and test instances.

    ![Verify that there are valid update sources defined for both your development and test instances.](../image/releaseops-update-sources.png)

    **Note:** If there aren't valid update sources defined for both your development and test instances, you can define them by navigating to **All** &gt; **System Update Sets** &gt; **Update Sources** on your development and test instances and creating a new update source record.

4.  On your test instance, navigate to **All** &gt; **System Update Sets** &gt; **Update Sources** and confirm that there’s a valid update source defined for your development instance.

5.  On your development instance, set the property **sn\_releaseops.deployment\_controller** to the production \(or deployment controller\) URL.

    1.  Navigate to **All** &gt; **System Properties** &gt; **All**.

    2.  Using the search bar, enter `**sn\_releaseops.deployment\_controller**`.

        ![Use the search bar to search for the sn_releaseops.deployment_controller system property.](../image/releaseops-system-properties-deployment-controller.png)

    3.  Select the record for **sn\_releaseops.deployment\_controller**.

    4.  In the **Value** field, enter the URL for your production \(or deployment controller\) instance.

    5.  Select **Update**.


## Result

ReleaseOps is ready to deploy changes from your development to test to production instances.

