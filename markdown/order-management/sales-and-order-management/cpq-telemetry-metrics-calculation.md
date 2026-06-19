---
title: CPQ usage calculation
description: CPQ usage metrics track how users interact with CPQ Configurator and Sales Customer Relationship Management \(Sales CRM\) features. These metrics support accurate usage measurement.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/sales-and-order-management/cpq-telemetry-metrics-calculation.html
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2026-06-02"
reading_time_minutes: 3
breadcrumb: [CPQ app, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# CPQ usage calculation

CPQ usage metrics track how users interact with CPQ Configurator and Sales Customer Relationship Management \(Sales CRM\) features. These metrics support accurate usage measurement.

## Usage metrics

Two usage metrics are collected for CPQ: user count and configuration count. These metrics are visible in the Usage Analytics area of your CPQ instance and are used to measure product usage across CPQ Microservices and Sales CRM.

Metric data is collected daily and displayed in the Usage Intelligence dashboard. When viewing metrics, select **Last full day** or **Last 7 days** to confirm data is available, as a default filter of the current day may return no results if the daily collection has not yet run.

## Prerequsites and Requirements

For CPQ telemetry metrics to function correctly, the following conditions must be present:

-   A CPQ microservices connection must be configured and available on the instance.
-   The application scope must be set to **CPQ Integration** when accessing or validating the CPQ Users table.
-   Users must hold the required CPQ Sales CRM product roles to be included in the user count.

For the full list of conditions required for metrics to populate, refer to the associated knowledge base articles.

## User count

The user count metric reflects the number of active users who have access to CPQ or Sales CRM features on your instance. This count combines users from two sources:

-   CPQ users fetched from CPQ microservices connected to your instance.
-   Sales CRM users from the Sales CRM `sys_user` table who hold relevant CPQ or Sales CRM product roles.

The combined count appears in the CPQ Users table, which provides a single view of all users with access to CPQ and Sales CRM functionality.

## Which users are counted

Not all users in the `sys_user` table are included. The user count tracks active Fulfillers as licensed seats. Business stakeholders are counted conditionally, based on their activity. Requesters aren't included in the user count.

The user count and configuration count metrics are complementary: Fulfillers are measured as seats in the user count, while non-Fulfiller users such as business stakeholders are reflected through configuration records in the configuration count.

**Note:** Inactive users are excluded from the count.

CPQ Users table: The CPQ Users table is a remote table that queries both CPQ microservices and the Sales CRM instance to populate user data. The table includes the following fields:

-   **CPQ user**: the username from CPQ microservices.
-   **User**: the corresponding record in the Sales CRM `sys_user` table, populated when a matching user is found.
-   **Role type**: the subscription role associated with the user.

The table may be empty if the required CPQ microservices connection is not configured or available on the instance. Several conditions must be met for the metric to populate correctly; refer to the associated knowledge base article for the complete list of requirements.

## Configuration count

Each initialization of configuration is counted whether it's just initiated, abandoned or completed.

The act of initiating a configuration is sufficient to increment the count, regardless of whether the deployment completes successfully. After a Blueprint is deployed, it is set to available for use in customer-facing sales scenarios.

## Data freshness and caching

The CPQ Users table uses a built-in cache to avoid repeated queries to CPQ microservices on every request. The cache has a time-to-live \(TTL\) of 24 hours. As a result, data in the table may not reflect the most recent changes immediately after a deployment or user update. After the cache expires, the next request reruns the query and refreshes the table data.

This cache behavior is part of the remote table configuration and is not controlled by a system property.

