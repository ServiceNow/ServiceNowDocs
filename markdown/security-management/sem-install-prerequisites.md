---
title: Migration upgrade prerequisites
description: Before you install the required applications for Security Exposure Management Workspace, review the following information and setup tasks.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-08-14"
reading_time_minutes: 1
breadcrumb: [Installing Security Exposure Management Workspace applications, Implement, Unified Security Exposure Management, Security Operations]
---

# Migration upgrade prerequisites

Before you install the required applications for Security Exposure Management Workspace, review the following information and setup tasks.

## Unified Security Exposure Management overview

Unified Security Exposure Management \(USEM\) introduces a unified foundation across all Vulnerability Response and Security Exposure Management applications. The new architecture consolidates data models, streamlines feature sets, and enhances performance and scalability. However, migrating to USEM is a significant upgrade that requires careful planning, validation, and change management.

Security Exposure Management supports the following applications:

-   Vulnerability Response \(infrastructure\)
-   Application Vulnerability Response
-   Container Vulnerability Response
-   Configuration Compliance

## Prerequisites and notes for upgrade

-   You cannot use Operational Technology Vulnerability Response \(OT VR\) in the same instance with Unified Security Exposure Management.
-   You are aware of the significant data model changes and user experience updates outlined in this document.
-   Perform the upgrade in a non-critical, non-production instance first and validate the migrated data and any customizations.
-   Rollback is not possible once an instance is upgraded to USEM.
-   You must deactivate all third-party integrations and ensure that no integration runs are underway before upgrade.

    To deactivate scheduled jobs and scheduled jobs within integration-specific scopes:

    1.  Navigate to the Third Party Integration \[sn\_sec\_int\_integration\] table.
    2.  Open an integration record.
    3.  Locate the integration instances related list and open a record.
    4.  Clear the Active flag and save \(Update\) the record.
-   You must deactivate the scheduled jobs and scheduled jobs within integration-specific scopes for the Vulnerability Response, Application Vulnerability Response, Container Vulnerability Response, and Configuration Compliance applications. For a list of scheduled jobs you must deactivate, see [Migration upgrade reference information](../reference/sem-migration-prereq-reference-data.md).

    To deactivate scheduled jobs:

    1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs**.
    2.  Open a record.
    3.  Clear the Active flag and save \(Update\) the record.

After you have completed the deactivation of scheduled jobs and third-party integrations, upgrade plugins in sequential order to migrate to USEM. See [Download and activate applications](../task/sem-install-required-applications.md) for more information.

1.  Vulnerability Response \(This will upgrade all the dependent plugins shown in the flow chart\)
2.  Configuration Compliance
3.  Container Vulnerability Response
4.  Upgrade each of the third-party integrations you are using, one at a time.

