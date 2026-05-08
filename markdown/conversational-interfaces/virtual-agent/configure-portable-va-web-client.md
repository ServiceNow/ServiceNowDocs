---
title: Configure the portable Virtual Agent chat widget
description: Configure the portable Virtual Agent chat widget to run Virtual Agent on third-party web pages.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Adding Virtual Agent to your web page, Configure, Virtual Agent, Conversational Interfaces]
---

# Configure the portable Virtual Agent chat widget

Configure the portable Virtual Agent chat widget to run Virtual Agent on third-party web pages.

## Before you begin

**Note:** For new customers onboarding from Vancouver onward, the chat widget is only accessible to authenticated users by default. To allow unauthenticated users to access the chat widget, you must enable the sn\_va\_web\_client\_app\_embed page for public access. For more information, see Make UI pages public or private.

Role required: admin

## About this task

ServiceNow only supports the portable Virtual Agent when the top-level domain and domain name match the site that is loading the chat widget. SSO is only supported through the service-now.com URL. Anything beyond that will require custom solution and implementation.

## Procedure

1.  Navigate to **All**, and then enter `sys_properties.list` in the filter.

2.  In the System Properties \[sys\_properties\] table, search for the **com.glide.cs.embed.csp\_frame\_ancestors** property by name.

3.  Click the property name to open the form and specify the directive values.

<table id="table_mny_mrp_ktb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Type

</td><td>

**string** This is the default value.

</td></tr><tr><td>

Value

</td><td>

Source value of the HTTP header directive: `Content-Security-Policy:frame-ancestors<source>`This property applies to most major browsers, except for Internet Explorer. Specify one or more sources, including the following:

-   **'self'**: Indicates that the origin is the same as the page being served. For example, if the value is **'self' http://mywebsite.com**, then the iframe is embedded within the parent domain as well as mywebsite.com. This is the default value.
-   **host-source**: The domains in which the external web page can be embedded. Specify the Internet host site by name, IP address, or optional URL and/or port number. Site address can start with a wildcard \(asterisk\) character. Example value: **http://\*.example.com**
-   **scheme-source**: A schema. For example: **http:** or **https:**
-   **none**: No matching URLs.


</td></tr></tbody>
</table>4.  Return to the System Properties \[sys\_properties\] table to search for the **com.glide.cs.embed.xframe\_options** property by name.

5.  Click the property name to open the form and specify the directive values.

<table id="table_mrd_5v5_4qbxxxxx"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Type

</td><td>

**string** This is the default value.

</td></tr><tr><td>

Value

</td><td>

Value of the of the X-Frame-Options header directive, to indicate whether the browser can render an external web page in a frame. Specify one of the following values:

-   **sameorigin**: Displays the page in a frame that has the same origin as the page itself. This is the default value. This property applies to older browsers, such as Internet Explorer 11. Example value: **allow from https://example.com**
-   **deny**: Does not display the page in a frame.
-   **allow-from uri**: Displays the page only in a frame on the specified origin.

**Note:** This value no longer works in modern browsers.

</td></tr></tbody>
</table>6.  Configure CORS Rules for the REST API to give access across domains.

    This rule gives the web domain you specify the rights to call the API that gives it access to the chat widget on the web page without a security restraint. All domains must share a common parent domain. Also, you must create a new CORS Rule for each subdomain that you want to support.

    1.  Navigate to **All** &gt; **System Web Services** &gt; **REST** &gt; **CORS Rules**.

    2.  Click **New**.

    3.  On the form, fill in the fields.

<table id="table_cvf_c5p_ktb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name for the rule.

</td></tr><tr><td>

Application

</td><td>

Scope of the application. **Global** is the default value.

</td></tr><tr><td>

REST API

</td><td>

Name of the REST API. Select **Conversation Consumer Account \[now/cs\]**.

</td></tr><tr><td>

Domain

</td><td>

The domain for your website. For example: **https://mycompany.com** If you have multiple subdomains for your website, you must create a CORS Rule for each. For example, **support.mycompany.com** and **products.mycompany.com** would require two separate CORS Rules.

 **Note:** Wildcards are not allowed.

</td></tr><tr><td>

Max age

</td><td>

The number of seconds to cache the client session. After an initial CORS request, further requests from the same client within the specified time do not require a preflight message.If you do not specify a value, the default value of **0** indicates that all requests require a preflight message.

</td></tr></tbody>
</table>    4.  On the **HTTP Methods** tab, select **GET**.

        The portable chat widget will only receive requests.

    5.  Click **Submit**.

    6.  Repeat these steps if you want to add the portable chat widget to another subdomain on your website.

7.  Create a JavaScript script that uses the**window.postMessage\(\)** method \(Web API\) to define event conditions that trigger SSO authentication in a user interface page and returns users to a chat widget page that you specify.

    To redirect users to a chat widget page, use the following string: `"https://<your-instance>.service-now.com/sn_va_web_client_login.do?sysparm_redirect_uri=’ + encodeURIComponent(<your-page>)`

    **Note:** Before you run the script, use the **com.glide.cs.web\_client\_login\_redirect\_urls** system property to specify the URLs that can be passed in the script. The redirection works only when you specify one or more allowed URLs in the property value. Specify the full redirect URLs or the host part of the URL. For example: `https://example.com` .

    Example script

    ```
    <script>
        window.addEventListener("message", function(e) {
           // redirect to SSO login if the chat widget logs in but is logged in as a guest user(unauthenticated)
          if(e.data.type==="SESSION_CREATED" && e.data.authenticated === false)
            window.location.href = "https://<your-instance>.service-now.com/sn_va_web_client_login.do?sysparm_redirect_uri=<’ + encodeURIComponent(<your-page>);
          
          // redirect to SSO login if the ServiceNow platform logs out from underneath the chat widget
          if(e.data.type==="SESSION_LOGGED_OUT")
            window.location.href = "https://<your-instance>service-now.com/"https://<your-instance>service-now.com/sn_va_web_client_login.do?sysparm_redirect_uri=’ + encodeURIComponent(<your-page>);
        });
      </script>
    ```

    In this example, authentication is triggered in the specified instance when the SESSION\_CREATED or SESSION\_LOGGED\_OUT events occur. After authentication \(when the SSO credentials for users are accepted\), users are redirected to the embedded chat widget page that you specified in `sn_va-web_client_login.do?sysparm_redirect_uri=’ + encodeURIComponent(<your-page>)`, as long as you also specified the page URL in the **com.glide.cs.web\_client\_login\_redirect\_urls** property.


## What to do next

[Add the portable Virtual Agent chat widget to a third-party website](add-portable-va-client-website.md).

**Parent Topic:**[Use the portable chat widget to add Virtual Agent to your web page](../concept/use-portable-va-web-client.md)

