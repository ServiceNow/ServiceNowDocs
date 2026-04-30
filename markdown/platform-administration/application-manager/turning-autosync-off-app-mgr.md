---
title: Deactivating automatic synchronization with the ServiceNow Store
description: By default, the Application Manager in hosted ServiceNow AI Platform instances syncs automatically with available applications and updates from the ServiceNow Store. Automatic synchronization can be deactivated so you can receive updates only when you choose to.
locale: en-US
release: zurich
product: Application Manager
classification: application-manager
topic_type: concept
last_updated: "2025-10-07"
reading_time_minutes: 1
breadcrumb: [Configure, Application Manager, Administering applications, Get started, Administer]
---

# Deactivating automatic synchronization with the ServiceNow Store

By default, the Application Manager in hosted ServiceNow AI Platform instances syncs automatically with available applications and updates from the ServiceNow Store. Automatic synchronization can be deactivated so you can receive updates only when you choose to.

Automatic syncing with the ServiceNow Store can be deactivated by taking the instance offline. If you take the instance offline, you can use the **Sync now** button in the Application Manager to sync the Available for you page with the ServiceNow Store.

To take the instance offline, contact [Customer Service and Support](https://support.servicenow.com/now) and request that the `sn_appclient.app.install.offline` system property be set to `true`.

**Parent Topic:**[Configuring Application Manager](configuring-app-manager.md)

