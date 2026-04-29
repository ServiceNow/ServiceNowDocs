---
title: Configure address suggestion properties
description: Configure the address suggestion system properties so that the Address \(Simple\) field retrieves matching addresses as you enter text.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Address field with auto-suggestions, Reference, Field administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Configure address suggestion properties

Configure the address suggestion system properties so that the Address \(Simple\) field retrieves matching addresses as you enter text.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System properties** &gt; **All properties**.

2.  Search for and select the **glide.ui.address.suggestions.api.host.url** system property.

    1.  In the **Value** field, enter the host URL of the address suggestions API.

        For example, https://places.googleapis.com/v1/places

    2.  Select **Update**.

3.  Search for and select the **glide.ui.address.suggestions.api.host.apikey.encrypted** system property.

    1.  In the **Value** field, enter the API key of the host URL.

    2.  Select **Update**.


## Result

The address suggestions API displays closely matched addresses as you enter text in the Address \(Simple\) field.

