---
title: Configure service definitions
description: Configure service definitions for the services in Financial Services Operations applications. You can review and modify the predefined service definitions that the application installs or add new ones.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/financial-services-operations/financial-services/configure-service-definitions.html
release: australia
product: Financial Services
classification: financial-services
topic_type: task
last_updated: "2026-05-12"
reading_time_minutes: 2
breadcrumb: [Configure, Financial Services Operations \(FSO\)]
---

# Configure service definitions

Configure service definitions for the services in Financial Services Operations applications. You can review and modify the predefined service definitions that the application installs or add new ones.

## Before you begin

Ensure that the scope is selected for the application that you're configuring a service definition for. For more information, see Application picker.

Roles required: When you enable application administration for a scoped application, the system automatically applies that application's ACL rules \(which control user access and permissions\). For example, in Financial Services Payment Operations, the sn\_bom\_payment.admin and admin roles are needed and applied automatically.

## About this task

Service definitions are configured for both cases and tasks for each service in the application and enable a unique flow and view for each service. You can add new case types and configure service definitions for each type.

## Procedure

1.  In the application navigation filter, navigate to **\[_&lt;Application name&gt;_\]** &gt; **Administration** &gt; **Service Definitions** list, where *&lt;Application name&gt;* is the name of the application that you are configuring.

    For example for Financial Services Payment Operations application, the navigation sequence is **Payment Operations** &gt; **Administration** &gt; **Service Definitions**.

2.  Create a service definition or modify an existing one.

    -   To create a service definition, click **New**.
    -   To modify a predefined one, select the service definition that you want to modify, from the application. Use the link on the top of the modal to edit the record.
3.  Fill the fields in the Service Definition form to create or modify a service definition.

    The details you enter in this form are used to configure a service definition and store the details about a service that you provide to customers.

    For more information about the form fields, see .

4.  Click **Submit** \(for new service definitions\) or **Update**\(for modified service definitions\).

5.  Define who can view this service definition by navigating to the appropriate visibility configuration.

    Choose the configuration based on the user type you want to control:

    -   For **Agent visibility**: Navigate to **All** &gt; **sn\_csm\_case\_types\_service\_user\_criteria.list**
    -   For **Customer visibility**: Navigate to **All** &gt; **sn\_csm\_case\_types\_service\_customer\_criteria.list**
6.  Configure the visibility properties for the service definition by setting the appropriate user criteria values.

    Use the following values to control visibility for both agents and customers:

    -   To **hide the service definition**: Set the value to `No User`.
    -   To **show the service definition**: Set the value to `User with sn_bom_service_definition_read`.

