---
title: Connect your instance with CPQ instance
description: Set up the connections between the ServiceNow instance and the CPQ instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/connect-sn-instance-logik.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Without guided setup, Setting up CPQ Configurator, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Connect your instance with CPQ instance

Set up the connections between the ServiceNow instance and the CPQ instance.

## Before you begin

Role required: admin

## Procedure

1.  Set the application scope to CPQ Integration.

    Use the scope selection menu icon \[Omitted image "globe-outline-24.svg"\] Alt text: in the Unified Navigation menu to select the scope.

2.  Navigate to `https://<service_instance_url>/oauth_entity.do?sys_id=3b119df83b566210a0c0989e53e45a15`.

    1.  Update the Redirect URL to `https://<tenant-url>/login/oauth2/code/<tenant-name>-login`.

        -   The tenant-name is the name of the CPQ site. The tenant-url is the full URL of the site \(for example, cpq-som.test.logik.io\)
        -   Example: `https://logiksite-som.test.logik.io/login/oauth2/code/logiksite-som-login`
    2.  Select the **Activate** property.

    3.  Select **Update**.

3.  In the filter, enter `sys_properties.list`.

    1.  Open the **sn\_cpq\_intg.tenant\_url** system property.

    2.  Set the **Value** to `https://<tenant-url>.cpq`

    3.  Select **Update**.

4.  Validate that the connection to the CPQ site is valid by navigating to **All** &gt; **CPQ Administration** and open the CPQ site \(listing no blueprints by default\).

    If this fails to open, check the previous steps for typos and trailing slashes.

5.  Generate the admin API key in CPQ.

    1.  In CPQ, login as admin user and navigate to **Select Utilities** &gt; **Admin API Keys**.

    2.  Specify a name and user ID \(with the same name: by default, "admin"\).

    3.  Select **Permissions as Admin**.

        This will automatically select Read, Edit, Deploy, and Bulk.

    4.  Set an expiration date far in the future.

    5.  Select **Save** and copy the token.

        **Note:** Be sure to do this step. After the confirmation window is closed, the token is no longer accessible.

6.  Populate the connection and credential aliases.

    1.  In ServiceNow Sales CRM, navigate to `https://<service_instance_url>/now/workflow-studio/integration/connection`

    2.  Select **Advanced Setup of the CPQ – Sync connection**.

    3.  Open the CPQ–sync connection.

        -   Set the connection URL to `https://<tenant-url>.cpq`.
        -   Ensure that there is no ending slash.
        -   Make the connection active, if it is not already.
        -   Select **Save**.
    4.  From the CPQ–sync connection, select the CPQ–sync token in the Credential column.

    5.  Set the API key to `Bearer {admintoken}` and add the value of the token that you copied in step 5e, and then select **Save**.

        Example: `Bearer _53eT_sxJHJ5rcfgXe8-8LDEK3Of1zHpQ`


## What to do next

[Set up an external connection in CPQ](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/set-up-external-connection-logik.md)

**Related topics**  


[Request a CPQ tenant](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/set-up-logik-instance.md)

