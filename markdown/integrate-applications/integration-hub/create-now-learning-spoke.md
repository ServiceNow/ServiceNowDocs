---
title: Set up the ServiceNow University spoke
description: Connect ServiceNow University with Coaching with Learning to pull courses from ServiceNow University into your ServiceNow instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/integrate-applications/integration-hub/create-now-learning-spoke.html
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-09-02"
reading_time_minutes: 2
breadcrumb: [ServiceNow University Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up the ServiceNow University spoke

Connect ServiceNow University with Coaching with Learning to pull courses from ServiceNow University into your ServiceNow instance.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the ServiceNow University spoke.
-   Role required: admin.

-   Integrate Coaching with Learning with ServiceNow University. For more information, see [External Content Integration Sources](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/integration-source-coaching-with-learning-coaching-wfo-itsm.md).
-   Contact [nowlearningapi@servicenow.com](mailto:nowlearningapi_servicenow.com) to get your spoke credentials.

    **Note:** You must have an ITSM Enterprise license subscription to get your spoke credentials.

-   For more information on OAuth Credentials, see [OAuth 2.0 credentials](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-security/oauth-2-credentials.md).

**Note:** If you are using an earlier version of the ServiceNow University spoke and want to upgrade to ServiceNow University spoke v1.1.1, you must delete the existing connection and credential records.

To delete the existing connection and credential record:

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Connection &amp; Credential Aliases**.
2.  Search and open the default connection and credential record for the ServiceNow University spoke. For example, **ServiceNow University**.
3.  Under the **Connections** tab, open the default HTTP\(s\) Connection record. For example, **ServiceNow University Connection**.
4.  Click **Delete**. System prompts you confirm delete action.
5.  Click **Delete**.
6.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Credentials**.
7.  Search and open the default credential record for the Ansible spoke. For example, **ServiceNow University Credential**.
8.  Click **Delete**. System prompts you confirm delete action.
9.  Click **Delete**.

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  Click the **Integrations** tab.

3.  Under **Connections**, toggle and enable the **Outbound** connections.

4.  Locate the alias for **Now Learning** and click **View Details**.

    -   To configure the default connection and credential alias record that is shipped along with the ServiceNow University spoke, click **View Details**.

        \[Omitted image "image.now-learning-conf-temp"\] Alt text:

    -   To manage more than one ServiceNow University spoke connection records, you should create a new child alias record by clicking **Add Connection**. For more information about using multiple connections, see [Supporting multiple connections](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/integration-hub/support-multiple-connections.md).
    If you are configuring the spoke for the first time, click **Configure**. Otherwise, click **Edit**.

    \[Omitted image "image.now-learning-conf-temp2"\] Alt text:

5.  On the form, fill in these fields:

<table id="table_hcp_4b1_lkc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td colspan="2">

**Connection Information**

</td></tr><tr><td>

Connection Name

</td><td>

A unique name for the connection; for example, Now Learning.

</td></tr><tr><td>

Connection URL

</td><td>

The ServiceNow server to retrieve the API information.**Default value**: [https://api.servicenow.com](https://api.servicenow.com).

</td></tr><tr><td>

Ocp-Apim-Subscription-Key

</td><td>

Encryption key for the ServiceNow University subscription. Contact [nowlearningapi@servicenow.com](mailto:nowlearningapi_servicenow.com) to get your encryption key.

</td></tr><tr><td colspan="2">

**Credential Information**

</td></tr><tr><td>

Credential Name

</td><td>

A unique name for the credential; for example, ServiceNow University Credential.

</td></tr><tr><td>

Application Registry Name

</td><td>

A unique name for the application registry; for example, ServiceNow University OAuth.

</td></tr><tr><td>

Token URL

</td><td>

OAuth server token endpoint in this format: `https://servicenowsignon.okta.com/oauth2/<id>/v1/token`. Replace `<id>` with the value of `authorizationServerId`.

</td></tr><tr><td>

Client Id

</td><td>

The Client ID of the application registered in the third-party OAuth server. Contact [nowlearningapi@servicenow.com](mailto:nowlearningapi_servicenow.com) to get your Client ID.

</td></tr><tr><td>

Client Secret

</td><td>

The Client Secret of the application registered in the third-party OAuth server. Contact [nowlearningapi@servicenow.com](mailto:nowlearningapi_servicenow.com) to get your client secret.

</td></tr></tbody>
</table>    \[Omitted image "image.now-learning-temp"\] Alt text:

6.  Click **Save and Get OAuth Token**.


