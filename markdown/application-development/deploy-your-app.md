---
title: Deploy your app
description: Once the application is built and validated, the application needs to be moved to the production environment. Applications can be moved through an application repository or by using Update Sets. Applications should be deployed to test environments prior to moving to production.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Exploring professional development, Building pro-code applications, Developing your application, Building applications]
---

# Deploy your app

Once the application is built and validated, the application needs to be moved to the production environment. Applications can be moved through an application repository or by using Update Sets. Applications should be deployed to test environments prior to moving to production.

## Application Repository \(App Repo\)

Publishing an application to the App Repo makes this version of the application available to all of an organization’s ServiceNow instances. Use the App Repo to deploy an application to QA / Test instances \(for testing\) and finally to Production \(Prod\) instances.

![Deploy apps through the Application Repository](../image/deploy-app-repo.png)

For more information, see [Publishing an application to the application repo](https://servicenow.com/docs/bundle/paris-application-development/page/build/applications/task/t_PublishAppsToTheAppRepository.html), [Install an application](https://servicenow.com/docs/bundle/paris-application-development/page/build/applications/task/t_InstallApplications.html).

## Update Sets

If the application repository cannot be used to deploy applications, use Update Sets instead. The diagram shows the best practice lifecycle of an Update Set to deploy a customization from the development instance to the test instance.

![Deploy apps using Update Sets](../image/deploy-update-sets.png)

Practices that lead to a quality development and release process:

-   Always move customizations from the bottom of the stack up.
    -   Ensures down-stack instances match up-stack instances.
    -   Customizations introduced mid-stack can be overwritten by future pushes from down-stack.
    -   Common scenarios include:
        -   Fixes need in test or prod – always push them from dev up
        -   Common Prod admin customization, such as choice lists – always push updates from dev up
-   Always review updates contained in an Update Set before transferring.
    -   Look for updates associated with other development efforts and updates associated with testing.
    -   Watch for system properties and integration end-points changes. Ex: pushing sys\_properties change that directs all email to test email account
    -   Move updates to a “scrap” Update Set rather than deleting the update.
-   Always test after pushing to ensure that all desired customizations are captured and applied as expected.
-   In situations with multiple, parallel releases, ensure communication and coordination between the development teams.
-   Avoid experimenting on the development instance, because customizations can be captured accidentally and migrated by other team members.
-   Do not capture development in the Default Update Set.

List all user Story numbers with a short description in the **Description** field of an Update Set. Include all manual steps that are required to deploy the Update Set.

Some typical examples of manual steps that are needed for a deployment that are not captured in an Update Set:

-   Plugin activation.
-   Transfer of tables that are not tracked in the Update Set \(typically, starting with “x\_” or “u\_”\).
-   Creation of database indexes on the tables. The index creation is not tracked via Update Set and needs to be done manually.

## Update Set management

Be sure the correct Update Set is selected when working on a story or a defect and check the records in the Update Set daily.

Do not manually move sys\_update\_xml records between Update Sets. The only exception is to move a record to the Default Update Set.

Update Sets capture configuration information but not task or process data. For example, Update Sets track Service Catalog item definitions and related configuration data like variables and variable choices. However, the orders \(requests, items, catalog tasks\) placed in testing are not tracked by Update Sets.

Be aware of Update Set DOs and DON’Ts:

-   To remove a specific sys\_update\_xml record from the current Update Set, move the record to the Default Update Set and populate the **sys\_update\_set.comments** field of the record with the reason for moving the record to the Default Update Set.
-   Never move customization records from one Update Set to another Update Set.
-   Never delete an Update Set unless the Update Set has been merged successfully into a new Update Set.
-   Always use data extracts or Import Sets to move data from one instance to other \(and not Update Sets\).

## Update Set batching

Batch Update Sets to preview and commit Update Sets in bulk.

Dealing with multiple Update Sets can lead to problems, including committing Update Sets in the wrong order or inadvertently leaving out one or more sets. Avoid these problems by grouping completed Update Sets into a batch.

The system organizes Update Set batches into a hierarchy. One Update Set can act as the parent for multiple child Update Sets. A given set can be both a child and parent, enabling multiple-level hierarchies. One Update Set at the top level of the hierarchy acts as the base Update Set.

Previewing or committing the base Update Set previews or commits the entire batch. The system determines the processing order, and checks for collisions based on the dates the changes were recorded and on their sequential ancestry. Their ancestries are the specific instances in which the changes in the Update Sets took place.

Update set batching can be applied to releases, where an empty parent Update Set is created for the release, and actual Update Sets are included in the release as children.

Advantages of using Update Set batching are:

-   Individual Update Sets can be removed from the release at the last moment.
-   Batching is similar to merging, except batching allows updates to be removed.
-   Batch Update Sets are easy to deploy. Only the Parent Update Set needs to be processed.

For more information, see [System update sets](https://servicenow.com/docs/bundle/paris-application-development/page/build/system-update-sets/concept/system-update-sets.html).

## What to do next

Now that the app is deployed, think about how to improve and enhance it. Here are some suggestions for determining where to go next:

-   The people using the application day-to-day will be the best source of feedback. Talk to them about what new features or changes they would like to see.
-   Determine if additional related process flows can be automated through Flow Designer.
-   Determine if new IntegrationHub spokes can be leveraged for new integrations.

