---
title: Service Creator roles
description: The Service Creator application uses the specific roles.
locale: en-US
release: zurich
product: Service Creator
classification: service-creator
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Activate Service Creator, Service Creator, Building pro-code applications, Developing your application, Building applications]
---

# Service Creator roles

The Service Creator application uses the specific roles.

To learn more about managing per-user subscriptions, see [Managing per-user subscriptions in Subscription Management](https://www.servicenow.com/docs/access?context=managing-user-subscriptions-v2&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US) and contact your account representative.

|Role Title \[Name\]|Description|
|-------------------|-----------|
|`[service_category_user]` `[service_category_table_name_user]`|Accesses request records for a service category. The table name for the service category determines the name of the role. Users designated as the manager, editors, or service fulfillers for a service category automatically receive this role.|
|Catalog Administrator `[catalog_admin]`|Creates, edits, and publishes service categories and services, and creates and edits notifications including template notifications. Catalog administrators are primarily responsible for approving service category requests.|
|Catalog Manager `[catalog_manager]`|Creates, edits, and publishes services, and designates editors and service fulfillers. A user designated as the manager of a service category receives this role automatically.|
|Catalog Editor `[catalog_editor]`|Creates and edits services. A user designated as an editor of a service category receives this role automatically.|

