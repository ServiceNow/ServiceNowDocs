---
title: Metadata enrichment prerequisites
description: Before running AI enrichment jobs, confirm that the required applications are installed, email notifications are configured, and the correct roles are assigned.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/integrate-applications/ai-enrichment-prerequisites-dc.html
release: australia
topic_type: concept
last_updated: "2026-10-22"
reading_time_minutes: 1
keywords: [AI metadata enrichment, metadata enrichment, prerequisites, Data Catalog, data steward]
breadcrumb: [Metadata enrichment with ServiceNow Otto, Data Catalog, Workflow Data Fabric]
---

# Metadata enrichment prerequisites

Before running AI enrichment jobs, confirm that the required applications are installed, email notifications are configured, and the correct roles are assigned.

## Applications

The following application must be installed:

-   Otto for Workflow Data Fabric \(sn\_nowassist\_wdf\) starting with version 2.1.4 plugin
-   Data Catalog application \(sn\_dcg\_app\)

## Email notifications

Email notifications must be configured on the instance. Enrichment jobs send an email when they finish. For configuration details, see [Email properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/c_EmailProperties.md).

## Roles

The following roles must be assigned to users who run and review enrichment jobs:

-   df\_data\_steward
-   now\_assist\_panel\_user
-   wdf\_operator

To assign roles, see:

-   [Assign a role to a user](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/t_AssignARoleToAUser.md)
-   [Assign a role to a group](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/t_AssignRoleToGroup.md)

