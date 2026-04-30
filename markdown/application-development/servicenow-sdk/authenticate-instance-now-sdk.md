---
title: Authenticating to a ServiceNow instance with the ServiceNow SDK
description: Authenticate to a ServiceNow instance and store user credentials for accessing the instance on your system with the ServiceNow SDK.
locale: en-US
release: xanadu
product: ServiceNow SDK
classification: servicenow-sdk
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [ServiceNow SDK, Building applications in source code, Building pro-code applications, Developing your application, Building applications]
---

# Authenticating to a ServiceNow instance with the ServiceNow SDK

Authenticate to a ServiceNow instance and store user credentials for accessing the instance on your system with the ServiceNow SDK.

You can use basic or OAuth 2.0 credentials to authenticate to an instance. To use OAuth 2.0 authentication, your instance must have ServiceNow IDE \(version 1.1 or later\) installed or have the required XML configuration imported. By default, instances on the Xanadu release include ServiceNow IDE version 1.1.4 and support using OAuth 2.0 authentication with the ServiceNow SDK.

After authenticating to an instance with the ServiceNow SDK command-line interface \(CLI\), you can begin developing applications and installing them on your instance. A non-production instance should be used for application development.

-   **[Authenticate to a ServiceNow instance using basic authentication with the ServiceNow SDK](../task/authenticate-instance-basic-auth.md)**  
Use basic authentication to connect to a ServiceNow instance with the ServiceNow SDK.
-   **[Authenticate to a ServiceNow instance using OAuth 2.0 with the ServiceNow SDK](../task/authenticate-instance-oauth.md)**  
Use OAuth 2.0 authentication to connect to a ServiceNow instance with the ServiceNow SDK.

**Parent Topic:**[ServiceNow SDK](servicenow-sdk-landing.md)

