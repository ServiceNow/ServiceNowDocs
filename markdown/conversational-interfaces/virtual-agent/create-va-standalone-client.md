---
title: Embed the Virtual Agent chat widget in an external web page \(legacy method\)
description: Load the Virtual Agent chat widget interface in an external web page by using an inline frame element \(iframe\). You can also optionally enable the single sign-on \(SSO\) authentication process to run automatically for guest users who are using the chat widget and are not logged in.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Adding Virtual Agent to your web page, Configure, Virtual Agent, Conversational Interfaces]
---

# Embed the Virtual Agent chat widget in an external web page \(legacy method\)

Load the Virtual Agent chat widget interface in an external web page by using an inline frame element \(iframe\). You can also optionally enable the single sign-on \(SSO\) authentication process to run automatically for guest users who are using the chat widget and are not logged in.

## Before you begin

**Important:** Consider adding the Portable Virtual Agent Web Client to your web page instead. It reduces code complexity and is easier to implement. It also includes standard chat features, such as click actions for launching or closing the chat. For details, see [Add the portable Virtual Agent chat widget to a third-party website](add-portable-va-client-website.md).

-   In the iframe, you specify the URL of the instance to be embedded. If you're embedding the chat widget on any page that is not on your ServiceNow instance, the URL must be a custom instance URL. Due to increased browser security, the chat widget may fail to load if you don't use a custom URL. To learn more about using custom URLs, see [Associating custom URLs to your instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/authentication/custom-url.md).

    To use a custom URL, do the following:

    -   [Activate the custom url plugin \(com.snc.customurl\) in your instance.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/authentication/activate-custom-url-plugin.md)
    -   [Add the custom URL \(that you previously purchased and registered\) to your instance.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/authentication/configure-custom-url.md)
    **Note:** The Virtual Agent chat widget does not work from an iframe in Safari by default. Apple blocks cross-origin iframes \(when the domain of the URL used in the iframe does not match the domain of the website itself\).

-   After you embed the Virtual Agent client, you can optionally trigger SSO authentication from the chat widget, but only when your instance is set up to use an external SSO provider. Your hosting site must also use the same SSO provider as your instance. For details on setting SSO providers, see [External single sign-on \(SSO\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/authentication/c_MultipleProviderSingleSignOn.md).

    To trigger SSO authentication, you create a JavaScript script that defines conditions for running authentication and redirects users to a chat widget page that you specify \(see Step 2 below\). You also specify the allowed URLs that can be passed in this script, by identifying them in the **com.glide.cs.web\_client\_login\_redirect\_urls** system property. Specify the full redirect URLs or the host part of the URL, such as `https://example.com` .


Role required: admin

## About this task

This procedure requires that you set values for the following two system properties:

-   **com.glide.cs.embed.csp\_frame\_ancestors**
-   **com.glide.cs.embed.xframe\_options**

These properties determine the security policy for the embedded chat widget, namely how browsers render and secure HTML content for Virtual Agent and Live Agent chat, in an iframe, before you embed the web chat client.

To generate SSO authentication for your guest users, you can create a script that uses the `window.postMessage()` method \(Web API\) to trigger authentication and specify the URL where users are redirected after authentication. For more information on this method and Window objects, see [Window.postMessage\(\)](https://developer.mozilla.org/en-US/docs/Web/API/Window/postMessage).

**Note:** If you're using the Content Management System \(CMS\) application to create custom interfaces for the ServiceNow AI Platform and ServiceNow® applications, be aware that it does not support Virtual Agent.

## Procedure

1.  Set both the **com.glide.cs.embed.csp\_frame\_ancestors** and **com.glide.cs.embed.xframe\_options** system properties to specify the HTTP header directives for securing the iframe contents.

    The HTTP header directives tell the browser whether a page can be embedded on certain domains to mitigate clickjacking attempts. Setting both properties ensures that there are security directives for major browsers and also older browsers, such as Internet Explorer.

    1.  In the navigation filter, enter `sys_properties.list`.

    2.  In the System Property \[sys\_properties\] table, search for the **com.glide.cs.embed.csp\_frame\_ancestors** property by name.

        **Note:** This property sets the source value of the HTTP header directive: `Content-Security-Policy:frame-ancestors<source>`. Use the `host-source` value to specify the domains in which the external web page can be embedded. This property applies to most major browsers, except for Internet Explorer.

    3.  Click the property name to open the form and specify the directive values.

<table id="table_ecw_cz5_4qb"><thead><tr><th>

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

Specify one or more sources, including: -   **'self'**: Indicates that the origin is the same as the page being served. For example, if the value is **'self' http://mywebsite.com**, then the iframe is embedded within the parent domain as well as mywebsite.com. This is the default value.
-   **host-source**: The domains in which the external web page can be embedded. Specify the Internet host site by name, IP address, or optional URL and/or port number. Site address can start with a wildcard \(asterisk\) character. Example value: **http://\*.example.com**
-   **scheme-source**: A schema. For example: **http:** or **https:**
-   **none**: No matching URLs.


</td></tr></tbody>
</table>        For more information about source values that you can specify, see [CSP:frame-ancestors](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Content-Security-Policy/frame-ancestors#Syntax) and [Virtual agent embedded client content security policy \(instance security hardening\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/instance-security-hardening-settings/sc-publicly-exposed-virtual-agent-embedded-web-client.md) in [Hardening settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/instance-security-hardening-settings/security-hardening-settings.md).

    4.  Return to the System Property \[sys\_properties\] table to search for the **com.glide.cs.embed.xframe\_options** property by name.

        **Note:** This property sets the value of the of the X-Frame-Options header directive, to indicate whether the browser can render an external web page in a frame. Use the default `sameorigin` value to specify the domains in which the external web page can be embedded. This property applies to older browsers, such as Internet Explorer 11.

    5.  Click the property name to open the form and specify the directive values.

<table id="table_mrd_5v5_4qb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Type

</td><td>

string. Default value.

</td></tr><tr><td>

Value

</td><td>

Specify a value, including: -   `sameorigin`. Default value. Displays the page in a frame that has the same origin as the page itself. Example value: allow from https://example.com.
-   `deny`. Does not display the page in a frame.
-   `allow-from uri`. Displays the page only in a frame on the specified origin.

**Note:** This value no longer works in modern browsers.

</td></tr></tbody>
</table>        For more information about source values that you can specify, see [X-Frame-Options](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/X-Frame-Options#Syntax) and [Set Xframe options to prevent embedding third-party websites](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/instance-security-hardening-settings/sc-xframe-options.md) in [Hardening settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/instance-security-hardening-settings/security-hardening-settings.md).

2.  After associating your ServiceNow instance to a custom URL, create the iframe element and specify the custom URL in the inline element \(iframe\) used to embed the Virtual Agent client in an external web page: `"https://<your-domain>.com/sn_va_web_client_app_embed.do"`

    **Note:** Your instance may have multiple custom URLs, but only one instance URL. You must use your custom instance URL only.

    For example:

    ```
    <iframe id="sn_va_web_client"
        title="ServiceNow Virtual Agent Client"
        width="600"
        height="900"
        src="https://<your-domain>.com/sn_va_web_client_app_embed.do">
    "https://<your-domain>.com/"https://<your-domain>.com/</iframe>
    
    ```

    **Note:** Use the `?sysparm_skip_load_history=true` parameter at the end of the URL to load the interface without the conversation history.

3.  Create a JavaScript script that uses the `window.postMessage()` method \(Web API\) to define event conditions that trigger SSO authentication in a user interface page and returns users to a chat widget page that you specify.

    To redirect users to a chat widget page, use this string: `"https://<your-instance>.service-now.com/sn_va_web_client_login.do?sysparm_redirect_uri=’ + encodeURIComponent(<your-page>)`

    **Note:** Before you run the script, use the **com.glide.cs.web\_client\_login\_redirect\_urls** system property to specify the URLs that can be passed in the script. The redirection works only when you specify one or more allowed URLs in the property value. Specify the full redirect URLs or the host part of the URL, such as `https://example.com` .

    Example script:

    ```
    <script>
        window.addEventListener("message", function(e) {
           // redirect to SSO login if the chat widget logs in but is logged in as a guest user(unauthenticated)
          if(e.data.type==="SESSION_CREATED" && e.data.authenticated === false)
            window.location.href = "https://<your-instance>.service-now.com/sn_va_web_client_login.do?sysparm_redirect_uri="+ encodeURIComponent(location.href);
          
          // redirect to SSO login if the ServiceNow platform logs out from underneath the chat widget
          if(e.data.type==="SESSION_LOGGED_OUT")
            window.location.href = "https://<your-instance>service-now.com/sn_va_web_client_login.do?sysparm_redirect_uri=" + encodeURIComponent(location.href);
        });
      </script>
    ```

    In this example, authentication is triggered in the specified instance when the SESSION\_CREATED or SESSION\_LOGGED\_OUT events occur. After authentication \(when the SSO credentials for users are accepted\), users are redirected to the embedded chat widget page that you specified in `sn_va-web_client_login.do?sysparm_redirect_uri=’ + encodeURIComponent(<your-page>)`, as long as you also specified the page URL in the **com.glide.cs.web\_client\_login\_redirect\_urls** property.


**Parent Topic:**[Use the portable chat widget to add Virtual Agent to your web page](../concept/use-portable-va-web-client.md)

