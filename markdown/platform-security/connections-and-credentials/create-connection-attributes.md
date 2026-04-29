---
title: Create connection attributes for IntegrationHub
description: Define connection-specific variables that you can use in Integration Hub integration steps.
locale: en-US
release: australia
product: Connections and Credentials
classification: connections-and-credentials
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Get started with connections, Connections and Credentials, Access Management]
---

# Create connection attributes for IntegrationHub

Define connection-specific variables that you can use in Integration Hub integration steps.

## Before you begin

Role required:

-   The admin role is required to create connection attributes.
-   The connection\_admin or admin role is required to assign attribute values.
-   The action\_designer or admin role is required to use attributes in a custom action.

Connection attributes are only used by integration steps, which require a subscription to Integration Hub. For more information about activating Integration Hub, see [Request an Integration Hub plugin](https://www.servicenow.com/docs/access?context=request-integrationhub&version=australia&pubname=australia-integrate-applications&ft:locale=en-US).

## About this task

When using an integration step, you must establish a connection with an external system. Use a Connection &amp; Credential alias instead of defining the connection inline. An alias enables you to update the connection details once without having to reconfigure every action. Any action step that uses an alias inherits the attributes associated with it. Workflow Studio displays attributes as data pills that you can drag into your action step. For example, you can create a page size attribute that becomes a REST step query parameter.

For more information about building custom Workflow Studio actions, see [Workflow Studio](https://www.servicenow.com/docs/access?context=actions&version=australia&pubname=australia-build-workflows&ft:locale=en-US).

## Procedure

1.  Navigate to **All** &gt; **Credentials &amp; Connections** &gt; **Connection &amp; Credential Aliases**.

2.  Create or select an alias record.

3.  From the Connection Attributes related list, click **New**.

4.  Define the attribute label and field type.

    For a list of field types, see [field types](https://www.servicenow.com/docs/access?context=r_FieldTypes&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

5.  Click the Advanced view related link to set advanced dictionary preferences for the attribute.

    For example, to create an attribute with a dynamically calculated value. See [Dictionary entry form](https://www.servicenow.com/docs/access?context=r_DictionaryEntryForm&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

6.  Click **Submit**.

7.  Define the attribute values in the connection record.

    1.  Navigate to **Credentials &amp; Connections** &gt; **Connections**.

    2.  Create or select a connection record with the same connection type as the alias.

    3.  From **Connection alias**, select the alias with connection attributes.

    4.  Save the record.

        The Attributes tab populates with the connection attributes defined in the alias record.

    5.  Set values for the attributes.

        If the alias has **Support Multiple Active Connections** enabled, you can associate more than one connection record with an alias and define attribute values in each connection record. If there are multiple connection records with attribute values for the same alias, the connection used when the flow executes determines the attribute values. For example, suppose that you have one action that uses an alias with two active connections endpoints: production and test. The attribute resolves to the value defined by the connection used at runtime.

8.  Add the alias to an integration step in Workflow Studio.

    1.  Navigate to Workflow Studio and create or select an action.

    2.  Add an integration step to the action.

    3.  Under Connection Details, add the alias you created attributes for.

    The connection attributes associated with the alias display as data pills in the Data pane.

    **Note:** The system does not track changes to connection attribute labels and data types after you associate the alias to a step. To refresh the connection attribute label or data type, delete the alias from the step and add it again.


**Parent Topic:**[Get started with connections](../reference/connection-information.md)

