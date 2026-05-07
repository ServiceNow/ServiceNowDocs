---
title: The calendar display component
description: Use the calendar display component in CPQ to present time-based configuration options in a monthly view. Configure sets, fields, and selection settings to let users view, select, and manage date-specific records directly in the configuration interface.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [CPQ app, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# The calendar display component

Use the calendar display component in CPQ to present time-based configuration options in a monthly view. Configure sets, fields, and selection settings to let users view, select, and manage date-specific records directly in the configuration interface.

CPQ native UI allows the administrator to present a calendar display component to the user to aid in time-based configurations. The calendar displays in the context of a month. The data underlying the calendar display is a set, with each calendar day represented by one record in the set.

The example below shows a set with 30 records, one for each day, represented as a calendar display component.

![Calendar interface](../images/cpq-layout-calendar-display.png)

Key elements that support this example include a set with the variable name `availableDates`. This set contains the following associated fields:

-   `selectedDate` \(Boolean\): captures whether the user has selected one or more date/records
-   `rawDate` \(Text\): holds the raw date formatted for each set record
-   `availableDate` \(Text\); holds the date in "MM/DD/YYYY" format for each set record. This is used to facilitate the human-readable date on the calendar display
-   `loadSize` \(Picklist\): Options include S, M, and L. This picklist is displayed in each record \(each day on the monthly calendar\).

    Calendar records \(days\) can display any number of set-associated fields. The administrator should apply a practical limit to the number of fields defined, based on users' screen sizes and responsiveness provided by the application.


The On Configure/Reconfigure enrichment initializes the set with the appropriate size for the months to be displayed and a JSON element that contains field values for each record. The following is the output of the On Configure enrichment for the raw calendar above:

```
{
	"availableDates": {
			"data": [
			{
				"availableDate": { "value": "6/1/2024" },
				"rawDate": {
				"value": "2024-06-01T00:00:00.000Z"
				}
			}, //skipped interior records for brevity
			{
				"availableDate": { "value": "6/30/2024" },
				"rawDate": {
				"value": "2024-06-30T00:00:00.000Z"
				}
			}
		],
		"userEdited": false
	}
}
```

Note that the loadSize field was left out of the set JSON because the administrator did not want to prepopulate the field.

In the blueprint layout, the administrator defines where the set will be displayed and the subfields that will be displayed in each record/calendar day.

![Calendar demo](../images/cpq-layout-calendar-display-blueprint-layout.png)

In the Set Properties &gt; Selection Settings, the Admin defines whether the user should be allowed to select one or multiple days. The Boolean field for selection \(in this case, selectedDate\) stores whether a specific set record/calendar day is selected.

![Selectionsettings](../images/cpq-layout-calendar-display-selection-settings.png)

The Set Properties &gt; Search Settings help you display the most relevant subset of days for the user when your calendar lets the user select from more than one month. For this purpose, Source Field is the day \(record\) that the Admin wishes to feature in the monthly calendar set. Target Field is the set-associated field that contains the full range of calendar dates.

![Search settings](../images/cpq-layout-calendar-display-search-settings.png)

The Set Properties &gt; Raw Value area contains the JSON output by the selections on the page above. However, as "calendar" is not currently selectable as a displayType, the administrator must edit the JSON to define it explicitly.

![Raw value code](../images/cpq-layout-calendar-display-raw-value.png)

