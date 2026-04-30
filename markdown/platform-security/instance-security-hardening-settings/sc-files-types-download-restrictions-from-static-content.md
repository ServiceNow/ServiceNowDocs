---
title: Restrict downloadable files types in static content \[Updated in Security Center 1.3\]
description: Use the glide.ui.strict\_customer\_uploaded\_static\_content property to enable restrictions on the file types that can be downloaded when they have been uploaded using the Upload File functionality.
locale: en-US
release: xanadu
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [File and resources, Hardening settings, Platform Security]
---

# Restrict downloadable files types in static content \[Updated in Security Center 1.3\]

Use the **glide.ui.strict\_customer\_uploaded\_static\_content** property to enable restrictions on the file types that can be downloaded when they have been uploaded using the Upload File functionality.

You use this property with the **glide.ui.strict\_customer\_uploaded\_content\_types** property, which creates a comma-delimited list of restricted downloadable file types. To learn more, see Downloadable file types.

**Warning:** The value for this property is a no DB override. It can't be altered or overridden.

## More information

|Attribute|Description|
|---------|-----------|
|Property name|**glide.ui.strict\_customer\_uploaded\_static\_content**|
|Configuration type|System Properties \(/sys\_properties\_list.do\)|
|Category|[File and resources](sc-file-resources.md)|
|Purpose|To ensure that safe file types are permitted to be downloaded from the application.|
|Recommended value|true|
|Default value|true|
|Security risk rating|3.1|
|Functional impact|This remediation enforces restriction of file downloads based on the values specified in the **glide.ui.strict\_customer\_uploaded\_content\_types** property. To learn more, see Downloadable file types.|
|Security risk|\(Low\) File download restrictions should be applied to any untrusted user input sources.|

**Parent Topic:**[File and resources](sc-file-resources.md)

