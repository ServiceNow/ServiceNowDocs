---
title: How encrypted data is handled
description: By default, encrypted values appear in all views as \*\*\*\*\*\*\*. Only users with the CDM Secrets \[sn\_cdm.cdm\_secrets\] role can view, create, update, and delete encrypted values in config data. The system validates and exports encrypted data appropriately.
locale: en-US
release: australia
product: DevOps \(Family\)
classification: devops-family
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [DevOps Config reference, DevOps Config, IT Service Management]
---

# How encrypted data is handled

By default, encrypted values appear in all views as `*******`. Only users with the CDM Secrets \[sn\_cdm.cdm\_secrets\] role can view, create, update, and delete encrypted values in config data. The system validates and exports encrypted data appropriately.

**Important:** DevOps Config is now deprecated and no longer supported or available for new activation.

## Permissions of users with the CDM Secrets \[sn\_cdm.cdm\_secrets\] role

-   Encrypted values appear in all views as `*******` by default.
-   Select the **View encrypted data** menu option to display encrypted values in any view.
-   Validate and export a snapshot that includes encrypted data. All exported data is readable by the CI/CD pipeline apps.
-   Create, update, delete abilities:
    -   View an encrypted value.
    -   Edit an encrypted value.
    -   While creating a CDI, specify that the value should be encrypted.
    -   Permanently encrypt a value that is currently not encrypted.
    -   Permanently decrypt a value that is currently encrypted.
    -   Delete a CDI that has an encrypted value.

## Permissions of all other users

-   Encrypted values always appear in all views as `*******`.
-   Request manual validation of snapshots that include encrypted data.
-   Delete encrypted values in config data.
-   Cannot view, create, or update encrypted values in config data.
-   Cannot export a snapshot that includes encrypted data.

**Parent Topic:**[DevOps Config reference](../../devops-config/reference/devops-config-reference.md)

