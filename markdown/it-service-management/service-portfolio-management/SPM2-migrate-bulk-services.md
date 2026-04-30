---
title: Convert services in bulk in Service Portfolio Management
description: Convert multiple services from the Configuration Management Database \(CMDB\) service table to one of the dedicated child tables. You can convert to a business service or to a technical service.
locale: en-US
release: xanadu
product: Service Portfolio Management
classification: service-portfolio-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Using Service Portfolio Management, Service Portfolio Management, IT Service Management]
---

# Convert services in bulk in Service Portfolio Management

Convert multiple services from the Configuration Management Database \(CMDB\) service table to one of the dedicated child tables. You can convert to a business service or to a technical service.

## Before you begin

Role required: admin

## About this task

You can convert services individually but to reduce manual overhead, convert multiple services at once from the CMDB service table \[cmdb\_ci\_service\] to one of the dedicated child tables:

-   Business service table \[cmdb\_ci\_service\_business\]
-   Technical service table \[cmdb\_ci\_service\_technical\]

When you convert a service, the record and all its relationships remain intact.

**Note:** Service offerings can’t be converted but they inherit the parent type \(Service classification if your organization uses that field\).

## Procedure

1.  Navigate to **All** &gt; **Service Portfolio Management** &gt; **Services**.

2.  Select the services that you want to convert.

    If your organization uses the Service classification field for business and technical services, then you can filter by Service classification.

3.  Select **Actions on selected rows**, and then select **Convert to business service** or **Convert to technical service**.

4.  At the prompt, select **OK** to continue to convert the services or select **Cancel**.

    **Note:** If a selected item can’t be converted, a warning message is displayed.

5.  Convert a service while in the service record.

    To convert a service wile in the service record, find the convert options under **Related Links**. If you don't see the convert options, then you might be in a record that isn't in the CMDB service table \[cmdb\_ci\_service\].


**Parent Topic:**[Using Service Portfolio Management](../concept/SPM2-using.md)

