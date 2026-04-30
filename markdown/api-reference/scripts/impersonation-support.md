---
title: Script Debugger impersonation support
description: You can use the Script Debugger while impersonating another user, but only if the impersonated user has the script\_debugger role and has read access to the target script.
locale: en-US
release: zurich
product: Scripts
classification: scripts
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Script Debugger, Debugging scripts, Scripting, API implementation, API implementation and reference]
---

# Script Debugger impersonation support

You can use the Script Debugger while impersonating another user, but only if the impersonated user has the script\_debugger role and has read access to the target script.

While impersonating another user, you can:

-   See and change breakpoints that belong to the impersonated user.
-   View and pause on scripts that the impersonated user has read access to.
-   Evaluate expressions in Console on behalf of the impersonated user.

The Script Debugger step-through controls also use the read access of the impersonated user. For example, if the impersonated user does not have read access to a function in the call stack, any **Step into** action instead becomes a **Step over** action.

The impersonated debugging session lasts until:

-   You stop impersonating the user.
-   You log out or the user session ends.
-   You pause the Script Debugger.
-   You close the Script Debugger.

**Parent Topic:**[Script Debugger and Session Log](script-debugger.md)

**Related topics**  


[Script Debugger multiple developer support](multiple-developer-support.md)

