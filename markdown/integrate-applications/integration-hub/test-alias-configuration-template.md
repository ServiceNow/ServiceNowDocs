---
title: Create a test action to test a connection alias from a configuration template
description: For connection aliases using a configuration template, you can create a test action that enables you to test the connection directly from the Action Properties section of actions contained in a flow in Workflow Studio.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Supporting multiple connections, Manage connections, Integration Hub, Workflow Data Fabric]
---

# Create a test action to test a connection alias from a configuration template

For connection aliases using a configuration template, you can create a test action that enables you to test the connection directly from the Action Properties section of actions contained in a flow in Workflow Studio.

## Before you begin

Role required: admin

Plugin required: Integration Hub Starter

To test a connection alias with a test action, the connection alias must be associated with a configuration template. You can check if an alias already has a configuration template by navigating to **All** &gt; **Integration Hub** &gt; **Connection &amp; Credential Aliases**, selecting the alias record from the list, and checking the **Configuration Template** field.

If you don't have a connection alias or an associated configuration template, you can create them. For step-by-step instructions on setting up a configuration template, see [Create a configuration template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/connections-and-credentials/create-template.md). After you create a configuration template, you can [Create a Connection &amp; Credential alias](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/connections-and-credentials/connection-alias.md) and associate it with the template by adding the template name to the **Configuration Template** field.

## About this task

This task is divided into two main steps. The first step describes how to create a test action in Workflow Studio that uses the alias you want to test. The second step describes how to add the name of the test action to the **Test Action** field in the configuration template.

## Procedure

1.  Create a test action in Workflow Studio.

    1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

    2.  In Workflow Studio, select **New**, then **Action**.

    3.  On the New Action form, enter a name in the **Action name** field.

        This name is the name that you’ll add to the **Test Action** field in the configuration template.

    4.  Fill out the rest of the form, then select **Build action**.

    5.  In the action, add a new step by selecting the plus icon, then select **REST**.

    6.  On the form, enter the following field values, then select **Save**.

        |Field|Value|
        |-----|-----|
        |Connection|**Use Connection Alias**|
        |Connection Alias|&lt;name of the connection alias to test&gt;|
        |Build Request|**Manually**|
        |HTTP Method|**GET**|
        |If this step fails|**Stop the action and go to error evaluation**|

2.  Add the name of the test action to the **Test Action** field in the configuration template.

    1.  Navigate to **All** &gt; **Integration Hub** &gt; **Configuration Templates**.

    2.  Select the template associated with the connection alias you're testing and enter the name of the action in the **Test Action** field, then select **Save**.


## What to do next

Test your connection directly in the Action Properties section of an action contained in a flow in Workflow Studio. For details, see Action-level connection selection in [Supporting multiple connections](../concept/support-multiple-connections.md).

