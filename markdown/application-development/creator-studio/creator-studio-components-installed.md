---
title: Components installed with Creator Studio
description: When you activate the Creator Studio plugin, various components like tables and user roles are automatically installed.
locale: en-US
release: yokohama
product: Creator Studio
classification: creator-studio
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Installing Creator Studio from the ServiceNow Store, Configuring Creator Studio, Creator Studio, Building no-code applications, Developing your application, Building applications]
---

# Components installed with Creator Studio

When you activate the Creator Studio plugin, various components like tables and user roles are automatically installed.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see [Find components installed with an application](https://www.servicenow.com/docs/access?context=find-components&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

## What plugins are required to activate Creator Studio?

You must install the following plugins for Creator Studio:

-   Creator Studio \[sn\_creatorstudio\]
-   Creator Studio - Global \[com.glide.creator\_studio.global\]

## Properties installed with Creator Studio

-   **com.glide.creator\_studio.template\_deny\_list**

    Hides App Engine Studio template from appearing for users when they create an app.

    -   Type: string
    -   Default value: 211f71ca73202010ae42d31ee2f6a785
    -   Hide additional templates by adding their system values \(sys\_id for the template\), separated by commas, in the **Value** field. For more information on the sys\_id, see [Unique record identifier \(sys\_id\)](https://www.servicenow.com/docs/access?context=c_UniqueRecordIdentifier&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).
    For more information, see [Show the AES template](../task/creator-studio-unhide-template.md).

-   **sn\_creatorstudio.history\_record\_limit**

    Limits the last accessed history, for example in recent apps and sorting on the Creator Studio home page.

    -   Type: integer
    -   Default value: 1000
    -   Set this value to -1 to disable the limit
    -   Reduce this value from the default if the home page isn't loading fast enough

## Roles installed with Creator Studio

The following table lists all roles installed with Creator Studio. For details on how the roles work with Creator Studio, see [Creator Studio roles and personas](roles-creator-studio.md).

<table id="table_oyr_sy3_v1c"><thead><tr><th>

Role

</th><th>

Description

</th><th>

Contains role

</th></tr></thead><tbody><tr><td>

sn\_creatorstudio.user

</td><td>

-   Provides access to Creator Studio
-   Users can create new apps

</td><td>

-   catalog\_builder\_editor
-   sn\_collab\_request.basic\_write
-   sn\_udc.basic\_read
-   sn\_creatorstudio.basic\_read
-   sn\_collab\_request.basic\_read
-   app\_template\_runner
-   sn\_g\_app\_creator.app\_creator

</td></tr><tr><td>

sn\_creatorstudio.restricted\_user

</td><td>

-   Provides access to Creator Studio
-   Users can't create new apps

</td><td>

-   catalog\_builder\_editor
-   sn\_creatorstudio.app\_requestor
-   sn\_collab\_request.basic\_write
-   sn\_udc.basic\_read
-   sn\_creatorstudio.basic\_read
-   sn\_collab\_request.basic\_read
-   app\_template\_runner

</td></tr><tr><td>

sn\_creatorstudio.basic\_read

</td><td>

Primitive read access to Creator Studio resources

</td><td>

 

</td></tr><tr><td>

sn\_creatorstudio.basic\_write

</td><td>

Primitive write access to Creator Studio resources

</td><td>

 

</td></tr><tr><td>

sn\_creatorstudio.admin

</td><td>

Admin write access to Creator Studio**Note:** App Engine admins \(app\_engine\_admin\) with this role are not restricted from accessing ServiceNow Studio in the experience switcher.

</td><td>

sn\_creatorstudio.admin\_write

</td></tr><tr><td>

sn\_creatorstudio.admin\_write

</td><td>

Admin write access to Creator Studio

</td><td>

-   sn\_creatorstudio.basic\_read
-   sn\_creatorstudio.basic\_write

</td></tr><tr><td>

sn\_creatorstudio.app\_requestor

</td><td>

Primitive app requester access to Creator Studio resources

</td><td>

 

</td></tr><tr><td>

sn\_creatorstudio.basic\_fulfiller

</td><td>

Gives some fulfillers the following:-   Access to the Request App Workspace
-   Ability to edit some fields in the sn\_creatorstudio\_task table

</td><td>

canvas\_user

</td></tr></tbody>
</table>## Tables installed with Creator Studio

<table id="table_dhl_j4l_51c"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Request Subtask \[sn\_creatorstudio\_child\_task\]

</td><td>

Extends the Task table.

</td></tr><tr><td>

New Application Admin Task \[sn\_creatorstudio\_new\_application\_admin\_task\]

</td><td>

Extends the Task table.

</td></tr><tr><td>

New Application Task \[sn\_creatorstudio\_new\_application\_task\]

</td><td>

Extends the Task table.

</td></tr><tr><td>

Request App Config \[sn\_creatorstudio\_request\_app\_config\]

</td><td>

Extends the Application File table.

</td></tr><tr><td>

Request Task \[sn\_creatorstudio\_task\]

</td><td>

Table where all requests from apps made in Creator Studio are stored.**Note:**

-   You must have the Request Task table installed on the production instance as well as the non-production instance.
-   Admins can change the underlying table that each app in Creator Studio uses. However, the tables in this topics are still installed by default.

</td></tr><tr><td>

Creator Studio Activities \[sn\_creatorstudio\_activity\]

</td><td>

Table where all standard and custom activities for Creator Studio automations are stored.**Note:** This table is readable by Creator Studio users and delegated developers.

</td></tr></tbody>
</table>**Parent Topic:**[Installing Creator Studio from the ServiceNow Store](../concept/installing-creator-studio-from-the-store.md)

