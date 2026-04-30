---
title: Create an application in DevOps Config
description: Create an app in DevOps Config to manage its configuration data, and link DevOps Config with other ServiceNow products, including DevOps Change Velocity.
locale: en-US
release: yokohama
product: DevOps \(Family\)
classification: devops-family
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configure, DevOps Config, IT Service Management]
---

# Create an application in DevOps Config

Create an app in DevOps Config to manage its configuration data, and link DevOps Config with other ServiceNow products, including DevOps Change Velocity.

## Before you begin

**Important:** DevOps Config is now deprecated and no longer supported or available for new activation.

An admin can create, edit, delete, and view DevOps Config apps.

Role required: sn\_devops\_config.admin

## About this task

Watch this short video to see how to create an application in DevOps Config.

Create an application in DevOps Config

An app in DevOps Config is the container for the config data of an application. An app also ties it with the DevOps Change Velocity application, where configuration data can be viewed in the DevOps Pipeline UI.

In DevOps Change Velocity, an app links work items, code commits and CI/CD pipeline executions together in the DevOps data model, which is displayed in change request, as well as the DevOps Insights dashboard.

Apps in the DevOps Config application and in the DevOps Change Velocity application are synced. Meaning, when an app is created in DevOps Config, it is also created in DevOps Change Velocity, if installed, and vice versa.

You can edit or delete apps in DevOps Config. When you delete an app:

-   In DevOps Config, the state of the application is set to **Inactive** and is no longer accessible in DevOps Config.
-   In DevOps Change Velocity, it's also deleted in DevOps Config \(if installed\).

## Procedure

1.  Navigate to **All** &gt; **DevOps Config** &gt; **DevOps Config Workspace**.

2.  Click the apps icon \(![DevOps Config apps icon](../image/devops-config-apps-icon.png)\) in the left navigation to open the Apps tab.

3.  On the Applications form, click **New** to create an application and a new model, or to create an application and specify an existing model \(or service\).

    ![DevOps Config create application](../image/devops-config-create-app.png)

    For a **New application** without an existing application model, both application and model are created.

    For a new application to be tied to an **Existing application model or service**, only the application is created.

    The CSDM application model \(name, owner, manufacturer\) functions as the link between ServiceNow DevOps products. There is an SDLC Component of the CMDB for each CSDM application model.

4.  In the **Overview** tab, fill in the Application details and select **Save**.

<table id="table_nzd_ntm_psb"><tbody><tr><td>

Maintained by

</td><td>

User groups that maintain the application.With the cdm\_admin role, you can add or remove any user groups.

If groups you're a member of are removed, you will lose access to the application.

**Note:** A user with cdm\_all\_app\_access and one of the other roles \(cdm\_admin, cdm\_editor, or cdm\_viewer\) can see and manage the application even if they are not in those groups. For more information, see [Roles in CDM](../../configuration-data-management/reference/cdm-roles.md).

</td></tr><tr><td>

Application description

</td><td>

Description of the application.

</td></tr><tr><td>

Application model owner

</td><td>

Username who owns the application model.

</td></tr><tr><td>

Manufacturer

</td><td>

Manufacturer of the application.

</td></tr></tbody>
</table>    The application does not yet contain config data, so the next step is to import your existing config data into the application.

    After you have imported config data and snapshots are generated, the list of snapshots are displayed in the **Overview** tab.


## Example

![DevOps Config app overview](../image/devops-config-app-overview.png "DevOps Config App Overview")

