---
title: Address \(Simple\) field type
description: The Address \(Simple\) field type provides real-time address suggestions as you enter text to reduce manual entry errors.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Reference, Field administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Address \(Simple\) field type

The Address \(Simple\) field type provides real-time address suggestions as you enter text to reduce manual entry errors.

You can add the Address \(Simple\) field type to any form in both Core UI and Workspace experiences. When a user enters text in the Address field, closely matched addresses appear for selection. It helps you add accurate addresses without manual entry errors.

The Address \(Simple\) field type uses an external address suggestions API to retrieve matching addresses for suggestion. The following system properties control the API connection:

|Property|Description|
|--------|-----------|
|**glide.ui.address.suggestions.api.host.url**|Specifies the host URL of the third-party address validation API. For example, Google Places API.|
|**glide.ui.address.suggestions.api.host.apikey.encrypted**|Stores the encrypted API key for the third-party address validation API specified in host URL. For example, Google Places API key.|

**Note:** You must configure both system properties so that the Address field can return address suggestions.

## Configuring Address field type

To configure the Address field to a form, complete the following setup:

1.  Add the Address \(Simple\) field to a table to store and display data.

    For more information, see [Add and customize a field in a table](../task/t_CreatingNewFields.md).

2.  Configure the address suggestions API in system properties.

    For more information, see [Configure address suggestion properties](../task/configure-address-suggestion-properties.md).


