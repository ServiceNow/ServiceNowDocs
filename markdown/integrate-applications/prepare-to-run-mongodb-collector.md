---
title: Prepare to run the MongoDB collector
description: Create a MongoDB user and configure authentication before running the collector.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [MongoDB metadata collector, Configuring metadata collectors, Data Catalog, Workflow Data Fabric]
---

# Prepare to run the MongoDB collector

Create a MongoDB user and configure authentication before running the collector.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **MongoDB Project properties** &gt; **Database Access**.

2.  Select **Add new database user**.

3.  Select an authentication method:

    -   User-password \(SCRAM\) authentication
    -   X.509 authentication
    -   AWS authentication
4.  Configure user permissions.

    -   For built-in roles: Assign the Read any database role.
    -   For specific privileges: Assign Read permission for every database that you want to collect.

**Parent Topic:**[MongoDB metadata collector](../concept/mongodb-metadata-collector.md)

