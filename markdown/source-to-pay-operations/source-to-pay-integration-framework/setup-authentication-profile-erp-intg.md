---
title: Set up the authentication profile
description: Create a basic authentication profile that can be used for web service integration with ERP. Register the ERP integration user name and password to create the authentication profile and associate it to service maps.
locale: en-US
release: xanadu
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Integration settings on Source-to-Pay side, Source-to-Pay integration framework, Source-to-Pay integration with third-party applications, Source-to-Pay Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Set up the authentication profile

Create a basic authentication profile that can be used for web service integration with ERP. Register the ERP integration user name and password to create the authentication profile and associate it to service maps.

## Before you begin

-   Verify that the application scope is set to Finance – ERP Integration.
-   Credentials required: ERP integration user credentials provided by ERP.

Role required: sn\_fcms\_intg.integration\_user

## About this task

If the application needs to support multiple ERP instances, create a separate credential alias and authentication profile for each instance.

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
    |Username|User name as provided by ERP.|
    |Password|Password as provided by ERP. This username and password is used to authenticate the HTTP request when this basic authentication profile is enabled.|
    |Credential alias|Credential alias created for the ERP configuration. This alias is auto-populated when you create an authentication profile from a credential alias.|

7.  Click **Submit**.


## What to do next

Configure service maps for the source configuration and associate the basic authentication profile to these service maps.

