---
title: Use Business Application Lifecycle Management to request or retire an application - Legacy
description: If you are an Enterprise Architecture user, you should use the Business Application Lifecycle Management services to request or register a new business application for your business. You can request a business application like you place an order for any other service catalog item.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Use - Legacy, Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Use Business Application Lifecycle Management to request or retire an application - Legacy

If you are an Enterprise Architecture user, you should use the Business Application Lifecycle Management services to request or register a new business application for your business. You can request a business application like you place an order for any other service catalog item.

## Before you begin

Role required: sn\_apm.apm\_user

## About this task

The base system also offers **Register a Business Application** as a service to all ServiceNow AI Platform customers. The Enterprise Architecture Core plugin \(com.snc.apm\_core\) provides this service and the plugin is available on new and restarted instances. Customers who do not have the Enterprise Architecture application can avail this service to request a new business application. However, activating the Enterprise Architecture plugin \(com.snc.apm\) enhances this service to predict and set application category using the machine-learning solution.

For more information on the plugin, see [Activate Application Portfolio Management](activate-apm.md#apm-oob-plugin). See [Predictive Intelligence for Application Portfolio Management](../concept/predictive-intelligence-apm.md) to know more about machine-learning solution for business applications.

## Procedure

1.  Navigate to **All** &gt; **Enterprise Architecture** &gt; **Business Application Lifecycle Management** &gt; **Business Application Catalog**.

    Business Application Lifecycle Management Services opens in a service catalog page.

2.  Click the **Register a Business Application** card or click **View Details** in the Register a Business Application card to register a new business application.

3.  Enter the details in the Register a Business Application form.

    Name of the business application is mandatory. Mandatory fields have a red asterisk \(\*\) beside them.

4.  Click **Submit**.

    The system validates your request to check if a business application with the same name exists. If yes, then an error message is displayed. If no, then a flow is triggered and a request to register a business application is created.

    The approval request is sent to the Business Application Registration Approval Group. After a member of the group approves your request, the business application gets created as a record in the business application table. You will receive an email notification for the same.

5.  To retire a business application that you no longer require, click the **Retire a Business Application** card or click **View Details** in the Retire a Business Application card.

    1.  Select the name of the application from the list of values in the Retire a Business Application form.

        Conditions to retire a business application:

        -   Only if you are an IT owner of the application, business owner, or a user who supports the application, you can request to retire an application.
        -   You require sn\_apm.apm\_user or sn\_apm.apm\_analyst role to retire a business application.
        -   As an Enterprise Architecture user, you cannot delete a business application record or mark the application as **Inactive**. However, you can raise a new request to decommission an application.
        -   The business application that you choose to retire must not be in **Retired** status nor the application record **False** \(inactive\) in the **Active** field.
    2.  Click **Submit**.


**Parent Topic:**[Using Enterprise Architecture \(formerly Application Portfolio Management\) - Legacy](../concept/using-apm.md)

