---
title: Signing Tool arguments
description: Learn about the available arguments for the Signing Tool.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Standalone signing tool, Using Code Signing, Code Signing, Platform Security]
---

# Signing Tool arguments

Learn about the available arguments for the Signing Tool.

|Argument|Required|Description|
|--------|--------|-----------|
|-d|Yes|Root directory of project to sign. Should contain project directory \(random 32 alphanumeric\), sn\_source\_control.properties file, and a &lt;project\_name&gt;.iml file|
|-f|Yes|The file path of the keystore.|
|-a|No|Alias used to access a specific entry within the keystore.|
|-c|No|Concatenate record signatures into one file.|
|-k|No|Password to access the key stored within the keystore. You can also enter this password when prompted instead of within the argument.|
|-o|No|Sign with a new certificate in place of any existing sys\_cert files.|
|-p|No|Password to access the keystore if it has a password. You can also enter this password when prompted instead of within the argument.|
|-w|No|Wipe all existing signature record files.|
|-h|No|Show this help message and exit.|

**Parent Topic:**[Standalone signing tool](../concept/sa-code-signing-tool.md)

