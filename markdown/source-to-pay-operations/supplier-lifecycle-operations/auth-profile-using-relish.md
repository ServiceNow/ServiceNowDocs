---
title: Set up authentication profile using Relish credentials
description: Create a basic authentication profile that can be used for web service integration with Relish. Register the Relish user name and password to create the authentication profile.
locale: en-US
release: australia
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Relish Integration, Integrate, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Set up authentication profile using Relish credentials

Create a basic authentication profile that can be used for web service integration with Relish. Register the Relish user name and password to create the authentication profile.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **Connections &amp; Credentials** &gt; **Connection &amp; Credential Aliases**.

2.  Click **New**.

3.  Enter a unique name for the alias and set the **Type** value to **Credential**.

4.  Click **Submit**.

    A new credential alias with a unique ID is created.

5.  In the Credentials related list, click **New** and then select **Basic Auth Credentials**.

6.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the authentication configuration.|
    |Username|User name as provided by Relish.|
    |Password|Password as provided by Relish. This username and password is used to authenticate the HTTP request when this basic authentication profile is enabled.|
    |Credential alias|Credential alias created for the Relish configuration. This alias is auto-populated when you create an authentication profile from a credential alias.|

7.  Click **Submit**.


**Parent Topic:**[Relish Integration for Supplier Lifecycle Operations](../concept/relish-slo-connector.md)

**Related topics**  


[Relish Integration for Supplier Lifecycle Operations](../concept/relish-slo-connector.md)

