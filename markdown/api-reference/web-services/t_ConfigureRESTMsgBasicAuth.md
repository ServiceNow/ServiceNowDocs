---
title: Configure a REST message with basic auth
description: Configure an outbound REST message to provide basic authentication credentials with each request.
locale: en-US
release: yokohama
product: Web Services
classification: web-services
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Outbound REST authentication, Outbound REST web service, Outbound web services, Web services, API implementation, API implementation and reference]
---

# Configure a REST message with basic auth

Configure an outbound REST message to provide basic authentication credentials with each request.

## Before you begin

Before starting this procedure, ensure there is a REST Message record that you want to configure to use basic auth.

**Note:** Ensure any scripts that call this REST message use the RESTMessageV2 API. The RESTMessageV2 API is required to send authenticated REST messages via scripts.

Role required: web\_service\_admin

## Procedure

1.  Navigate to **All** &gt; **System Web Services** &gt; **Outbound** &gt; **REST Message**.

2.  Select a REST message record.

3.  In the **Authentication type** field, select **Basic**.

    **Note:** The **Basic \(Simple\)** choice appears on REST message records configured to use basic authentication prior to the Geneva release. This choice is intended for compatibility with older REST messages and should not be used for REST messages created in the Geneva release or later.

4.  In the **Basic auth profile** field, select the basic authentication profile that contains the credentials you want to send.

5.  Click **Submit**.


## What to do next

Test the REST message to ensure you receive the expected response. You can optionally specify different authentication settings for each HTTP method related to this REST message, overriding the parent REST message settings.

-   **[Create a basic auth profile](t_CreateABasicAuthProfile.md)**  
Create a basic auth profile to specify basic authentication credentials for one or more REST messages.

**Parent Topic:**[Outbound REST authentication](../concept/c_OutboundRESTAuth.md)

