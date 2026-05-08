---
title: Configure properties to integrate Change Management
description: Configure predefined properties through the Pipelines and Deployments Guided Setup to tailor your Change Management and AEMC integration to your company's needs. Configuring these properties is optional.Configure the change model you would like to use during application deployments. If not configured, the Normal change model is used by default.Configure the default change template used to create change requests during application deployments.Customize how Configuration Items \(CIs\) are created during application deployment using AEMC.
locale: en-US
release: australia
product: App Engine Management Center
classification: app-engine-management-center
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Configuration tasks, Configure Pipelines and Deployments, Configure, App Engine Management Center, Governing app development, Building applications]
---

# Configure properties to integrate Change Management

Configure predefined properties through the Pipelines and Deployments Guided Setup to tailor your Change Management and AEMC integration to your company's needs. Configuring these properties is optional.

## Configure the change model

Configure the change model you would like to use during application deployments. If not configured, the **Normal** change model is used by default.

### Before you begin

Role required: admin

### About this task

There are several change models you can use to tailor change activities and flows for specific use cases. For more information about each type of model, see Change models. Use the steps below to select which change model you would like to use during app deployments.

This task can be completed within the Guided Setup system. This task opens within Guided Setup when you select **Configure**. If you prefer, you can follow the instructions below to access the same configuration task outside of the Guided Setup.

### Procedure

1.  Navigate to the System Properties table by typing `sys_properties.list` in the navigation filter and pressing **Enter**.

2.  Locate the following property: sn\_deploy\_pipeline.change\_management.default.model.

    To change the value of this property, and therefore the model that's being used, you must identify the **sys\_id** of the change model you want to switch to.

    1.  Navigate to **All** &gt; **Change** &gt; **Administration** &gt; **Change Models**.

    2.  Select the Change model you want to make the default for app deployments \(for example, **Standard**\).

    3.  Right-click in the header bar for the record, and select **Copy sys\_id**.

3.  In the **sn\_deploy\_pipeline.change\_management.default.model** property, paste the sys\_id you have copied into the **Value** field, replacing its current contents.

4.  Select **Update**.

5.  In the Pipelines and Deployments Guided Setup, in the **Configure Change Model** section, select **Mark Complete**.


## Configure the change template

Configure the default change template used to create change requests during application deployments.

### Before you begin

Role required: admin

### About this task

There are several templates that you can choose from to use as the default template for creating change requests. For more information, see . Use the following steps to select which change template you would like to use during app deployments.

This task can be completed within the Guided Setup system. This task opens within Guided Setup when you select **Configure**. If you prefer, you can follow the instructions below to access the same configuration task outside of the Guided Setup.

### Procedure

1.  Navigate to the System Properties table by typing `sys_properties.list` in the navigation filter and pressing **Enter**.

2.  Locate the following property: sn\_deploy\_pipeline.change\_management.default.template.

    To change the value of this property, and therefore the default template used for change requests, you must identify the **sys\_id** of the referenced template in the change template that you want to switch to.

    1.  Navigate to **All** &gt; **Change** &gt; **Standard Change** &gt; **All Templates**.

    2.  Select the update personalized list icon \(![Update personalized list icon](../image/update-personalized-list-icon.png)\) from the list header.

    3.  In the Available column, select **Template** and use the move icon \(![Move icon](../../app-engine-studio/image/app-tutorial-move-right-icon.png)\) to add it to the Selected column.

    4.  Select **OK**.

    5.  Select the value in the **Template** field of the change template that you want to make the default for app deployments.

    6.  Right-click in the header bar for the template record and select **Copy sys\_id**.

3.  In the **sn\_deploy\_pipeline.change\_management.default.template** property, paste the sys\_id that you have copied into the **Value** field, replacing its current contents.

4.  Select **Update**.

5.  In the Pipelines and Deployments Guided Setup, in the **Configure Change Template** section, select **Mark Complete**.


## Configure CI creation subflow

Customize how Configuration Items \(CIs\) are created during application deployment using AEMC.

### Before you begin

Role required: admin

### About this task

By default, the **Create CMDB CI if not present** subflow will run automatically during deployment to create a CI if for your application if it doesn't exist. However, you can change how Configuration Items \(CIs\) are created during deployment by using the following steps.

### Procedure

1.  Navigate to the System Properties table by typing `sys_properties.list` in the navigation filter and pressing **Enter**.

2.  Locate the following property: sn\_deploy\_pipeline.change\_management.config\_ci\_creation\_subflow.

    To change the value of this property, and therefore the template that's being used, you must identify the **sys\_id** of the subflow you want to switch to.

    1.  Navigate to **All** &gt; **Flow Designer**.

    2.  Select the update personalized list icon \(![](../image/update-personalized-list-icon.png)\) from the list header.

    3.  In the Available column, select **Template** and use the move icon \(![](../../app-engine-studio/image/app-tutorial-move-right-icon.png)\) to add it to the Selected column.

    4.  Select the More Actions menu icon \(![](../../../administer/ui-builder/image/MoreActionsIcon.png)\), and select **Copy subflow**.

    5.  Enter a name for the subflow, and make sure the application is in the **Deployment Pipeline** scope.

    6.  Select **Copy**.

    7.  Modify the subflow, and select **Save**.

    8.  To find the sys\_id of the subflow, select the More Actions menu icon \(![](../../../administer/ui-builder/image/MoreActionsIcon.png)\), and select **Executions**.

    9.  Copy the sys\_id.

        The sys\_id is listed at the top of the page, after **All&gt; Flow=**.

        ![Subflow's sys_id](../image/subflow-sys-id.png)

3.  In the **sn\_deploy\_pipeline.change\_management.config\_ci\_creation\_subflow** property, paste the sys\_id you have copied into the **Value** field, replacing its current contents.

4.  Select **Update**.

5.  In the Pipelines and Deployments Guided Setup, in the **Configure CI Creation Subflow** section, select **Mark Complete**.


