---
title: Version records
description: The sys\_update\_version table contains records that represent the state of a customizable object at a particular time.
locale: en-US
release: zurich
product: Team Development
classification: team-development
topic_type: reference
last_updated: "2025-10-02"
reading_time_minutes: 1
breadcrumb: [Team Development Reference, Team Development, Planning your application, Building applications]
---

# Version records

The sys\_update\_version table contains records that represent the state of a customizable object at a particular time.

A customizable record is any object that is tracked by update sets, such as business rules or script includes. A new version record is created automatically whenever a customizable record is changed or changes the application file for the customizable record.

<table id="table_bqn_rf3_bq"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

A unique identifier for coalescing versions of the same customized record.

</td></tr><tr><td>

Record name

</td><td>

Name of the customized record.

</td></tr><tr><td>

Source

</td><td>

Indicator of how the version was added on the instance.-   System upgrade: From a baseline version software upgrade.
-   Update Set: From an update set that was created or committed on the instance.
-   Pull History: From a pull in Team Development.

</td></tr><tr><td>

State

</td><td>

Indicator of whether the version is or has ever been loaded on the instance.-   Current: The version is loaded.
-   Previous: The version has previously been loaded on the instance. When a current version is replaced by a new version, it becomes a previous version.
-   History: The version was never loaded on the instance and was only inserted for historical purposes, such as when pulling versions from the parent in Team Development.

</td></tr><tr><td>

Application

</td><td>

The application for the customized record, if it’s assigned to an application.

</td></tr><tr><td>

Payload

</td><td>

The data for this version of the customized record.

</td></tr><tr><td>

Reverted from

</td><td>

A reference to the older version record, if this version was created by [reverting to an older version](../task/t_RevertAChange.md). This field is only visible in the list view.

</td></tr><tr><td>

Instance Name

</td><td>

The name of the remote instance where the version was originally created. This field is added by configuring the form.

</td></tr><tr><td>

Instance ID

</td><td>

The URL of the remote instance where the version was originally created. This field is added by configuring the form.

</td></tr><tr><td>

Version List

</td><td>

All versions of the customized record that are available on the instance. This field is only visible in the form view.

</td></tr></tbody>
</table>**Parent Topic:**[Team Development Reference](team-development-reference.md)

