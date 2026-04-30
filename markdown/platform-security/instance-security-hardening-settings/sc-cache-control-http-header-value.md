---
title: Cache-Control HTTP Header Value \[Updated in Security Center 1.3 and removed in 1.5\]
description: Use the glide.http.cache\_control property to set the default cache-control value in the HTTP response headers that the ServiceNow AI Platform sends when requesting static content data for a page. Examples of static content include images, CSS, and JavaScript rendered from within, for a page.
locale: en-US
release: xanadu
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2024-02-01"
reading_time_minutes: 2
breadcrumb: [Configuration, Hardening settings, Platform Security]
---

# Cache-Control HTTP Header Value \[Updated in Security Center 1.3 and removed in 1.5\]

Use the **glide.http.cache\_control** property to set the default cache-control value in the HTTP response headers that the ServiceNow AI Platform sends when requesting static content data for a page. Examples of static content include images, CSS, and JavaScript rendered from within, for a page.

The **glide.http.cache\_control** property sets the default Cache-Control value in HTTP response headers to **private** or **public**. The default is **private**.

|Value|Description|
|-----|-----------|
|private|Static content can be cached at the browser \(client\) level, but not at the proxy server level.|
|public|Static content can be cached at the browser \(client\) level, and also at the proxy server level.|

The Expires value in the HTTP response headers control when the static content expires, and has a default value of 369 days. To manually override the default value, use the **glide.http.expire.days** property.

![Control-Cache and Expires HTTP response header values](../../security/image/Cache-Control-header.png)

**Note:** You can use the **glide.http.cache** property designate whether to enable or disable setting of the Cache-Control and Expires values in HTTP response headers. Its default is **true**, which allows you to set the:

-   Cache-Control value default using the **glide.http.cache\_control** property.
-   Expires value default using the **glide.http.expire.days** property.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Property name

</td><td>

**glide.http.cache\_control**

</td></tr><tr><td>

Configuration type

</td><td>

System Properties \(/sys\_properties\_list.do\)

</td></tr><tr><td>

Category

</td><td>

[Configuration](sc-configuration.md)

</td></tr><tr><td>

Purpose

</td><td>

To configure the Cache-Control HTTP response header value for static content.

</td></tr><tr><td>

Recommended value

</td><td>

private

</td></tr><tr><td>

Default value

</td><td>

private

</td></tr><tr><td>

Security risk rating

</td><td>

4.3

</td></tr><tr><td>

Functional impact

</td><td>

Sets the default Cache-Control value in an HTTP response header.

</td></tr><tr><td>

Security risk

</td><td>

\(High\) If you set this property to **public**, instances with CDN/proxies may cache static content and render without authentication. -   **private** is a more appropriate setting for instances with CDN/proxy setup.
-   If an the instance does not have a CDN/proxy setup, either value should be fine.

</td></tr></tbody>
</table>To learn more about adding or creating a system property, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=xanadu&pubname=xanadu-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

**Parent Topic:**[Configuration](sc-configuration.md)

