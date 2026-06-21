---
title: Components installed with Enterprise-Wide Deployment
description: Several types of components are installed with installation of the Enterprise-Wide Deployment application, such as user roles, tables, and scheduled jobs.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/strategic-portfolio-management/components-installed-with-ewd.html
release: australia
product: Strategic Portfolio Management
classification: strategic-portfolio-management
topic_type: reference
last_updated: "2026-06-21"
reading_time_minutes: 1
breadcrumb: [Reference, SPM Enterprise-Wide Deployment, Strategic Portfolio Management]
---

# Components installed with Enterprise-Wide Deployment

Several types of components are installed with installation of the Enterprise-Wide Deployment application, such as user roles, tables, and scheduled jobs.

## Roles installed

The following roles are installed with Enterprise-Wide Deployment and govern partition creation, access, and visibility.

|Role title \[name\]|Description|
|-------------------|-----------|
|EWD Admin \[sn\_spm\_ewd.ewd\_admin\]|Can create and configure partitions. Users with this role can define partition criteria, associate a role with the partition, and manage all partition settings.|
|EWD PMO \[sn\_spm\_ewd.ewd\_pmo\]|Grants visibility across all partitions regardless of the assigned partition role. This role is intended for PMO users who require enterprise-wide visibility.|

## Tables installed

|Table \[ID\]|Description|
|------------|-----------|
|Partition \[sn\_spm\_ewd\_partition\]|Stores partition details that define a data separation boundary, with an assigned role association and criteria configuration.|
|Partitioned table \[sn\_spm\_ewd\_partitioned\_table\]|Stores partitioned table details that define the scope of data separation, with a criteria field configuration that controls record visibility for each supported table.|

## Scheduled jobs installed

The following scheduled jobs are installed with Enterprise-Wide Deployment.

|Job name|Description|
|--------|-----------|
|Update existing records with partition details|Populates partition values on existing records — projects, demands, programs, and portfolios — that were created before partition configuration was completed. Run this job after defining partitions to associate historical records with the correct partition.|

**Parent Topic:**[SPM Enterprise-Wide Deployment reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/strategic-portfolio-management/ewd-reference.md)

