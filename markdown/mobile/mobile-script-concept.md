---
title: Mobile scripting in offline
description: Use mobile scripts to run reusable JavaScript on the user’s device while offline, so offline buttons and write-back actions stay consistent with online behavior. Mobile scripts are a subset of web scripts, and are stored centrally on the instance. The platform pushes them to mobile devices as part of the offline cache.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/mobile/mobile-script-concept.html
release: australia
topic_type: concept
last_updated: "2026-10-28"
reading_time_minutes: 1
breadcrumb: [Offline mode, Before implementation, Configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Mobile scripting in offline

Use mobile scripts to run reusable JavaScript on the user’s device while offline, so offline buttons and write-back actions stay consistent with online behavior. Mobile scripts are a subset of web scripts, and are stored centrally on the instance. The platform pushes them to mobile devices as part of the offline cache.

Mobile scripts, which is a subset of web scripts, are reusable JavaScript code written to run in ServiceNow mobile apps, including while the device is online. Each script is stored centrally on the instance in the Mobile script \[sys\_sg\_mobile\_script\] table, and the platform pushes it to mobile devices as part of the offline cache. You can call these scripts for mobile components, such as button conditions and write-back actions.

The model is similar to Script Includes, which are reusable server-side JavaScript that you define once and call from any script that needs it. A Script Include runs only when another script explicitly calls it, rather than running automatically in response to a platform event like a record insert. Mobile scripts follow the same reuse pattern, though they run on the device instead of the server.

**Note:** Mobile scripts created before the Brazil release continue to run. We suggest that you update your scripts and use the Brazil version-related syntax. Scripts you don’t update currently function, but ServiceNow doesn’t support any capabilities that stop working.

## Button conditions and write-back actions with mobile scripts

Mobile scripts can be triggered from button conditions and write-back actions, which are the currently supported components. For more information, see [Button condition support enablement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/mobile/button-config-mobile-script.md) and [Write-back action support](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/mobile/wba-mobile-script.md).

## Reference material

: For details about mobile scripts’ supported components, available classes and other API requirements.

-   **[Configuring mobile scripts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/mobile/mobile-scripts-config.md)**  
Learn how to use mobile scripts and to configure within the Mobile script \[sys\_sg\_mobile\_script\] table.
-   **[Components that support mobile scripts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/mobile/components-mobile-scripts.md)**  
Review the components which use mobile scripting.
-   **[Scripting logic for mobile scripts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/mobile/invoking-mobile-scripts.md)**  
Use the Mobile Scripts table \(\[sys\_sg\_mobile\_scripts\]\) to invoke specific records.

**Parent Topic:**[Offline mode](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/mobile/mobile-offline-mode.md)

