---
title: Disable MultiSSO Debugging \[Updated in Security Center 1.3 and 1.5\]
description: The glide.authenticate.multisso.debug property controls debug logging for Multi-SSO.
locale: en-US
release: yokohama
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-01-30"
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
|Category|[Configuration](sc-configuration.md)|
|Purpose|Disables Multi-SSO debug.|
|Recommended value|false|
|Default value|false|
|Configuration type|Boolean|
|Security risk|\(High\) Set the property to the recommended value of "False", otherwise, MultiSSO debug is enabled which could lead to unintended sensitive information leak.|
|Security risk rating|4.0|
|References|[Multi-Provider SSO properties, tables, and scripts](../../../integrate/single-sign-on/reference/r_InstalledWithMultiProviderSSO.md)|

To learn more about adding or creating a system property, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=yokohama&pubname=yokohama-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

**Parent Topic:**[Configuration](sc-configuration.md)

