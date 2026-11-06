---
title: Scripting logic for mobile scripts
description: Use the Mobile Scripts table \(\[sys\_sg\_mobile\_scripts\]\) to invoke specific records.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/mobile/invoking-mobile-scripts.html
release: australia
topic_type: reference
last_updated: "2026-11-02"
reading_time_minutes: 1
breadcrumb: [Mobile scripting in offline, Offline mode, Before implementation, Configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Scripting logic for mobile scripts

Use the Mobile Scripts table \(\[sys\_sg\_mobile\_scripts\]\) to invoke specific records.

Learn how to call the logic in a mobile script from another script. To do this, first create an instance of the mobile script by its script name. If the class has a constructor, pass in the required arguments. Then call the method you need, passing in the current record.

Scripts can be standalone or can call other scripts. To call another script, see the usage examples in the Supported syntax for the Script field section of the .

Fore more information about the mobile script table and where to add your scripts, see [Configuring mobile scripts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/mobile/mobile-scripts-config.md).

The mobile script syntax can be used with the following elements:

-   Button conditions
-   Write-back actions
-   An internal call from Script A to Script B, where both scripts are defined in the Script field of the Mobile Scripts table.

**Parent Topic:**[Mobile scripting in offline](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/mobile/mobile-script-concept.md)

