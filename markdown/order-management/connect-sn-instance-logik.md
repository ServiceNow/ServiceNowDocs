---
title: Set up ServiceNow instance connection with CPQ instance
description: Set up the connections between the ServiceNow instance and the ServiceNow CPQ instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/order-management/connect-sn-instance-logik.html
release: zurich
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Without guided setup, CPQ Configurator, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Set up ServiceNow instance connection with CPQ instance

Set up the connections between the ServiceNow instance and the ServiceNow CPQ instance.

## Before you begin

Role required: admin

## Procedure

1.  Set the application scope to CPQ Integration using the scope selection menu icon \[Omitted image "globe-outline-24.svg"\] Alt text: in the Unified Navigation menu.

2.  Navigate to `https://<service_instance_url>/oauth_entity.do?sys_id=3b119df83b566210a0c0989e53e45a15`.

    1.  Update the Redirect URL to `https://<tenant-url>/login/oauth2/code/<tenant-name>-login`.

        -   The tenant-name is the name of the `<service_instance>` site \(for example, logiksite-som\). The tenant-url is the full URL of the site \(for example, logiksite-som.test.logik.io\)
        -   Example: `https://logiksite-som.test.logik.io/login/oauth2/code/logiksite-som-login`
        **Note:** The redirect URL details is provided in the email that you receive after the request for a new ServiceNow CPQ instance is complete.

    2.  Select **Activate** check-box.

    3.  Select **Update**.

3.  Navigate to **All** and enter `sys_proprties.list` in the **Filter** search box.

    1.  Open the **sn\_cpq\_intg.tenant\_url** system property.

    2.  Enter `https://<tenant-url>.logik.io` in the **Value** field.

    3.  Select **Update**.

4.  Navigate to **All** &gt; **CPQ Administration** to validate the connection to ServiceNow CPQ.

    If ServiceNow CPQ fails to open, check the previous steps for any incorrect values \(typos and trailing slashes\).

5.  Generate the Admin API key in ServiceNow CPQ.

    1.  Log in as admin and navigate to **All** &gt; **CPQ Administration** &gt; **Utilities** &gt; **Admin API Keys**.

    2.  Enter the values for **Name** and **User ID**.

        Enter the same value for both the fields. The default value is admin.

    3.  Set an Expiration Date far in the future.

    4.  Select **Admin** permissions.

        This will auto select Read, Edit, Deploy, and Bulk.

    5.  Select **Save** and copy the token.

        **Important:** Be sure to do this step. After closing the confirmation modal, the token will no longer be accessible.

6.  Populate the Connection and Credential Aliases.

    1.  In ServiceNow Sales CRM, navigate to `https://<service_instance_url>/now/workflow-studio/integration/connection`

    2.  Select **Advanced Setup** of the **CPQ – Sync** connection.

    3.  Select **CPQ –Sync Connection** in the **Connections** related list.

        -   Enter `https://<logik-tenant-url>.logik.io` in the **Connection URL** field. Ensure there is no ending slash added in the connection URL value.
        -   Select **Active** check-box \(if not already\).
        -   Select **Submit**.
    4.  Select the value **CPQ – Sync Token** in the **Credential** column of the **CPQ –Sync Connection** record in the **Connections** related list.

    5.  In the **API Key** field, enter the value Bearer \{admintoken\}, replacing \{admintoken\} with the token copied from Step 5e.

        For example: Bearer \_53eT\_sxJHJ5rcfgXe8-8LDEK3Of1zHpQ

    6.  Select **Save**.


