---
title: Set a custom URL as the instance URL
description: Add a custom URL to your instance configuration to use instead of your ServiceNow URL.
locale: en-US
release: xanadu
product: Authentication
classification: authentication
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Custom URLs association to your instance, Authentication, Access Management]
---

# Set a custom URL as the instance URL

Add a custom URL to your instance configuration to use instead of your ServiceNow URL.

## Before you begin

Role required: admin

You must activate the custom URL plugin and have purchased or registered a URL before adding the custom URL to your instance.

## Procedure

1.  Navigate to **All** &gt; **Custom URL** &gt; **Custom URLs**.

2.  You should either:

    -   Click **New** to associate a new domain name that is new to your instance.
    -   Select a custom URL already set up to set as your instance URL.
3.  Fill in the appropriate fields:

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

Check box to enable this custom URL for all outbound URLs. Only one active custom URL can be the instance URL. To enable this setting for a custom URL, click **Set as Instance URL** on the URL record. Any previous custom URLs are then removed.

</td></tr><tr><td>

Status

</td><td>

Status of the custom URL record. If the status is **Active**, the custom URL is provisioned and ready to use.

</td></tr><tr><td>

Service Portal

</td><td>

Service portal that you want to use when you redirect users to your instance using the custom URL.

</td></tr><tr><td>

Identity Provider

</td><td>

Identity Provider for the custom URL enables you to allow users to auto-redirect to specified IdPs defined at the custom URL record.

</td></tr></tbody>
</table>    A custom URL should activate within six hours on your instance.

    **Note:**

    -   You must delete custom URL record from ServiceNow instance first and then delete any Domain Name Server \(DNS\) entries from the DNS server.
    -   Any deletion of DNS entry from DNS server prior to deletion of custom URL record from ServiceNow instance would result in blocking the deletion of other corresponding custom URL records from ServiceNow.

