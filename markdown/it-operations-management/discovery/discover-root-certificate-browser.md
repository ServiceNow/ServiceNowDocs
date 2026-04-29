---
title: Discover root certificates hosted outside your server
description: Collect information about root certificates stored outside your server. Create a specialized Discovery schedule.
locale: en-US
release: australia
product: Discovery
classification: discovery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Visibility to TLS certificates, Configuring Certificate Inventory and Management, Certificate Inventory and Management, ITOM Visibility, IT Operations Management]
---

# Discover root certificates hosted outside your server

Collect information about root certificates stored outside your server. Create a specialized Discovery schedule.

## Before you begin

Role required: Admin, discovery\_admin, Certificate administrator

## About this task

To discover root certificates stored outside your server, create a special Discovery schedule to target them.

## Procedure

1.  Navigate to **All** &gt; **Discovery** &gt; **Discovery Schedules**.

2.  From the Discovery Schedule page, select **New**.

3.  On the Discovery Schedule form, fill in the fields.

    For a description of the field values, see [Discovery schedule form table](../reference/discovery-schedule-form-table.md).

4.  Save this record by selecting **Update**.

5.  Select the **Serverless Execution Patterns** tab.

6.  Create a Serverless Execution Pattern.

    1.  Select **New**.

    2.  In the New Record page, select the search icon \(![Search icon](../../health-log-analytics-operator/image/icon-search-sow.png)\) in the **Pattern** field.

    3.  Fill in the **Name** field.

    4.  Find and select **Import SSL Certificate**.

    5.  Select **Submit**.

        You're redirected back to the Discovery Schedule page created in step 4.

7.  Select the **Serverless Execution Patterns** tab.

8.  Select the **Name** of the new pattern that you just made.

9.  Select the **\(empty\)** value field, and add a value for each parameter.

    For guidance on what values to set, see [Run Certificate Discovery via certificate file import](run-cert-inventory-mgmt-import.md).

10. Collect information on your root certificate by making a unique certificate file.

    1.  Navigate to the **Discovery Schedule** record that you created.

    2.  Select the link **Discover now** to begin Discovery that collects your root certificate.

11. Navigate to **All** &gt; **Unique Certificates**.

12. After the Discovery is complete, find your root certificate to confirm that it's there.


## Result

Your Discovery collects information on your root certificate located outside a server.

## What to do next

[Connect an intermediate certificate to its root certificate](connect-intermediate-certificate-to-root.md) to complete your certificate chain.

