---
title: Create a business calendar span using a Script includes
description: You can generate business calendar spans and their names using the Script includes titled BusinessCalendarGeneratorUtil. The calendars you create are accessible across both global and scoped applications.
locale: en-US
release: xanadu
product: Time Configuration
classification: time-configuration
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Creating business calendars, Using time configuration, Time configuration, Configure core features, Administer the ServiceNow AI Platform]
---

# Create a business calendar span using a Script includes

You can generate business calendar spans and their names using the **Script includes** titled **BusinessCalendarGeneratorUtil**. The calendars you create are accessible across both global and scoped applications.

## Before you begin

Role required: admin

## Procedure

1.  Access the **BusinessCalendarGeneratorUtil** script.

    1.  Navigate to **All** and search `Script Includes`.

    2.  Select the `Script Includes` option listed under **System UI**.

    3.  Type `BusinessCalendarGeneratorUtil` in the search bar near the top of the form, and press **enter** or **return** on your keyboard.

    4.  Select `BusinessCalendarGeneratorUtil`.

2.  Set options such as the scope of the script and who can call it \(**Client callable** or **Mobile callable**\), whether it’s **Sandbox enabled**, and the description of the script, at the beginning of the form.

3.  Modify the description of the script as needed.

4.  Enter the necessary values where you see placeholders for `calendarId`, `spanName`, `start`, `end`, `longName`, and `shortName`.

    ![Form the Script includes that it titled, BusinessCalendarGeneratorUtil](../image/BusinessCalendarGeneratorUtilScript.png)

5.  Select **Update** to save changes.


## Result

A business calendar span script includes is created. The year is appended to the beginning of the display name from the `longName` field.

**Parent Topic:**[Creating business calendars](../concept/business-calendars.md)

**Related topics**  


[Script includes](https://www.servicenow.com/docs/access?context=c_ScriptIncludes&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

