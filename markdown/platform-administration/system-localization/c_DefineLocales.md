---
title: Configuring locales
description: Specify a locale for an instance so information such as dates, times, and currencies display properly based on your location.Set the instance locale using a locale code.
locale: en-US
release: yokohama
product: System Localization
classification: system-localization
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring System Localization, System Localization, Translation and localization, Configure core features, Administer the ServiceNow AI Platform]
---

# Configuring locales

Specify a locale for an instance so information such as dates, times, and currencies display properly based on your location.

By default, the base system uses US standard formatting. For example, the currency default is the US dollar sign \($\) displayed with two decimal places: $100.00. By customizing your locale, you can make things such as currency appear as you expect. For example, in France, you may want to see 100,00 € instead of $100.00.

## Set the instance locale

Set the instance locale using a locale code.

### Before you begin

Role required: admin

### About this task

You should set the instance locale before a system has gone into production and not change it after it goes into production. If a user's locale must be changed, update the **Country code** field on the user record.

**Important:** The value of this property determines the system's default currency, or reference currency, into which all prices are automatically converted before other sums or conversions are performed. Changing this property after any price or currency fields have been given a value \(for Service Catalog items, Assets, Project Tasks, etc.\) may result in improper conversion or prices that sum incorrectly.

### Procedure

1.  Navigate to **All** &gt; **System Properties** &gt; **System Localization**.

2.  Enter the locale code to use under **Locale code to use for localization**.

    Format is \[language code\].\[country code\] \(e.g. en.GB for Britain fr.FR for France, de.DE for Germany, or ja.JP for Japan\).

    |Country|Locale code|
    |-------|-----------|
    |United States|en.US|
    |Great Britain|en.GB|
    |France|fr.FR|
    |Germany|de.DE|
    |Japan|ja.JP|

3.  Select **Save**.


