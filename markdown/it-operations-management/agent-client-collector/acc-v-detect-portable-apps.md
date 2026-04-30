---
title: Detecting portable applications using push-based discovery
description: Portable applications are those applications that don’t need to be installed on the target system. Starting in ACC-VC version 2.3.0, push-based Discovery can detect portable applications, such as Firefox, VLC, Notepad++ etc, for Windows only.
locale: en-US
release: yokohama
product: Agent Client Collector
classification: agent-client-collector
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
keywords: [Agent Client Collector, Agent Client Collector for Visibility, ACC for Visibility]
breadcrumb: [Using Agent Client Collector for Visibility - Content, Agent Client Collector for Visibility - Content, Agent Client Collector, IT Operations Management]
---

# Detecting portable applications using push-based discovery

Portable applications are those applications that don’t need to be installed on the target system. Starting in ACC-VC version 2.3.0, push-based Discovery can detect portable applications, such as Firefox, VLC, Notepad++ etc, for Windows only.

**Note:** Only portable applications listed in [https://portableapps.com/](https://portableapps.com/) are supported.

When the portable application is executed, it creates a running process. The application creates a path similar to the following for the configuration file 'appinfo.ini':

```
-\ <--- Directory with FirefoxPortable.exe 
 +\App 
 +\firefox 
 +\Data 
 +\profile 
 +\settings 
 +\plugins\ (optional) 
```

**Note:** ServiceNow users must have Local account access to get the data in order to read appinfo.ini file.

Name, Version, and Vendor attributes are fetched from the Portable software and are found in the appinfo.ini files. appinfo.ini is the mandatory file to execute any portable application. If SAM is installed, the information is displayed in Software installation \[cmdb\_sam\_sw\_install\] table. If SAM is not installed, the information shows in the Software instance \[cmdb\_software\_instance\] table.

**Parent Topic:**[Using Agent Client Collector for Visibility - Content](acc-v-using-agent-client-collector-for-visibility.md)

