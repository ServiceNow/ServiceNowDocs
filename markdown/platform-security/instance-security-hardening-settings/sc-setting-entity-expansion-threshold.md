---
title: Minimize Entity Expansion Threshold for GlideXMLUtil Scriptable \[Updated in Security Center 1.3, 1.5, and 2.0\]
description: Use the glide.xmlutil.max\_entity\_expansion property to change the maximum entity expansion limit to a smaller number.
locale: en-US
release: yokohama
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Validation, sanitization, and encoding, Hardening settings, Platform Security]
---

# Minimize Entity Expansion Threshold for GlideXMLUtil Scriptable \[Updated in Security Center 1.3, 1.5, and 2.0\]

Use the **glide.xmlutil.max\_entity\_expansion** property to change the maximum entity expansion limit to a smaller number.

This property controls the maximum amount of entity expansion within an XML Parser. If **glide.xmlutil.max\_entity\_expansion** is not set to the recommended value of 3000 or less, then the GlideXMLUtil parsing scriptable may be vulnerable to denial of service attacks.

Ensure the property **glide.xmlutil.max\_entity\_expansion** is set to 3000 or less. If the instance is on Washington or later, the default implied value is 3000 if the sys\_properties record does not exist. If the instance is not on Washington or later, the recommendaiton is for the instance admin to create a sys\_properties record with name **glide.xmlutil.max\_entity\_expansion** and the value 3000.

**Note:** 500 is the default minimum imposed by the ServiceNow AI Platform, which is considered to be a safe threshold.

## More information

|Attribute|Description|
|---------|-----------|
|Property name|**glide.xmlutil.max\_entity\_expansion**|
|Configuration type|System Properties \(/sys\_properties\_list.do\)|
|Category|[Validation, sanitization, and encoding](validation-sanitization-encoding.md)|
|Purpose|This remediation control must be enabled to defend against XML Entity Expansion/Billion Laugh attack.|
|Recommended value|3000|
|Default value|100000|
|Security risk rating|5.3|
|Functional Impact|If the customization is using large entity expansion, then, the ServiceNow AI Platform might block further processing.|
|Security risk|\(Moderate\) An attacker can use this vulnerability to expand data exponentially, quickly consuming all system resources.|

To learn more about adding or creating a system property, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=yokohama&pubname=yokohama-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

**Parent Topic:**[Validation, sanitization, and encoding](validation-sanitization-encoding.md)

