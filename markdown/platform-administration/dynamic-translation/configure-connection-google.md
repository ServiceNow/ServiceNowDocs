---
title: Configure the connection attributes for the GoogleTranslation alias
description: Connect to the Google's translation service by configuring the Google connection. Provide information that is used by HTTP\(s\) actions or activities to connect to that service.
locale: en-US
release: australia
product: Dynamic Translation
classification: dynamic-translation
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Set up the Google Cloud Translator Service spoke, Google Cloud Translator Service Spoke, Integration with other translation services, Dynamic Translation, Translation and localization, Configure core features, Administer the ServiceNow AI Platform]
---

# Configure the connection attributes for the GoogleTranslation alias

Connect to the Google's translation service by configuring the Google connection. Provide information that is used by HTTP\(s\) actions or activities to connect to that service.

## Before you begin

Role required: connection\_admin

## Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Connections**.

2.  Open for the record for **Google**.

3.  In the Attributes related list of the HTTP\(S\) Connection form, fill in the fields.

<table id="table_any_shp_gfb"><thead><tr><th>

Field

</th><th>

Value required

</th></tr></thead><tbody><tr><td>

location

</td><td>

Location of the customer. If the value is not specified when creating an account on Google Cloud, then specify `global`.

</td></tr><tr><td>

project\_id

</td><td>

Identifier of a project. Specify the **project\_id** value from the JSON file.

</td></tr><tr><td>

version

</td><td>

API version that the related spokes are built for. The default value is `v3beta1`.Because Google now supports the v3 version, you can override this value as `v3`.

</td></tr></tbody>
</table>4.  Right-click the form header and click **Save**.


**Parent Topic:**[Set up the Google Cloud Translator Service spoke](setup-google-translator.md)

**Previous topic:**[Configure the credential for the GoogleTranslation alias](configure-credential-google.md)

**Next topic:**[Microsoft Azure Translator Service spoke](../../dynamic-translation/concept/microsoft-translation-spoke.md)

