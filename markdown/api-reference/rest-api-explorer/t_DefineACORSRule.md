---
title: Define a CORS rule
description: You can define a CORS rule to control which domains can access REST API endpoints and other web resources.
locale: en-US
release: australia
product: REST API Explorer
classification: rest-api-explorer
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [REST APIs, Web services, API implementation, API implementation and reference]
---

# Define a CORS rule

You can define a CORS rule to control which domains can access REST API endpoints and other web resources.

## Before you begin

Role required: cors\_rule\_admin, web\_service\_admin, or admin

## Procedure

1.  Navigate to **All** &gt; **System Web Services** &gt; **REST** &gt; **CORS Rules**.

2.  Select **New**.

3.  On the form, fill in the fields.

<table id="table_o13_rs3_ls"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Enter a unique name for the rule.

</td></tr><tr><td>

Use Resource Path

</td><td>

Select this option to specify a path to a web resource. For REST APIs, leave this option cleared.

</td></tr><tr><td>

REST API

</td><td>

Select the REST API for the domain to access, such as the Table API.

</td></tr><tr><td>

Web Resource Path

</td><td>

If you selected **Use Resource Path**, enter a path to the web resource for the domain to access.

</td></tr><tr><td>

Domain

</td><td>

Enter the domain to access the specified REST API or web resource. This CORS rule is evaluated against requests from the specified domain.You can specify a domain pattern or an IP address. When using a domain pattern, you can use the wildcard character \(`*`\) to match incoming origin headers.

</td></tr><tr><td>

Max age

</td><td>

Enter the number of seconds to cache the client session. After an initial CORS request, further requests from the same client within the specified time don’t require a preflight message.If you don’t specify a value, the default value of 0 indicates that all requests require a preflight message.

</td></tr><tr><td>

For Embeddables

</td><td>

Reserved for future use.

</td></tr><tr><td>

Active

</td><td>

Select this option turn on the CORS rule.

</td></tr></tbody>
</table>4.  Select the **HTTP Methods** tab and the HTTP methods allowed.

    Only the selected methods can be called from the specified domain.

5.  Select the **HTTP Headers** tab and fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Access-Control-Allow-Credentials|Option to allow sending credentials in the request. If this option is enabled, you can't use a wildcard in the **Domain** field.|
    |Access-Control-Allow-Headers|Enter a comma-separated list of HTTP headers to allow in the request or the wildcard character \(`*`\) to allow any header.|
    |Access-Control-Expose-Headers|Enter a comma-separated list of HTTP headers to send in the response.|

6.  Select **Submit**.


**Parent Topic:**[REST APIs](../concept/c_RESTAPI.md)

