---
title: When to use Team Development
description: Team Development allows multiple developers to work on applications.
locale: en-US
release: xanadu
product: Team Development
classification: team-development
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Team Development overview, Team Development, Planning your application, Building applications]
---

# When to use Team Development

Team Development allows multiple developers to work on applications.

<table id="table_jbx_trm_5y"><thead><tr><th>

Deployment option

</th><th>

Good for

</th><th>

Future considerations

</th></tr></thead><tbody><tr><td>

Update Sets

</td><td>

Storing changes to a base system or installed application.Storing and applying a particular version of an application.

 Producing a file for export.

</td><td>

You can manually create update sets to store a particular application version.Use update sets to deploy patches or changes to installed applications.

 **Note:** Don’t use update sets to install applications. Instead, use the application repository or the ServiceNow Store to install applications.

</td></tr><tr><td>

Application Repository

</td><td>

Installing and updating applications on all company instances. Automatically managing application update sets.

 Restricting access to applications to the same company.

 Deploying completed applications to end users.

</td><td>

Consider uploading an application to the ServiceNow Store to share it with other users.

 Allows installation of and update to the latest application version only.

 Use update sets to store prior application versions.

 **Note:** If used with team development, publish applications only from a parent instance.

</td></tr></tbody>
</table>**Parent Topic:**[Team Development overview](../concept/c_UsingTeamDevelopment.md)

