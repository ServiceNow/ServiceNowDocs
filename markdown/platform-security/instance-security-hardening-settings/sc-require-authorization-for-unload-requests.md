---
title: Require authorization for unload requests \[Updated in Security Center 1.3\]
description: Use the glide.basicauth.required.unl \(useUnloadFormat\) property to designate if incoming unload requests should require basic authentication.
locale: en-US
release: xanadu
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [API and web service, Hardening settings, Platform Security]
---

# Require authorization for unload requests \[Updated in Security Center 1.3\]

Use the **glide.basicauth.required.unl** \(useUnloadFormat\) property to designate if incoming unload requests should require basic authentication.

## More information

|Attribute|Description|
|---------|-----------|
|Property name|**glide.basicauth.required.unl**|
|Configuration type|System Properties \(/sys\_properties\_list.do\)|
|Category|[API and web service](sc-api-web-service.md)|
|Purpose|To enforce basic authentication on unload requests.|
|Recommended value|true|
|Security risk rating|7.5|
|Functional Impact|This remediation enforces a combination of authentication methods, in the form of basic authentication and system level access control. It performs this authentication while retrieving data from tables/pages in the form of unload data on the instance.|
|Security risk|\(High\) Without appropriate authorization configured on the datasource unload requests, an unauthorized user can get access to sensitive content/data on the target instance. Ensure that **glide.basicauth.required.unl** exists in the sys\_properties\_table and is set to true.|
|References|[Authentication](../../../integrate/single-sign-on/concept/c_Authentication.md)|

**Parent Topic:**[API and web service](sc-api-web-service.md)

