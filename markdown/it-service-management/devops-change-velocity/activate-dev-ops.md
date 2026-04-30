---
title: Install DevOps Change Velocity
description: Install the DevOps Change Velocity application from the ServiceNow Store.
locale: en-US
release: xanadu
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configure, DevOps Change Velocity, IT Service Management]
---

# Install DevOps Change Velocity

Install the DevOps Change Velocity application from the ServiceNow Store.

## Before you begin

Role required: admin

Ensure that the application and all of its associated store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).

If you’re installing DevOps Change Velocity in your production instance for the first time, ensure that you opt-in to the following required products. For more information, see [Opt in to the ServiceNow Store products](https://www.servicenow.com/docs/access?context=optin-optout-prod&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

<table id="table_ux3_lfg_cyb"><tbody><tr><td>

Devops Change Velocity

</td><td>

[https://store.servicenow.com/sn\_appstore\_store.do\#!/store/product/e5ff61c51b345d50ee92cb31604bcba4](https://store.servicenow.com/sn_appstore_store.do#!/store/product/e5ff61c51b345d50ee92cb31604bcba4)

</td></tr><tr><td>

Playbook Experience

</td><td>

[https://store.servicenow.com/sn\_appstore\_store.do\#!/store/product/e4cecaf0db2be81079279ee4db9619f2](https://store.servicenow.com/sn_appstore_store.do#!/store/product/e4cecaf0db2be81079279ee4db9619f2)

</td></tr><tr><td>

CMDB CI Class Models

</td><td>

[https://store.servicenow.com/sn\_appstore\_store.do\#!/store/application/ae99d84b2320330006c0110d96bf65b3/1.45.1](https://store.servicenow.com/sn_appstore_store.do#!/store/application/ae99d84b2320330006c0110d96bf65b3/1.45.1)

</td></tr><tr><td>

Expanded Model and Asset Classes

</td><td>

[https://store.servicenow.com/sn\_appstore\_store.do\#!/store/application/7e67d4ff091b4110f87739da6a8d8c7d/2.1.0](https://store.servicenow.com/sn_appstore_store.do#!/store/application/7e67d4ff091b4110f87739da6a8d8c7d/2.1.0)

</td></tr><tr><td>

Universal Task

</td><td>

[https://store.servicenow.com/sn\_appstore\_store.do\#!/store/application/e09af33a533d10103a80ddeeff7b1247/2.2.0](https://store.servicenow.com/sn_appstore_store.do#!/store/application/e09af33a533d10103a80ddeeff7b1247/2.2.0)

</td></tr><tr><td>

Jira Spoke

</td><td>

[https://store.servicenow.com/sn\_appstore\_store.do\#!/store/application/4fab4673db1893009a985404ce961942/4.1.0](https://store.servicenow.com/sn_appstore_store.do#!/store/application/4fab4673db1893009a985404ce961942/4.1.0)

</td></tr><tr><td>

GitHub Spoke

</td><td>

[https://store.servicenow.com/sn\_appstore\_store.do\#!/store/application/9a025c563b22330006f1600713efc4cf/2.2.6](https://store.servicenow.com/sn_appstore_store.do#!/store/application/9a025c563b22330006f1600713efc4cf/2.2.6)

</td></tr><tr><td>

Jenkins V2 Spoke

</td><td>

[https://store.servicenow.com/sn\_appstore\_store.do\#!/store/application/c66af1ca1b8a8c5033fbdbd3cc4bcb75/1.2.0](https://store.servicenow.com/sn_appstore_store.do#!/store/application/c66af1ca1b8a8c5033fbdbd3cc4bcb75/1.2.0)

</td></tr></tbody>
</table>## About this task

To install the DevOps application on a subprod instance, navigate to the DevOps Change Velocity app on the ServiceNow Store and select **Request Install** to send your request.

## Procedure

1.  Navigate to **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Select the **Not Installed** tab to view a list of applications available for installation.

3.  Find the DevOps Change Velocity application using the filter criteria and search bar.

    You can search for the application by its name or ID \(sn\_devops\_chgvlcty\). If you can’t find an application, you may have to request it from the ServiceNow store.

    Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release note information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

4.  Select **Install**.

5.  In the Application installation dialog box, review the application dependencies.

    If your application requires other applications, install them first if they are not already installed.

    Installing your application also automatically installs the dependent applications or plugins if they aren’t installed already.

6.  If you want to install demo data, select **Load demo data**.

    Demo data includes sample records that describe application features for common use cases. Load demo data when you first install the application on a development or test instance.

    **Note:** If you don't load the demo data for a store application during installation, you can’t load it later.

7.  Select **Install**.

    Based on your connection, the installation procedure can take almost an hour or more to complete.


## Result

Installing DevOps Change Velocity also installs the dependent applications, user roles, tables, scheduled jobs, and other components.

See [Components installed with DevOps Change Velocity](../reference/installed-with-dev-ops.md).

## What to do next

[Assign roles and tasks using workspace](assign-roles-tasks-workspace.md).

**Note:** Roles that are installed with DevOps Change Velocity are listed in [Components installed with DevOps Change Velocity](../reference/installed-with-dev-ops.md).

