---
title: Custom instance URLs
description: You can enable your ServiceNow instance to be accessible from a company-branded or custom URL.
locale: en-US
release: zurich
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Authentication, Access Management]
---

# Custom instance URLs

You can enable your ServiceNow instance to be accessible from a company-branded or custom URL.

## Custom URL overview

You can use custom URL to enable ServiceNow instance to be accessible from one or more company-branded or custom URLs.

Custom URLs can be associated with specific portal. For example, admin can define `http://support.acme.com` for CSM portal and `http://hr.acme.com` for HR portal. In such situation there is a need to redirect users to different IdPs for authentication on the basis of the custom URL that users are accessing.

**Important:**

-   Do not create a custom URL with more than 100 domains per instance.
-   You must delete custom URL record from ServiceNow instance first and then delete any Domain Name Server \(DNS\) entries from the DNS server.
-   Any deletion of DNS entry from DNS server prior to deletion of custom URL record from ServiceNow instance would result in blocking the deletion of other corresponding custom URL records from ServiceNow.

From Tokyo, you can allow users to auto-redirect to specified IdPs defined at the custom URL record.

**Note:** Custom URLs are not available for on-premise customers or developer instances. Also, the URL must be public-facing.

Only the owner of the top-level domain \(TLD\) or any subdomain can configure the custom URL to a DNS subdomain. For example, your instance might have the following designated URL and additional custom URLs:

|Example URLs|Usage|
|------------|-----|
|`https://acme.service-now.com`|The initial domain name for Acme that came with the ServiceNow instance.|
|`https://support.acme.com`|A custom URL that associates to your ServiceNow instance. This URL is referred to as an alias \(CNAME\) of the initial domain name.|
|`https://US-support.acme.com`|A secondary custom URL that associates to a service portal on your instance. Your instance can support multiple custom URLs to the same service portal.|

## Custom URL considerations outside of your instance

Before you can associate a custom URL, you must own \(or purchase\) a URL through a domain provider. There are also specific configurations necessary before you can create and associate a custom URL on your instance.

|Configuration items|Description|
|-------------------|-----------|
|Set the CNAME with the provider|The CNAME record must be set as the ServiceNow instance URL.|
|Determine your dedicated VIP status|The status of VIP.|

**Note:** When deleting or updating CNAME records which point to your instance, you must follow this sequence to avoid dangling records in the instance. First, delete the CNAME records from your instance and then remove or update the CNAME setting at your DNS provider.

