---
title: Set up the Wiz environment
description: You must obtain the credentials associated with the Wiz service account to configure Wiz for use with the Service Graph Connector for Wiz.
locale: en-US
release: yokohama
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Wiz, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Set up the Wiz environment

You must obtain the credentials associated with the Wiz service account to configure Wiz for use with the Service Graph Connector for Wiz.

## Before you begin

Role required: Wiz user with a role that has Write \(W\) permission on service accounts

## About this task

To create a service account, you must be logged in as a Wiz user with Write \(W\) permission on service accounts. Project-scoped roles can create service accounts only on their own projects.

For more information on obtaining Wiz details, see [Add a Service Account](https://docs.wiz.io/wiz-docs/docs/service-accounts-settings#add-a-service-account) on the Wiz documentation site \(requires Wiz login\).

## Procedure

1.  Log in to your Wiz dashboard.

2.  Obtain the Wiz URL.

    1.  Navigate to your user profile and copy the API Endpoint URL.

        **Note:** The Service Graph Connector for Wiz uses the following token URL:

        ```
        https://auth.app.wiz.io/oauth/token
        ```

3.  Obtain the client ID and client secret.

    1.  Navigate to **Settings** &gt; **Service Accounts**.

    2.  Select **Add Service Account**.

    3.  Name the new service account.

    4.  In the Projects list, select projects to limit access of the service account.

    5.  In the **API Scopes** field, select the permissions read:resources and read:projects.

    6.  Select **Add Service Account**.

    7.  From the Copy your secret credentials dialog box that appears, copy the client secret and client ID from their respective fields.

    8.  Select **Finish** to return to the Wiz dashboard.


