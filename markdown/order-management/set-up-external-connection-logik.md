---
title: Set up an external connection in CPQ
description: Set up an external connection in CPQ by copying the client ID and client xecret of the Logik.ai Auth record.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [CPQ Configurator, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Set up an external connection in CPQ

Set up an external connection in CPQ by copying the client ID and client xecret of the Logik.ai Auth record.

## Before you begin

Role required: admin

## Procedure

1.  In ServiceNow Sales CRM, navigate to `https://<service_instance_url>/oauth_entity.do?sys_id=99a63a9e2baeea1001bff246f291bf57`.

    We will use the integration we created to set up an external connection in CPQ.

2.  Copy the client ID and the client secret.

3.  In CPQ, navigate to **Utilities** &gt; **External Connections**.

4.  Click **New**.

5.  Set the name to `pricing`.

    If you enter a different name, you must update the default enrichment scripts to point to the varname.

6.  Under **Integration Type**, select **External**.

7.  For **Authentication Type**, select **OAuth - Client Credentials Flow**.

8.  Enter the client ID and client secret that you copied in step 2.

    The token URL is `https://<site>.service-now.com/oauth_token.do`.

9.  Set the remaining details as follows:

    -   Scope: useraccount
    -   HTTP method: POST
    -   Host: https://&lt;site&gt;.service-now.comstep
    -   Path: `“/{{pricingPath}}”step`
    -   Body: `“{{pricingRequest}}”`
10. Make sure that the content type is `application/json`.

11. Click **Save**.

12. Navigate to **Utilities** &gt; **Settings** and set the pricing connection to the newly created connection.


