---
title: Set up External Connection in Logik
description: Set up an External Connection in Logik by copying the Client ID and Client Secret of the Logik.ai Auth record.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2025-12-07"
reading_time_minutes: 1
breadcrumb: [CPQ Configurator, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Set up External Connection in Logik

Set up an External Connection in Logik by copying the Client ID and Client Secret of the Logik.ai Auth record.

## Before you begin

Role required: admin

## Procedure

1.  In Sales and Order Management, navigate to: https://&lt;service\_instance\_url&gt;/oauth\_entity.do?sys\_id=99a63a9e2baeea1001bff246f291bf57

    We will use the integration we created to set up an External Connection in Logik.

2.  Copy the Client ID and Client Secret.

3.  In Logik, navigate to **Utilities** &gt; **Exernal Connections**.

4.  Select **New**.

5.  Set the name to pricing.

    If you give a different name, it will require updating the default Enrichment scripts to point to the varname given.

6.  Select “External” under “Integration Type”

7.  Select “OAuth - Client Credentials Flow” for ‘Authentication Type’

8.  Fill in Client ID and Client Secret you copied in step 2.

    Token URL is: https://&lt;site&gt;.service-now.com/oauth\_token.do

9.  Scope: useraccount

10. HTTP method: POST

11. Host: https://&lt;site&gt;.service-now.comstep

12. Path: “/\{\{pricingPath\}\}”step

13. Body: “\{\{pricingRequest\}\}”

14. Ensure the Content Type is application/json.

15. Save.

16. Navigate to **Utilities** &gt; **Settings**, then set the Pricing Connection to the newly created connection.


