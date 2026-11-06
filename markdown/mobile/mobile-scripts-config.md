---
title: Configuring mobile scripts
description: Learn how to use mobile scripts and to configure within the Mobile script \[sys\_sg\_mobile\_script\] table.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/mobile/mobile-scripts-config.html
release: australia
topic_type: task
last_updated: "2026-10-28"
reading_time_minutes: 1
breadcrumb: [Mobile scripting in offline, Offline mode, Before implementation, Configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Configuring mobile scripts

Learn how to use mobile scripts and to configure within the Mobile script \[sys\_sg\_mobile\_script\] table.

## Before you begin

Role required: mobile\_admin

**Note:** To enable mobile scripting for button conditions, you must enable the option in the button table. For more information, see [Button condition support enablement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/mobile/button-config-mobile-script.md)

.

## Procedure

1.  Navigate to **All** &gt; **sys\_sg\_mobile\_script.list**.

    The Mobile script list displays.

2.  Select **New** to create a mobile script record.

3.  On the form, fill in the required fields.

    |Field|Description|
    |-----|-----------|
    |Name|Unique name of the mobile script, used as the display field. This name is the class name, so it can use only letters, numbers, and underscores, and it can’t start with a number.|
    |API Name|A read-only, automatically generated name. The API name combines the scope and the name, separated by a period \(for example, global.my\_script\). If no scope is set, the scope defaults to global.|
    |Description|Free-form description of the mobile script you’re creating.|
    |Active|Define whether this mobile script should be active not. The default value is &lt;true&gt;.|
    |Script|The JavaScript source executed on the device. For script examples, see .|
    |Script dependencies|A read-only automatically generated list of the API names this script calls. It lists the API names this script calls, and any other scripts that are downloaded for this script to work end to end.|

4.  In the **Name** field, add a unique name for the Mobile script.

5.  Select **Turn on ECMAScript 2021 \(ES12\) mode** if you want to use ES2021 syntax and feature.

6.  Select **Submit**.


**Parent Topic:**[Mobile scripting in offline](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/mobile/mobile-script-concept.md)

