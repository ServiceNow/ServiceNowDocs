---
title: Set up ServiceNow instance connection with Logik.ai instance
description: Set up the connections between the ServiceNow instance and the Logik.ai instance.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2025-12-07"
reading_time_minutes: 1
breadcrumb: [CPQ Configurator, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Set up ServiceNow instance connection with Logik.ai instance

Set up the connections between the ServiceNow instance and the Logik.ai instance.

## Before you begin

Role required: admin

## Procedure

1.  Set the application scope to CPQ Integration.

    Use the scope selection menu icon in the Unified Navigation menu to select the scope.

2.  Navigate to: https://&lt;service\_instance\_url&gt;/oauth\_entity.do?sys\_id=3b119df83b566210a0c0989e53e45a15

    1.  Update the Redirect URL to: https://&lt;logik-tenant-url&gt;/login/oauth2/code/&lt;logik-tenant-name&gt;-login

        -   The logik-tenant-name is the name of the logik site \(for example, logiksite-som\). The logik-tenant-url is the full URL of the site \(for example, logiksite-som.test.logik.io\)
        -   Example: https://logiksite-som.test.logik.io/login/oauth2/code/logiksite-som-login
    2.  Select the **Activate** property.

    3.  Select **Update**.

3.  In the filter, enter ``.

    1.  Open the **sn\_cpq\_intg.tenant\_url** system property.

    2.  Set the **Value** to `https://<logik-tenant-url>.logik.io`

    3.  Select **Update**.

4.  Validate that the connection to the Logik site is valid by navigating to **All** &gt; **CPQ Administration** and open the Logik site \(listing no Blueprints by default\).

    If this fails to open, check the previous steps for typos and trailing slashes.

5.  Generate the Admin API key in Logik.

    1.  In Logik, login as admin user and navigate to **Select Utilities** &gt; **Admin API Keys**.

    2.  Specify a Name and User ID \(with the same name, by default admin\).

    3.  Select Permissions as Admin.

        This will auto select Read, Edit, Deploy, and Bulk.

    4.  Set an Expiration Date far in the future.

    5.  Select **Save** and copy the Token.

        **Note:** Be sure to do this step. After closing the confirmation modal, the token will no longer be accessible.

6.  Populate the Connection and Credential Aliases.

    1.  In SOM, navigate to: https://&lt;service\_instance\_url&gt;/now/workflow-studio/integration/connection

    2.  Select Advanced Setup of the CPQ – Sync connection.

    3.  Open the CPQ –Sync Connection.

        -   Set the Connection URL to: https://&lt;logik-tenant-url&gt;.logik.io
        -   Ensure there is no ending slash.
        -   Make the connection Active \(if not already\).
        -   Select **Save**.
    4.  From the CPQ – Sync Connection, select the CPQ – Sync Token in the Credential column.

    5.  Set the API Key to be “Bearer \{admintoken\}” and add the value copied in step 5e, then select **Save**.

        For example: Bearer \_53eT\_sxJHJ5rcfgXe8-8LDEK3Of1zHpQ


