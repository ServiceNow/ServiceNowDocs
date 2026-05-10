---
title: Migrating your data from a lower environment to a higher environment in RPA Hub
description: As a system administrator, after you restructure the RPA Hub tables to extend the Application file \(sys\_metadata\), you can use the update set capability to migrate your data from a lower \(non-production\) environment to a higher \(production\) environment for real-time use.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 7
keywords: [bot process configuration update set rpa hub, update set bot process configuration rpa hub]
breadcrumb: [Migrate data, RPA Hub, Workflow Data Fabric]
---

# Migrating your data from a lower environment to a higher environment in RPA Hub

As a system administrator, after you restructure the RPA Hub tables to extend the Application file \(sys\_metadata\), you can use the update set capability to migrate your data from a lower \(non-production\) environment to a higher \(production\) environment for real-time use.

There are two ways you can migrate your data from a lower environment to a higher environment:

-   Using the update set capability described in this page for migrating your data from one environment to another environment
-   Using the **Migrate** button in RPA Hub

    In RPA Hub, you can migrate the bot process configuration and associated assets from one environment to another environment with a click of a button. After the migration is complete, you will have to create a bot process record, create credentials, make necessary changes, and then publish the bot process. For more information, see [Migrating the bot process configuration in RPA Hub](bot-process-migration.md).


## Restructured RPA Hub tables \(Tokyo and earlier releases\)

For more information about the restructuring of the RPA Hub tables, see [Restructuring RPA Hub tables](restructured-rpa-hub-tables-utah.md).

For more information about update sets, see [Get started with update sets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/system-update-sets/get-started-update-sets.md).

## Functionality

The metadata of the automation \(package, package version, schedules, and so on\) is captured in the update set. System administrator then moves the update set to a higher \(production\) environment.

The metadata records are moved to the higher \(production\) environment but the package version does not contain an automation zip file.

RPA release manager manually downloads the zip file from the lower \(non-production\) environment and then uploads it to a higher \(production environment\). RPA admin can also perform this action. However, this task is restricted to classic environment.

RPA release manager automatically imports package version attachments by selecting the **Import Attachment** button on a package version. RPA admin can also perform this action. A flow is then triggered asynchronously and pulls the attachment from the configured connection using API. The automation zip file is attached to the package version and HashCode validation is performed automatically. An email is also sent to the user who performs the import attachment action.

To execute the orchestration of RPA Hub update sets from third-party tools, it is essential to recreate bot process on the higher environment. The **Change Life Cycle Stage Status of a Bot Process** action in Workflow Studio helps in ensuring the deployment and enablement of RPA Hub process is automated. For more information about this action, see [Workflow Studio actions and subflow in RPA Hub](../reference/rpa-hub-actions.md).

## List of steps for the migration tasks

Use this list of steps to guide you through all the tasks of the migration.

Complete all the tasks for a step before moving on to the next step.

Do the steps in the order that they’re presented.

<table id="table_ar4_w1b_5vb"><thead><tr><th>

Task

</th><th>

Environment

</th></tr></thead><tbody><tr><td>

1. [Create and select an update set as the current set](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/system-update-sets/create-select-update-set.md).

</td><td>

Lower \(non-production\) environment

</td></tr><tr><td>

2. [Create a bot process configuration record in RPA Hub](../task/create-botprocess-config.md#).

</td><td>

Lower \(non-production\) environment

</td></tr><tr><td>

3. [Adding details to your bot process in RPA Hub](post-req-bot-process-rpa.md).

</td><td>

Lower \(non-production\) environment

</td></tr><tr><td>

4. [Mark your current update set complete](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/system-update-sets/t_CompleteUpdateSets.md).

</td><td>

Lower \(non-production\) environment

</td></tr><tr><td>

5. [Export to XML](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/system-update-sets/t_SaveAnUpdateSetAsAnXMLFile.md).

</td><td>

Lower \(non-production\) environment

</td></tr><tr><td>

6. [Download a package version in RPA Hub](../task/download-package-version.md).Perform this task, if you are manually migrating the package attachment \(automation zip file\) from a lower \(non-production\) to a higher \(production\) environment.

You can skip step 12.

</td><td>

Lower \(non-production\) environment

</td></tr><tr><td>

7. Switch to higher instance. [Retrieve an update set](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/system-update-sets/t_RetrieveAnUpdateSet.md).

</td><td>

Higher \(production\) environment

</td></tr><tr><td>

8. [Preview a remote update set](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/system-update-sets/t_PreviewARemoteUpdateSet.md).

</td><td>

Higher \(production\) environment

</td></tr><tr><td>

9. [Commit an update set](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/system-update-sets/t_CommitAnUpdateSet.md).

</td><td>

Higher \(production\) environment

</td></tr><tr><td>

10. [Associate a bot process to a bot process configuration record](../task/select-botprocess.md#).

</td><td>

Higher \(production\) environment

</td></tr><tr><td>

11. [Verify the associated schedules, parameters, packages, and queues in RPA Hub](../task/verify-botprocess-tasks.md).

</td><td>

Higher \(production\) environment

</td></tr><tr><td>

12. If the instance connection is established with a required lower \(non-production\) instance, perform this import task.To establish an instance connection, create an active connection in the **RPA Automation Package** connection and credential alias. Ensure to provide the lower \(non-production\) environment in the **Connection URL** field. For more information, see [Create an HTTP\(s\) connection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/connections-and-credentials/create-https-connection.md).

Perform this task if you are automatically migrating the package attachment \(automation zip file\) from a lower \(non-production\) to a higher \(production\) environment.

[Import a package version attachment in RPA Hub](../task/import-attachment-package-version.md).

You can skip step 13 and 14.

</td><td>

Higher \(production\) environment

</td></tr><tr><td>

13. [Upload an automation package attachment in RPA Hub](../task/upload-package-version-attach.md).Perform this task in classic environment.

</td><td>

Higher \(production\) environment

</td></tr><tr><td>

14. [Verify the HashCode of a package version in RPA Hub](../task/view-hash-code.md).

</td><td>

Higher \(production\) environment

</td></tr><tr><td>

15. [Assign a business application to a bot process in RPA Hub](../task/associate-business-apps.md).

</td><td>

Higher \(production\) environment

</td></tr><tr><td>

16. [Create a credential group in RPA Hub](../task/create-credential-group.md#).

</td><td>

Higher \(production\) environment

</td></tr><tr><td>

17. [Assign a robot to a bot process in RPA Hub](../task/assign-robots.md).

</td><td>

Higher \(production\) environment

</td></tr><tr><td>

18. [Assign a process robot credential within a bot process in RPA Hub](../task/assign-process-robot-cred-botprocess.md).

</td><td>

Higher \(production\) environment

</td></tr><tr><td>

19. [Assign an attended user or group to an attended bot process](../task/assign-rda-users-botprocess.md).

</td><td>

Higher \(production\) environment

</td></tr></tbody>
</table>-   **[Import a package version attachment in RPA Hub](../task/import-attachment-package-version.md)**  
Import package version attachments automatically instead of manually uploading a package version attachment, by selecting the **Import Attachment** button on a package version.
-   **[Upload an automation package attachment in RPA Hub](../task/upload-package-version-attach.md)**  
Upload a zip file of the automation package in RPA Hub to manually migrate the package from a lower \(non-production\) to a higher \(production\) environment.

**Parent Topic:**[Migrating data in RPA Hub](migrating-data-rpa-hub.md)

