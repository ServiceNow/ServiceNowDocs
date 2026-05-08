---
title: Download the manifest file
description: Configure the user roles and download the add-in manifest file to use the Export to PowerPoint add-in for Microsoft PowerPoint.
locale: en-US
release: australia
product: Export to PowerPoint for Application Portfolio Management
classification: export-to-powerpoint-for-application-portfolio-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Export to PowerPoint for Strategic Portfolio Management, Strategic Portfolio Management]
---

# Download the manifest file

Configure the user roles and download the add-in manifest file to use the Export to PowerPoint add-in for Microsoft PowerPoint.

## Before you begin

Role required: sn\_ppt\_export.ppt\_admin

## Procedure

1.  Navigate to **All** &gt; **ServiceNow Add-Ins for Office** &gt; **Office Add-In Manifests**.

2.  Click **Templates for ServiceNow**.

    **Note:** Check the **Templates for ServiceNow** description to match with **PowerPoint plugin for ServiceNow** to ensure that the correct manifest file is selected.

3.  Click **Download Manifest** to download the add-in file.

    The manifest file you download is specific to your instance. It contains the instance URL and configuration details that apply only to your environment. Using a manifest from one instance on another instance does not work and may cause errors.

    If you work with more than one ServiceNow instance, for example, a development instance and a production instance — you have two options:

    -   Install a separate manifest for each instance. Download and install the manifest individually from each instance you need to connect to.
    -   Use the sideload option. If installing multiple manifests is not practical, use the sideload option to temporarily load the manifest for a different instance without installing it permanently.

## What to do next

-   Share the `manifest.xml` file with Microsoft Office 365 account manager to upload the manifest file for Microsoft Office 365 users to enable the Export to PowerPoint add-in for Microsoft PowerPoint.

    Alternatively, you can sideload the add-in for testing purposes using one of the following processes.

    -   For Windows machines: [https://learn.microsoft.com/en-us/office/dev/add-ins/testing/create-a-network-shared-folder-catalog-for-task-pane-and-content-add-ins](https://learn.microsoft.com/en-us/office/dev/add-ins/testing/create-a-network-shared-folder-catalog-for-task-pane-and-content-add-ins)
    -   For macOS machines: [https://learn.microsoft.com/en-us/office/dev/add-ins/testing/sideload-an-office-add-in-on-mac](https://learn.microsoft.com/en-us/office/dev/add-ins/testing/sideload-an-office-add-in-on-mac)
-   For more information about the additional configuration steps required to enable the Export to PowerPoint add-in for browser version of Microsoft PowerPoint, see the [KB1171422](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1171422) article in the Now Support Knowledge Base.

**Parent Topic:**[Configuring Export to PowerPoint](../concept/configure-export-to-ppt.md)

