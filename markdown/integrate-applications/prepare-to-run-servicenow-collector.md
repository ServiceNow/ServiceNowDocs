---
title: Prepare to run the ServiceNow collector
description: Create a ServiceNow user and configure permissions before running the collector.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [ServiceNow metadata collector, Configuring metadata collectors, Data Catalog, Workflow Data Fabric]
---

# Prepare to run the ServiceNow collector

Create a ServiceNow user and configure permissions before running the collector.

## Before you begin

Role required: admin

## About this task

The collector uses Basic Authentication with username and password. ServiceNow determines authorization based on roles.

## Procedure

1.  Log in to the ServiceNow instance.

2.  Navigate to **All** &gt; **System Security** &gt; **Users and Groups** &gt; **User**.

3.  Create a new user.

    1.  Select **New**.

    2.  Complete the required fields.

    3.  Select **Save**.

4.  Set a password for the user.

5.  Assign roles to the user.

    Assign these roles:

    -   rest\_api\_explorer
    -   admin
    These roles provide read access to the following tables:

    **Standard metadata tables:**

    -   sys\_app \(System Applications\)
    -   sys\_scope \(Application Scopes\)
    -   sys\_db\_object \(Tables\)
    -   sys\_dictionary \(Fields\)
    -   sys\_db\_view \(Views\)
    -   sys\_db\_view\_table \(View Table Mappings\)
    -   sys\_user \(Users - for connection testing\)
    **Data Fabric tables:**

    -   sn\_df\_connector \(Data Fabric Connectors\)
    -   sys\_df\_connection\_metadata \(Connection Metadata\)
    -   sys\_df\_data\_dictionary \(Data Dictionary\)
    -   sys\_df\_connection\_data \(Connection Data\)
    -   sn\_df\_connection\_attributes \(Connection Attributes\)
    -   sys\_variable\_value \(Variable Values\)

**Parent Topic:**[ServiceNow metadata collector](../concept/servicenow-metadata-collector.md)

