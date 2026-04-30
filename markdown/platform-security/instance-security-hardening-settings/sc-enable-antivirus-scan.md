---
title: Enable antivirus scan
description: The com.glide.snap.enable\_scan property activates the antivirus scan functionality.
locale: en-US
release: xanadu
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [File and resources, Hardening settings, Platform Security]
---

# Enable antivirus scan

The **com.glide.snap.enable\_scan** property activates the antivirus scan functionality.

Set **com.glide.snap.enable\_scan** to the recommended value of **true** to enable antivirus scanning.

**Warning:** This is a safe harbor property, meaning the value can't be altered once it's changed. It is non-revertible.

## More information

|Attribute|Description|
|---------|-----------|
|Property name|**com.glide.snap.enable\_scan**|
|Configuration type|System Properties \(/sys\_properties\_list.do\)|
|Category|[File and resources](sc-file-resources.md)|
|Purpose|To enable or disable antivirus scanning on the specific instance.|
|Recommended value|true|
|Default value|true|
|Data type|boolean|
|Security risk|\(High\) Antivirus scanning helps protect your instance against virus infections that can be introduced by file attachments to your system records, such as incidents, problems, and stories.|
|Security risk rating|7.7|

**Parent Topic:**[File and resources](sc-file-resources.md)

