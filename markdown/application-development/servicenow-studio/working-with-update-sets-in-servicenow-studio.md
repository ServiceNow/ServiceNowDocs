---
title: Working with update sets in ServiceNow Studio
description: An update set is a group of configuration changes that can be moved from one instance to another. This feature allows administrators to group a series of changes into a named set and then move them as a unit to other systems for testing or deployment.
locale: en-US
release: yokohama
product: ServiceNow Studio
classification: servicenow-studio
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Using ServiceNow Studio, Building applications with ServiceNow Studio, Developing your application, Building applications]
---

# Working with update sets in ServiceNow Studio

An update set is a group of configuration changes that can be moved from one instance to another. This feature allows administrators to group a series of changes into a named set and then move them as a unit to other systems for testing or deployment.

If you're an admin, you might work with update sets in ServiceNow Studio to move changes through your instances. Access update sets from within an individual application or from the **Deployment** tab. Most of the ways you can interact with update sets in ServiceNow Studio are very similar to how you would use them on the ServiceNow AI Platform. For more information about tasks you can accomplish with update sets, see [System update sets](../../system-update-sets/concept/system-update-sets.md).

Administrators have the following options with update sets.

-   Create an update set to store local changes.
-   Select the current update set to store local changes.
-   Commit an update set to prepare it for distribution.
-   Report on the contents of update sets.
-   Compare update sets to determine what differences they contain.
-   Merge separate update sets into a single update set.
-   Create an external file from an update set.
-   Retrieve update sets from remote instances.
-   Apply retrieved update sets.
-   Back out changes applied from an update set.
-   Set system properties related to update sets.

Delegated developers have the following options with update sets in ServiceNow Studio.

-   Create an update set to store local changes.
-   Switch between update sets easily using the update set picker.
-   Package changes for deployment using the **Publish** button in any app.

    **Note:** If your app was created in ServiceNow IDE and converted to Fluent, you must switch from ServiceNow Studio back into the ServiceNow IDE for the publishing and deployment process.


-   **[Create an update set in ServiceNow Studio](../task/sn-studio-create-update-set.md)**  
Create an update set to package app changes for deployment in ServiceNow Studio.
-   **[Mark an update set complete in ServiceNow Studio](../task/mark-update-set-complete.md)**  
Mark an update set as **Complete** in ServiceNow Studio to enable your changes to be retrieved by other instances.

**Parent Topic:**[Using ServiceNow Studio](using-servicenow-studio.md)

