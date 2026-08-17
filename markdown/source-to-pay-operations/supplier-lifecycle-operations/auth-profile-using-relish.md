---
title: Set up authentication profile using Relish credentials
description: Set up a basic authentication profile using Relish credentials to enable web service integration.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/source-to-pay-operations/supplier-lifecycle-operations/auth-profile-using-relish.html
release: zurich
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Relish Integration, Integrate, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Set up authentication profile using Relish credentials

Set up a basic authentication profile using Relish credentials to enable web service integration.

## Before you begin

Role required: admauthentication profile

## Procedure

1.  **nRelish credentialsConnections and CredentialsCredential aliasConfiguration formauthentication configurationBasic Auth Credentialsection &amp; Credential Aliases**.

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


## Result

The authentication profile is now linked and can be tested.

**Parent Topic:**[Relish Integration for Supplier Lifecycle Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/supplier-lifecycle-operations/relish-slo-connector.md)

**Related topics**  


[Relish Integration for Supplier Lifecycle Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/supplier-lifecycle-operations/relish-slo-connector.md)

