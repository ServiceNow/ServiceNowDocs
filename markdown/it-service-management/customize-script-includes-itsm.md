---
title: Script includes and customization
description: Many Script Includes are provided by default with the ITSM products. You can call existing script includes from a script or create your own script includes.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [IT Service Management]
---

# Script includes and customization

Many Script Includes are provided by default with the ITSM products. You can call existing script includes from a script or create your own script includes.

You can find script includes by navigating to **Self Service** &gt; **System Definition** or **Self Service** &gt; **System UI**. To get the latest features and problem fixes without breaking the existing functionality during an upgrade, remember the following points:

To modify or customize an existing script include:

-   Do not use the script includes that are suffixed by SNC. Those script includes are read-only and must not be customized. For example, the following script include must not be customized.

    ```
    var ChangeProcessSNC = Class.create();
    ChangeProcessSNC.prototype = {
        // SNC functions
        type: "
    ```

-   Do not override methods that start with an underscore. Those methods indicate that the functions are private.

You can override the functions of the non-SNC script includes that extend the SNC scripts. For example, the following script include can be overridden.

```
var ChangeProcess = Class.create(); 
ChangeProcess.prototype = Object.extendsObject(ChangeProcessSNC, 
{  // Customer overridden functions  type: "ChangeProcess" });
```

