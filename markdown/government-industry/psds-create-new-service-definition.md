---
title: Configure a service definition for Playbooks in Public Sector Digital Services
description: Create a service definition for use with Playbooks in Public Sector Digital Services.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Service Request Playbook, Playbooks, Configure Agent Workspaces, Configuring Public Sector Digital Services, Public Sector Digital Services \(PSDS\)]
---

# Configure a service definition for Playbooks in Public Sector Digital Services

Create a service definition for use with Playbooks in Public Sector Digital Services.

## Before you begin

Role required: admin

## About this task

Service definitions are records used to store details about a service that is available to end customers. You can create service definitions for each public service offered by your government agency.

After upgrade to Public Sector Digital Services v8.0, Services Offered, an extension of Product Model, will no longer be used to model government services. Services Received, an extension of Sold Product, will no longer be used to model the government services that have been granted/delivered to constituents. The Service Definition table will be used to model all public services offered by governments. The following fields from the Service Offered table will be removed and replaced with Service Model fields:

-   Type
-   Status
-   Number
-   Period Start Date
-   Period End Date
-   Jurisdiction
-   Category
-   Subcategory
-   Payment source

**Important:** When upgrading to Vancouver, any data in the Services Offered and Services Received tables will need to be manually migrated into the Service Definition table. You can do so by creating a Service Definition for each entry in the Services Offered table. Services Offered and Services Received data will not be accessible within the application until this step is completed. This is an optional task for previous releases.

## Procedure

1.  Navigate to **All** &gt; **Customer Service** &gt; **Administration** &gt; **Service Definitions**.

2.  Select **New**.

3.  Enter the details for the Service Definition.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the service definition.|
    |ID|System-generated unique identifier for the service definition.|
    |Table|Table associated with the service definition. Select a case or task table based on the service.|
    |Customer service type|Select a service type for the service definition.|
    |Playbook record generator|Select a playbook record generator.|
    |Service Organizations offering Service|Service that the service organizations provide.|
    |Order|The order in which the case type appears in the interceptor.|
    |Active|Check box to activate or deactivate the service organization criteria.|
    |Description|Description of the service definition.|

4.  Select **Submit** or **Update**.

5.  Select the new Service Definition Record.

6.  In the Default Table Values field, select **Service Definition**.

7.  Select the search icon ![Search icon.](../../../help-center/vendor-management-workspace/image/magnifying-glass.png), and select the new Service definition in the choice menu.

8.  Select **Submit**.

    The service definition is now created and can be used with any of the playbooks in Public Sector Digital Services.


