---
title: Create a Connection &amp; Credential alias
description: Define an alias to label a credential or connection record.
locale: en-US
release: australia
product: Connections and Credentials
classification: connections-and-credentials
topic_type: task
last_updated: "2026-05-08"
reading_time_minutes: 3
breadcrumb: [Get started with credentials, Connections and Credentials, Access Management]
---

# Create a Connection &amp; Credential alias

Define an alias to label a credential or connection record.

## Before you begin

Role required:

-   The admin role is required to create an alias.
-   The credential\_admin and connection\_admin roles have read access to the alias record.

## About this task

The Connection &amp; Credential alias defines an alias that labels a credential or connection record. The alias contains these fields.

## Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Connection &amp; Credential Aliases**.

2.  Click **New**.

3.  Complete the fields on the form.

<table id="table_bbg_xmn_gdb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the alias. An alias can only contain alpha, number, and underscore characters. During an upgrade, the tag in the credential record migrates to a Connection &amp; Credential Alias. If the credential tag contains special characters other than alphabets, numbers, and underscores, it preserves the tag name after the upgrade. You can still use this migrated alias, but you cannot update the alias until you change the name to meet the naming restrictions.

</td></tr><tr><td>

ID

</td><td>

Unique identifier for the Connections &amp; Credentials alias, based on the format `scope_name.alias_name`. -   If the scope is Global, the ID is the alias name. For example, if you create a Workday alias in the global scope, it sets the ID to `workday`.
-   If you create a workday alias in the HR app scope, it sets the ID to `x_hr_app.workday`.


</td></tr><tr><td>

Type

</td><td>

Select either **Credential** or **Connection and Credential**. The default is Connection and Credential.

</td></tr><tr><td>

Application

</td><td>

Application scope against which the Connection &amp; Credentials alias is assigned. The current session scope you last selected in the application picker appears. -   For example, **Global** appears if it is the current scope for this session.
-   You can change the scope in the application picker before creating an alias. To learn more application scopes and how to select them, see:
    -   [Application scope](https://www.servicenow.com/docs/access?context=c_ApplicationScope&version=australia&pubname=australia-application-development&ft:locale=en-US)
    -   [Select an application from the application picker](https://www.servicenow.com/docs/access?context=t_SelectAnAppFromTheAppPicker&version=australia&pubname=australia-platform-administration&ft:locale=en-US)


</td></tr><tr><td>

Connection type

</td><td>

Name of the connection type, either Basic, HTTP, JDBC, JMS, or Kafka. The default is HTTP.

</td></tr><tr><td>

Support Multiple Active Connections

</td><td>

Designator that indicates whether the alias supports multiple active connections. Add connections using the Connections table and associated them to the alias using the Connections related list.

</td></tr><tr><td>

Default Retry Policy

</td><td>

Retry policy for the alias. For more information, see [Retry policy](https://www.servicenow.com/docs/access?context=retry-policy&version=australia&pubname=australia-build-workflows&ft:locale=en-US).

</td></tr><tr><td>

Configuration Template

</td><td>

Configuration template to use to create a connection and credential record.

</td></tr></tbody>
</table>4.  Click **Save**.

    The Connections and Connection Attributes related list appears.

    |Related List|Description|
    |------------|-----------|
    |Connections|Related connection records associated with this alias. After creating the alias, you can define connection records and associate them with the alias. If **Support Multiple Active Connections** is selected, you can associate more than one connection with an alias.|
    |Connection Attributes|Attributes for the connection. Define data specific to a connection and use it in an Integration Hub integration step. For more information, see [Create connection attributes for IntegrationHub](create-connection-attributes.md).|
    |Child Aliases|Child aliases associated with the parent alias. After creating a connection and credential alias, you can create child alias to configure multiple connections for the same application integration.|

    |Related list|Description|
    |------------|-----------|
    |Connections|Related connection records associated with this alias. After creating the alias, you can define connection records and associate them with the alias. If **Support Multiple Active Connections** is selected, you can associate more than one connection with an alias.|
    |Connection Attributes|Attributes for the connection. Define data specific to a connection and use it in an Integration Hub integration step. For more information, see [Create connection attributes for IntegrationHub](create-connection-attributes.md).|

5.  If you want to create a new credential and connection associated with your credential alias, under **Related Links**, click **Create New Connection &amp; Credential**.

    The resulting connection and credential records are based on a pre-defined configuration template. See [connection and credential configuration templates](../concept/spoke-configuration-template.md).

6.  If you want to create a child alias for your connection and credential alias, under the **Child Aliases** related list, select **New**.

    1.  Enter a name for the child alias and select **Submit**.

        The child alias inherits properties from the parent alias. You can then configure a child alias to contain its own set of connection and credential information.


## What to do next

Create one or more connection records to associate with the alias or child aliases. For more information about creating connections, see [Get started with connections](../reference/connection-information.md). Add connection attributes to the alias to make connection meta data available to flows in Workflow Studio.

