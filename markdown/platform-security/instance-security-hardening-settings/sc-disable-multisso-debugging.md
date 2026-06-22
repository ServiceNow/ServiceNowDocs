---
title: Disable MultiSSO Debugging \[Updated in Security Center 1.3 and 1.5\]
description: The glide.authenticate.multisso.debug property controls debug logging for Multi-SSO.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-security/instance-security-hardening-settings/sc-disable-multisso-debugging.html
release: zurich
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configuration, Hardening settings, Platform Security]
---

# Disable MultiSSO Debugging \[Updated in Security Center 1.3 and 1.5\]

The **glide.authenticate.multisso.debug** property controls debug logging for Multi-SSO.

## More information

|Attribute|Description|
|---------|-----------|
|Property name|**glide.authenticate.multisso.debug**|
|Configuration type|System Properties \(/sys\_properties\_list.do\)|
|Category|[Configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/instance-security-hardening-settings/sc-configuration.md)|
|Purpose|Disables Multi-SSO debug.|
|Recommended value|false|
|Default value|false|
|Configuration type|Boolean|
|Security risk|\(High\) Set the property to the recommended value of "False", otherwise, MultiSSO debug is enabled which could lead to unintended sensitive information leak.|
|Security risk rating|4.0|
|References|[Multi-Provider SSO properties, tables, and scripts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/authentication/r_InstalledWithMultiProviderSSO.md)|

To learn more about adding or creating a system property, see [Add a system property](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/ai-platform-administration/t_AddAPropertyUsingSysPropsList.md).

**Parent Topic:**[Configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/instance-security-hardening-settings/sc-configuration.md)

