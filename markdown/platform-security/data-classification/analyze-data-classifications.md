---
title: Analyzing data classifications using the Overview dashboard
description: The Overview dashboard reports the current state of data classifications within your instance and how your users are distributed by location.
locale: en-US
release: australia
product: Data Classification
classification: data-classification
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Data Classification, Platform Privacy]
---

# Analyzing data classifications using the Overview dashboard

The Overview dashboard reports the current state of data classifications within your instance and how your users are distributed by location.

If you have a data classification administrator or auditor role, you can visualize the current sensitivity of instance data, which helps increase security and compliance with privacy laws. By using the Location field in user records, administrators map users across different regions that have differing privacy regulations.

## Tables and columns tab

![Overview dashboard - Tables and Columns tab](../image/data-classification-overview-tables-columns.png)

## Users tab

![Overview dashboard - Users tab](../image/data-classification-overview-users.png)

## Required ServiceNow AI Platform roles

-   data\_classification\_admin: Administers all aspects of the Data Classification application, including data classification setup, and assignment.
-   data\_classification\_auditor: Audits Data Classification code assignments.

## Use cases

For additional examples of how different people in your organization would use this dashboard, see Use Cases in [Data Classification](../concept/data-classification.md).

|User|Dashboard use|
|----|-------------|
|data\_classification\_admin|Confirm that you have assigned data classifications to the correct fields in your instance.|
|data\_classification\_auditor|Audit the senility and security of data in your instance.|

## Reports

|Title|Type|Source table|Description|
|-----|----|------------|-----------|
|Breakdown of classified data|Donut chart|m2m\_dictionary\_dataclass|Provides a breakdown of instance data classifications, by data class, total displayed in center.|
|Total tables|Single Score|sys\_dictionary|Total number of data tables in the entire dictionary.|
|Total columns|Single Score|sys\_dictionary|Total number of classified data columns in the entire dictionary.|
|User reference columns|Single Score|sys\_dictionary|Total number of user reference columns in the dictionary.|
|User location count|Single Score|sys\_user|Total number of distinct locations found for users|
|User count|Single Score|sys\_user|Total number of user records in your instance.|
|Users by country|Map|sys\_user|Breakdown of user records by country.|

