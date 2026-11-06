---
title: Create connection and credential form fields
description: The Create Connection and Credential form enables you to create a connection and credential record for the Workday HR spoke to authorize actions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/employee-service-management/hr-service-delivery/cereate-connection-and-cred-form.html
release: australia
product: HR Service Delivery
classification: hr-service-delivery
topic_type: reference
last_updated: "2026-10-27"
reading_time_minutes: 1
breadcrumb: [Reference, HR Service Delivery Advanced Integration with Workday, Integration of HR Service Delivery with third-party systems, HR Service Delivery, Employee Service Management]
---

# Create connection and credential form fields

The Create Connection and Credential form enables you to create a connection and credential record for the Workday HR spoke to authorize actions.

<table id="table_phx_xrr_1lc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name to uniquely identify the record. For example, `Workday HR Connection`.

</td></tr><tr><td>

Connection URL

</td><td>

URL to connect to your Workday HR instance.

</td></tr><tr><td>

Tenant Name

</td><td>

Tenant name of your Workday application.

</td></tr><tr><td>

API Version

</td><td>

Version of theWorkday API to use for requests.

</td></tr><tr><td>

Client ID

</td><td>

Client ID generated in Workday for OAuth authentication.

</td></tr><tr><td>

Client Secret

</td><td>

Client Secret generated in Workday for OAuth authentication.

</td></tr><tr><td>

Authorization URL

</td><td>

URL used to authorize the OAuth connection. Use this format: `https://<auth-domain-name>.workday.com/<tenant>/authorize`

</td></tr><tr><td>

Token URL

</td><td>

URL used to generate the OAuth token. Use this format: `https://<workday_host>/token`

</td></tr><tr><td>

OAuth Redirect URL

</td><td>

URL where Workday redirects after successful authentication. Use this format: `https://<instance_name>.service-now.com/oauth_redirect.do`

</td></tr></tbody>
</table>**Parent Topic:**[Reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/hr-service-delivery/reference-hr-service-delivery-advanced-integration-with-workday.md)

