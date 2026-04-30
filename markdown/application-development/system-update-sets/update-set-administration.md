---
title: Update set administration
description: Manage how update sets store, retrieve, preview, and apply configuration changes between instances.
locale: en-US
release: yokohama
product: System Update Sets
classification: system-update-sets
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [System update sets, Deploying applications, Building applications]
---

# Update set administration

Manage how update sets store, retrieve, preview, and apply configuration changes between instances.

Administrators have the following options with update sets.

-   Create an update set to store local changes.
-   Select the current update set to store local changes.
-   Commit an update set to prepare it for distribution.
-   Report on the contents of update sets.
-   Compare update sets to determine what differences they contains.
-   Merge separate update sets into a single update set.
-   Create an external file from an update set.
-   Retrieve update sets from remote instances.
-   Apply retrieved update sets.
-   Back out changes applied from an update set.
-   Set system properties related to update sets

## Grant access to the update set picker

The update set picker allows users to choose an update set for making and tracking customizations. By default, only administrators can use the update set picker. You can [grant access to additional users](../task/t_GrantAccessToTheUpdateSetPicker.md).

## Automatically preview retrieved update sets

By default, the system automatically previews update sets as soon as it has retrieved them. To turn off this behavior, set the system property **glide.update\_set.auto\_preview** to **false**: in the navigator filter, type **sys\_properties.list** then navigate to the **glide.update\_set.auto\_preview** property and edit the **value** field.

## Track an application table

Application developers can track application changes in an update set to save or distribute a particular version of an application. During table creation, set **Extends Table** to Application File \[sys\_metadata\].

