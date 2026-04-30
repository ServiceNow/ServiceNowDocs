---
title: Install the Service Portfolio Management Sample Content Pack
description: Install the Service Portfolio Management Taxonomy Content Pack plugin \(com.snc.spm.content\) to access a sample portfolio structure and service taxonomy. This sample data accelerates your ability to create and manage a service portfolio.
locale: en-US
release: zurich
product: Service Portfolio Management
classification: service-portfolio-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configure, Service Portfolio Management, IT Service Management]
---

# Install the Service Portfolio Management Sample Content Pack

Install the Service Portfolio Management Taxonomy Content Pack plugin \(com.snc.spm.content\) to access a sample portfolio structure and service taxonomy. This sample data accelerates your ability to create and manage a service portfolio.

## Before you begin

Role required: admin or portfolio\_admin

Dependency: Service Portfolio Management Foundation application

## About this task

Installing the Service Portfolio Management Taxonomy Content Pack \(com.snc.spm.content\) plugin, enables you to:

-   Access demo data and a sample taxonomy structure metadata.
-   Create portfolios and associated taxonomies.
-   Access sample lists of service data.
-   Link to periphery example data, such as vendors and contracts.

You can view the sample content in the **Service Portfolios** module of the Service Portfolio Management application as **Sample IT Services Portfolio**. Alternatively, you can view data in the DPM Workspace. For more information, see [Digital Portfolio Management](../../digital-portfolio-management/reference/dpm-landing.md).

**Important:** For Step 2 in the procedure, enter `com.snc.spm.content` in the Search field, and check the box to **Load demo data**.

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the plugin using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated Admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/zurich-platform-administration/page/administer/plugins/task/find-components.html).


-   **[Installed with Service Portfolio Management Premium](../../service-owner-workspace/reference/installed-with-SOW.md)**  
Service Portfolio Management Premium installs the following components.
-   **[View Service Portfolio Management sample IT services portfolio content](use-SPM2-sample-service-portfolio.md)**  
Access, view, and analyze the Service Portfolio Management sample IT services portfolio content to plan and create your service portfolio. Consider the sample structure as a starting point. You can add to it or modify it to suit the specific needs of your organization.

**Parent Topic:**[Configuring Service Portfolio Management](../concept/SPM2-configuring.md)

