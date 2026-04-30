---
title: Pipelines and Deployments configuration tasks
description: As you work through the Pipelines and Deployments guided setup, you must perform different configuration tasks on each of your instances.
locale: en-US
release: yokohama
product: App Engine Studio
classification: app-engine-studio
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 7
breadcrumb: [Configure Pipelines and Deployments, Configuring App Engine Studio and related apps, Build apps using App Engine Studio, Building low-code applications, Developing your application, Building applications]
---

# Pipelines and Deployments configuration tasks

As you work through the Pipelines and Deployments guided setup, you must perform different configuration tasks on each of your instances.

## Setting up environments, pipeline records, and user access

The tasks for configuring Pipelines and Deployments are listed below, along with links to detailed instructions for completing them. These tasks build on each other, so it's important to complete them in the sequence listed in the Guided Setup.

<table id="table_lqq_1qt_rhb"><thead><tr><th>

Instance

</th><th>

Task

</th><th>

Description

</th></tr></thead><tbody><tr><td rowspan="7">

Production

</td><td>

Configure environment credentials.

</td><td>

Configure credentials for each instance in your pipeline so that the flows used by AEMC can access the instances in your pipelines.For more information, see [Configure environment credentials](../task/create-pipeline-credentials.md).

</td></tr><tr><td>

Configure environments.

</td><td>

Set up your production and non-production \(that is, development, test, and/or staging\) environments by adding the URLs and credentials used to access each instance.For more information, see [Configure your pipeline environments](../task/config-pipeline-environments.md).

</td></tr><tr><td>

Configure pipelines.

</td><td>

Set up and configure each pipeline by naming the pipeline, identifying each of the environments associated with the pipeline, and specifying the order in which apps are deployed between the environments in that pipeline.For more information, see [Configure your pipeline](../task/config-pipeline.md).

</td></tr><tr><td>

Add users to the App Engine admin group.

</td><td>

Add users involved with this flow of tasks to the App Engine admin group.**Note:** If already added users on the production instance using [AES guided setup](../../app-engine-studio/concept/configure-aes.md) or [Configure Application Intake](../../app-engine-studio/task/config-app-intake.md) guided setup, you can skip this step.

For more information, see [Add users to the App Engine Admin group](../../app-engine-studio/task/add-users-to-admin-grp.md).

</td></tr><tr><td>

Add Automated Test Framework \(ATF\) and Instance Scan suites.

</td><td>

Add your customized test suites as part of an application deployment in addition to the instance scan and ATF testing suites that are standard in AEMC.

 For more information, see [Add ATF and instance scan suites for testing](../../app-engine-studio/task/add-atf-instance-scan-suite-testing.md).

</td></tr><tr><td>

Enable Change Management integration

</td><td>

Connect an existing Change Management program with AEMC so that deployments through the pipeline to the production environment are automatically scheduled based on the Change request state and planned change window.

 For more information, see [Enable Change Management integration](../task/enable-change-management-integration.md).

</td></tr><tr><td>

Configure properties to integrate Change Management

</td><td>

Change requests and configuration items \(CIs\) are created using specifications set up in your existing Change Management program. If you want to change the change model, change template, or CI creation subflows used during app deployments, you must configure these properties during Guided Setup.

 For more information, see [Configure properties to integrate Change Management](../concept/configure-properties-integrate-cm.md#).

</td></tr><tr><td rowspan="5">

Testing

</td><td>

Configure environment credentials

</td><td>

For more information, see [Configure environment credentials](../task/create-pipeline-credentials.md).

</td></tr><tr><td>

Configure the controller instance

</td><td>

Identify the controller instance that contains the pipeline deployment flows, as well as all of the data associated with the pipeline. As each instance completes its assigned tasks, it communicates with the controller instance to determine where the next stage of deployment takes place.**Note:** Your production instance should be identified as the controller.

For more information, see [Configure your controller instance](../task/config-controller-instance.md).

</td></tr><tr><td>

Enable ATF properties on instances of type Testing.

</td><td>

Enable system properties that allow the ATF suite to run during the deployment process. If you do not enable these properties, a warning displays during the deployment process, but you can continue with the deployment.**Note:** If you plan on cloning your production instance to one or more non-production instances, you should either create a data preserver for these settings or enable these settings on your production instance. For more information, see [Create a clone preserver](https://www.servicenow.com/docs/access?context=create-new-clone-preserver&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

For more information, see [Enable Automated Test Framework \(ATF\) properties](../task/enable-atf-properties.md).

</td></tr><tr><td>

Configure Automated Test Framework \(ATF\) suite

</td><td>

For more information, see [Exploring Automated Test Framework](../../../administer/auto-test-framework/concept/automated-test-framework.md).

</td></tr><tr><td>

Configure Instance Scan suite

</td><td>

For more information, see [Configuring Instance Scan](https://www.servicenow.com/docs/access?context=hs-intro-scans&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

</td></tr><tr><td rowspan="2">

Non-production instances that aren’t of type Testing

</td><td>

Configure environment credentials

</td><td>

For more information, see [Configure environment credentials](../task/create-pipeline-credentials.md).

</td></tr><tr><td>

Configure the controller instance in your non-production instances

</td><td>

For more information, see [Configure properties to integrate Change Management](../concept/configure-properties-integrate-cm.md#).

</td></tr></tbody>
</table>-   **[Configure environment credentials](../task/create-pipeline-credentials.md)**  
Configure credentials in your production instance so that the flows used by the App Engine Management Center \(AEMC\) can access different instances.
-   **[Configure your pipeline environments](../task/config-pipeline-environments.md)**  
Set up your App Engine Studio \(AES\) production and non-production \(for example, development, test, and/or staging\) environments by adding the URLs and credentials used to access each instance.
-   **[Configure your pipeline](../task/config-pipeline.md)**  
Configure your App Engine Studio \(AES\) pipeline so that your administrator can quickly move an application from one environment to another.
-   **[Configure your controller instance](../task/config-controller-instance.md)**  
You must identify one of the instances in your App Engine Studio \(AES\) pipeline as the controller instance. All communication between the instances in your pipeline, including the deployment order for applications in the pipeline, takes place in the controller instance.
-   **[Add ATF and instance scan suites for testing](../../app-engine-studio/task/add-atf-instance-scan-suite-testing.md)**  
Add your customized test suites as part of an application deployment in addition to the instance scan and Automated Test Framework \(ATF\) testing suites that are standard in AEMC.
-   **[Enable Automated Test Framework \(ATF\) properties](../task/enable-atf-properties.md)**  
The App Engine Studio \(AES\) Pipelines and Deployments app includes an Application Test Framework \(ATF\) suite called the Application Deployment Test Suite. Two system properties control whether the test runs automatically whenever an app is deployed to a Test environment.
-   **[Enable Change Management integration](../task/enable-change-management-integration.md)**  
Enable Change Management integration with AEMC so that deployments through the pipeline to the production environment are automatically scheduled based on the Change request state and planned change window.
-   **[Configure properties to integrate Change Management](../concept/configure-properties-integrate-cm.md#)**  
Configure predefined properties through the Pipelines and Deployments Guided Setup to tailor your Change Management and AEMC integration to your company's needs. Configuring these properties is optional.

**Parent Topic:**[Configure Pipelines and Deployments](../task/config-p-and-d.md)

