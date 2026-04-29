---
title: Set up a custom URL as the instance URL
description: Add a custom URL to your instance configuration to use instead of your ServiceNow URL. This custom URL ensures that embedded components remain accessible in your browser, even when third-party cookies are turned off.
locale: en-US
release: australia
product: Customer Self-service and Omnichannel Engagement
classification: customer-self-service-and-omnichannel-engagement
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Set up Web EmbeddablesWeb Embeddable, Configure Web Embeddables, Set up self-service, Configure, Customer Service Management]
---

# Set up a custom URL as the instance URL

Add a custom URL to your instance configuration to use instead of your ServiceNow URL. This custom URL ensures that embedded components remain accessible in your browser, even when third-party cookies are turned off.

## Before you begin

-   You must Activate the custom URL plugin. For more information, see [Activate custom URLs](https://www.servicenow.com/docs/access?context=activate-custom-url-plugin&version=australia&pubname=australia-platform-security&ft:locale=en-US).
-   You must purchase or register a URL before adding the custom URL to your instance.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Custom URL** &gt; **Custom URLs**.

2.  You should either:

    -   Select New to associate a new domain name that is new to your instance.
    -   Select a custom URL that has already been set up as your instance URL.
3.  On the form, fill in the fields.

<table id="table_dbr_fzd_llb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Domain Name

</td><td>

Fully qualified domain name \(FQDN\) of the custom URL. The FQDN is a CNAME redirect created in the name server record for the custom domain.**Note:** For example, in the name server for acme.com, you might create an entry:

```
support.acme.com 300 IN CNAME acme.servicenow.com 
```

</td></tr><tr><td>

Is Instance URL

</td><td>

Option to enable this custom URL for all outbound URLs. Only one active custom URL can be the instance URL. To enable this setting for a custom URL, select **Set as Instance URL** on the URL record. Any previous custom URLs are then removed.

**Note:** If you set this as the instance URL, it automatically replaces any previously set custom URL that was used as the instance URL.

</td></tr><tr><td>

Status

</td><td>

Displays the status of the custom URL record. If the status is **Active**, the custom URL is provisioned and ready to use.

</td></tr><tr><td>

Service Portal

</td><td>

Service portal that you want to use when you redirect users to your instance using the custom URL.

</td></tr><tr><td>

Identity Provider

</td><td>

Identity Provider for the custom URL enables you to allow users to auto-redirect to specified IdPs defined at the custom URL record.

</td></tr></tbody>
</table>    A custom URL should activate within several hours on your instance.

    **Note:**

    -   You must delete the custom URL record from ServiceNow instance first and then delete any Domain Name Server \(DNS\) entries from the DNS server.
    -   Any deletion of a DNS entry from DNS server prior to deletion of custom URL record from ServiceNow instance results in blocking the deletion of other corresponding custom URL records from ServiceNow.

