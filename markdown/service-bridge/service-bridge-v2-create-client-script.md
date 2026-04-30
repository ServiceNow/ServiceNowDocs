---
title: Create catalog client scripts
description: As a provider, create catalog client scripts in Service Exchange to control the behavior of the catalog items when presented to your consumers.
locale: en-US
release: yokohama
product: Service Bridge
classification: service-bridge
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Using scripts in a remote record producer, Use Service Exchange for providers, Service Exchange for Providers, Service Exchange]
---

# Create catalog client scripts

As a provider, create catalog client scripts in Service Exchange to control the behavior of the catalog items when presented to your consumers.

## Before you begin

You must be using Service Exchange version 2.1.x+.

Role required: admin

## About this task

You can apply catalog client scripts to a catalog item or a variable set. These scripts run on the browser instead of the server, enables you to control the information that the consumer submits better.

## Procedure

1.  Navigate to **All** &gt; **Service Exchange Provider** &gt; **Administration** &gt; **Remote Catalog Items**.

2.  Select the Remote record producer.

    You can select only record producers with a Compatibility field value of 2.1.x+.

3.  In the Remote record producer form, select the Catalog Client Scripts related list and then select **New**.

4.  On the form, fill in the fields.

    For a description of the field values, see [Catalog client script new record form](../reference/service-bridge-v2-cat-script-fd.dita.md).

5.  Select **Submit**.


