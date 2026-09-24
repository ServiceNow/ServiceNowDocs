---
title: Activate migration of attachments to columnar storage
description: You can activate the Data Management Columnar Attachments Migration plugin \(com.glide.data\_management.columnar\_attachments\) for Data Management if you have the admin role. If the application does NOT include demo data or it does NOT install related applications and plugins, delete or revise the following sentence:
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/activate-columnar-attachments-migration.html
release: brazil
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Configure, Data Management, Tables and data, Configure core features, Administer the ServiceNow AI Platform]
---

# Activate migration of attachments to columnar storage

You can activate the Data Management Columnar Attachments Migration plugin \(com.glide.data\_management.columnar\_attachments\) for Data Management if you have the admin role.

## Before you begin

To successfully activate the Data Management Columnar Attachments Migration plugin \(com.glide.data\_management.columnar\_attachments\), you must also activate the Data Archiving – Columnar Storage plugin \(com.glide.db.columnar.archive\). See [Activate columnar storage](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/activate-columnar-storage.md).

Columnar storage for attachments requires RaptorDB Professional V2. RaptorDB Professional is a licensed database; for more information, contact your account team.

To purchase a subscription, contact your ServiceNow account manager. When you purchase a subscription, certain plugins are activated automatically. If a paid plugin isn't activated automatically, you can manually activate it from the All Applications list in your instance.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Data Management Columnar Attachments Migration plugin \(com.glide.data\_management.columnar\_attachments\) using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/find-components.md).


**Parent Topic:**[Configuring Data Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/configuring-data-management.md)

