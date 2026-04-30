---
title: Script Debugger Scripts - Background support
description: The Scripts - Background module does not support setting breakpoints directly in the script field. You can however, set breakpoints in the script objects called or triggered by the Scripts - Background module.
locale: en-US
release: zurich
product: Scripts
classification: scripts
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Script Debugger, Debugging scripts, Scripting, API implementation, API implementation and reference]
---

# Script Debugger Scripts - Background support

The Scripts - Background module does not support setting breakpoints directly in the script field. You can however, set breakpoints in the script objects called or triggered by the Scripts - Background module.

While running arbitrary JavaScript code in the **Scripts - Background** module, the Script Debugger can only pause scripts when you:

-   Call a script include containing breakpoints.
-   Trigger a business rule containing breakpoints.
-   Trigger a script action containing breakpoints.

**Parent Topic:**[Script Debugger and Session Log](script-debugger.md)

