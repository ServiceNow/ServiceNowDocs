---
title: Create a remote task using Workflow Studio in Service Exchange for Providers
description: As a provider, proactively create remote tasks for your customers by using Workflow Studio.
locale: en-US
release: xanadu
product: Service Bridge
classification: service-bridge
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Create remote task definitions in Service Exchange for Providers, Installing and configuring Service Exchange for Providers, Service Exchange for Providers, Service Exchange]
---

# Create a remote task using Workflow Studio in Service Exchange for Providers

As a provider, proactively create remote tasks for your customers by using Workflow Studio.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Flow Designer**.

2.  On the Flow Designer landing page's main header, select **New** &gt; **Flow**.

3.  In the Flow properties window, fill in the following fields.

    |Field|Action|
    |-----|------|
    |Flow name|Enter the name of your flow|
    |Description|Description of your flow|
    |Application|Global|
    |Domain|Global|
    |Protection|None|
    |Run As|System User|

4.  Under the TRIGGER section, select **Add a trigger**.

5.  In the Trigger section, fill in the following fields and click **Done**.

    |Field|Value|
    |-----|-----|
    |Trigger|`Created or Updated`.|
    |Table|Table name that you want to create for your consumer. For example, a Case \[sn\_customerservice\_case\].|
    |Condition|Details of the filter. For example, `Account` is `consumer-name`.|
    |Run Trigger|For every update|

    **Note:** For Advanced Option fields, don't change any values.

6.  Under the ACTIONS section, select **Add an Action, Flow Logic, or Subflow**.

7.  Click **Action** &gt; **Service Exchange for Providers** &gt; **Create remote task for Consumer**.

8.  Fill in the following fields.

    |Field|Value|
    |-----|-----|
    |Action|**Create remote task for Consumer**|
    |Task record \[Task\]|**Trigger - Record Created or Updated - Record**|
    |Remote task def record|Select the remote task definition from the list.|

9.  Select **Done** and click **Save**.


## Result

A remote task is created on your \(provider\) ServiceNow instance and it gets synchronized on the consumer's ServiceNow instance.

