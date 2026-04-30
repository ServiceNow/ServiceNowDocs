---
title: Creator Studio apps and tables
description: Creator Studio uses catalog templates to streamline the app creation process. Apps use the Task table, generating a new row for each submitted request.
locale: en-US
release: xanadu
product: Creator Studio
classification: creator-studio
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Exploring Creator Studio, Creator Studio, Building no-code applications, Developing your application, Building applications]
---

# Creator Studio apps and tables

Creator Studio uses catalog templates to streamline the app creation process. Apps use the Task table, generating a new row for each submitted request.

**Summary:** After reading this section, you'll understand:

-   The parts that go into building an app
-   Where requests from the apps go
-   How tables are used to store requests

## Parts of building an app

Apps contain one or all of the following parts.

|Functionality|Description|
|-------------|-----------|
|Form|When filled out, forms create a record with an associated task or workflow on the ServiceNow AI Platform.|
|Automation|Automation contains playbooks, or automated processes with limited actions that enable users to update records and complete tasks across multiple activities.|
|Form submissions|Workspace configuration that shows requests for the app built in Creator Studio, with standard and customizable filtered lists. Selecting a record in the **Form submissions** tab displays the record, which you can interact with in Creator Studio, enabling you to see how it will look.|

Your admin can create catalog templates to guide the process of building forms. For more information, see [Working with forms in Creator Studio](creator-studio-work-with-forms.md).

## Where requests from the apps go

Every app in Creator Studio automatically creates a task table where all opened records go when people use the app. The tables that Creator Studio apps generate extend the Request Task table that comes with Creator Studio, which extends the Task table.

[Extending](creator-studio-glossary.md#) a table means the new table inherits the parent \(extended\) table's columns, as well as its business logic. For more information on Task tables, see [Working with the Task table](https://www.servicenow.com/docs/access?context=c_TaskTable&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

For sys admin eyes only: Every app built in Creator Studio adds a record in the Request App Config table. The name of the table follows the format of scope\_request, for example, x\_snc\_02\_03\_request.

**Key term:**

-   **Record**

    A record is what the ServiceNow AI Platform generates for each request submitted through your app. Each record corresponds to a row in the app's Request Task table.


