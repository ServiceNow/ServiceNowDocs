---
title: Understand the Configuration page flow in Now Assist for Setup
description: Implement the following steps to understand the configuration page flow to start the configuration process for either the Platform module or a specific product module on your instance.
locale: en-US
release: australia
topic_type: task
last_updated: "2025-12-04"
reading_time_minutes: 4
breadcrumb: [Configure, Now Assist for Setup, Get started, Administer the ServiceNow AI Platform]
---

# Understand the Configuration page flow in Now Assist for Setup

Implement the following steps to understand the configuration page flow to start the configuration process for either the Platform module or a specific product module on your instance.

## Before you begin

Before performing this task, you must install Now Assist for Setup from the ServiceNow store, and setup the application you want to configure.

Role required: admin

## Procedure

1.  Once the setup of an application completes, select **Configure**.

    **Note:** The **Configure** option shows up only after the setup of an application completes.

    The Configuration Console page shows up.

    ![Image showing config page](../image/ia-config-page.png)

2.  Select Configuration Summary on the left panel of the Configuration Console page.

    You can see the modules and their specific configuration progress.

    **Note:** If the selected product module has enabled the update set functionality, a batch update set is created in the preferred scope that has been provided at the console level. This information shows up at the top menu bar on loading the Configuration Console page. Any update or metadata changes made on the console are captured in this update set unless you move to a different application or have switched to a different update set.

    The preferred scope can be updated depending on the next selected console item. For example, if you want to configure the Branding console item and it can be done in Global scope, you can override the preferred scope that was provided at the console level.

    The Platform module and the product specific module show up. The Platform module is a common module for all product modules. The product modules are based on the entitlement of the admin.

3.  Select **Get Started** on the modules.

    You are redirected to the first configuration of the selected module. See [Platform module configuration in Now Assist for Setup](../reference/ia-config-platform-il.md) for more information on Platform configuration steps.

4.  Expand the left panel configurations to view the pre-configured configurations.

    **Note:** The configurations that are pre-configured are marked with a checkmark. You can modify the default configurations that are preconfigured and marked with a Magic icon.

5.  Select a configuration that needs to be configured.

    Select each individual configurations that aren't pre-configured and complete the configurations.

    **Note:** Every application has different configurations that are either pre-configured or need to be configured.

6.  Select **Package and download** to consider all the update made in configuring the selected console item.

    This step packages the current batch of configuration changes into an update set XML file. A new XML file is created every time you make any configuration changes.

    **Note:** This step is applicable if you have selected either ITSM or CSM as the product module.

7.  Select **Configure with Now Assist** to start the configuration using Now Assist agent.

    **Note:** As a pre-req, install Now Assist for Setup \(app-ia-now-assist\) app for the **Configure with Now Assist** button to show up on the Configuration Console page.

    The Now Assist agent shows up and starts the configuration process.

    **Note:** The **Configure with Now Assist** button appears only for console items that are backed by AI capabilities.

8.  Select **Download XML** to download the XML update set batch file.

    You can also select **Back to configuration summary** to go back to the Configuration Console page.

9.  Review the labels and icons next to some selected console items.

    -   The Label icon indicates that the particular console item is either mandatory or recommended.
    -   The Update label indicates that the particular console item has been updated by the selected product family.
    -   The New label indicates that the particular console item is new.
    -   The Lock icon indicates that there is a pre-requisite that needs to be completed before unlocking the particular console item.

        **Note:** The Lock icon disappears as soon as the pre-requisite console item is marked as completed.

    If a new update is available, the system displays a banner on the Configuration Console page.

10. Select **Mark as configured** when you complete the configuration process of a configuration.

11. Scroll down to the Configuration activity section on the Configuration Console page to review the configured items and completed batch files by accessing **Configured items** and **Completed batches** tabs.

    You can download a batch file from **Completed batches** tab view. Under the **Configured items** tab, you can see the console items that were marked as configured after the current active batch update set was created.

12. Select **Go to active batch** file to review all the update that were captured in the currently active batch file.

    Select the Child Update Sets related list to view the child update sets under the parent update set.

    **Note:** You can review the child update sets to know the exact update made in the active batch file.

13. Select **Go to Update Set** on the Configuration Console page.

    **Note:** This option shows up only when the entire configuration of the application completes.

    You can then export the update set and move it to either test instance or production instance.


## What to do next

After the configuration completes, you can promote the changes to test or production instances by re-running the auto-installation, committing retrieved update sets, and validating ATF tests.

**Parent Topic:**[Configure in Now Assist for Setup](../concept/ia-config-landing.md)

