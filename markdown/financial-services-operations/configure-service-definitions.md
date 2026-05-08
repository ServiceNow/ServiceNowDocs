---
title: Configure service definitions
description: Configure service definitions for the services in Financial Services Operations applications. You can review and modify the predefined service definitions installed with the application or add new ones.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Financial Services Operations \(FSO\)]
---

# Configure service definitions

Configure service definitions for the services in Financial Services Operations applications. You can review and modify the predefined service definitions installed with the application or add new ones.

## Before you begin

Ensure that the scope is selected for the application that you are configuring a service definition for. For more information, see Application picker.

Roles required: When enabling application administration for a scoped application, the ACL rules for that application will be applied by default. For example, in Financial Services Payment Operations, the sn\_bom\_payment.admin and admin roles are needed.

## About this task

Service definitions are configured for both cases and tasks for each service in the application and enable a unique flow and view for each service. You can add new case types and configure service definitions for each type.

## Procedure

1.  In the application navigation filter, navigate to **\[_&lt;Application name&gt;_\]** &gt; **Administration** &gt; **Service Definitions** list, where *&lt;Application name&gt;* is the name of the application that you are configuring.

    For example for Financial Services Payment Operations application, the navigation sequence is **Payment Operations** &gt; **Administration** &gt; **Service Definitions**.

2.  Create a service definition or modify an existing one.

    -   To create a service definition, click **New**.
    -   To configure a predefined one, open the service definition that you want to modify.
3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Show in interceptor|Setting the field to true makes the service definition visible in the case type selector. Otherwise, it will be hidden.|
    |Sys ID|System-generated unique identifier for the service definition.|
    |Task type|Table associated with the service definition. Select a case or task table based on the service.|

    When you create a service definition, the Service Definition form displays information about the service definition configuration. This record stores the details of the service provided to customers. For more information about the other fields, see Service Definition form.

4.  Click **Submit** or **Update**.


