---
title: Configure a territory phone display rule
description: The string of numbers that make up a phone number is automatically validated and formatted for a specific territory by applying a series of regular expressions.Phone validations are already configured for all territories and are automatically applied to the phone number to ensure that the number is valid for the territory.Phone formats are already configured for all territories and are automatically applied to the phone number to ensure that the number is valid for the territory.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Phone number field type, Reference, Field administration, Forms, fields, and lists, Configure core features, Administer]
---

# Configure a territory phone display rule

The string of numbers that make up a phone number is automatically validated and formatted for a specific territory by applying a series of regular expressions.

## Before you begin

Role required: admin

## About this task

The number is first validated against the phone validations that have been defined for the territory, and in the order specified by the **Order** field. To be valid, the number must match the regular expression defined in the **Condition** field for at least one phone validation.

After a number has been validated, the **Condition** expression for each format defined for the territory is applied to the number in the order determined by the **Order** fields. The **Pattern** and **Format** regular expressions are applied to produce a phone number that is formatted correctly for the territory.

The Sys Phone Territory screen allows administrators to edit the display rules for a given territory. Administrators may want to modify the **Active**, **Display**, or **Order** fields. To edit the display rules for a territory:

## Procedure

1.  Navigate to **All** &gt; **System Policy** &gt; **Rules** &gt; **Telephone Display Rules**.

2.  Click a territory **Name**.

3.  Edit the fields, as appropriate \(see table\).

4.  Click **Update**.

    |Field|Description|
    |-----|-----------|
    |Name|The unique name of the territory.|
    |Country calling code|The [country code](http://countrycode.org/) for dialing numbers from outside the territory.|
    |International direct dial|The prefix for calling internationally from the territory, such as 00 or 001.|
    |STD|The subscriber trunk dialing code, also know as the direct distance dialing code, which is a sequence of numbers before the telephone number that indicate whether the call is to be routed outside of the local calling area.|
    |International prefix|The prefix required to dial an international call, such as a plus sign \(+\).|
    |National prefix|The prefix required to dial a local call.|
    |Active|An indicator for whether the territory phone definition is active. If deactivated, this territory unavailable to users.|
    |Trunk dialing code optional|An indicator for whether the STD code is optional.|
    |STD follows country|An indicator for whether the STD code should be displayed to the right of the country calling code.|
    |Display|An indicator for whether to display the territory in the choice list. Clearing this check box removes the territory from the choice list. If an international number is entered for a territory that is not displayed in the territory selector choice list, that territory is temporarily added to the selector choice list for that field only. For example, If the United Kingdom **Display** field is not selected, the United Kingdom does not appear in the territory selector choice list. However, if the user enters an international number beginning with +44, the United Kingdom is added to the list and the number is formatted and validated accordingly.|
    |Order|The order in which a territory appears in a choice list. Territories are sorted numerically by the number assigned here. If more than one territory is assigned the same number, they are subsorted alphabetically. All territories are assigned a default value of 100. To display a territory at the top of the list, assign a value that is less than 100. To display a territory at the end of the list, assign a value that is greater than 100. For example, if a territory is assigned an order of 500, it is displayed at the end of the list, and if more than one territory is assigned an order of 500, they are listed alphabetically at the end of the list.|


## Phone validations

Phone validations are already configured for all territories and are automatically applied to the phone number to ensure that the number is valid for the territory.

## Phone formats

Phone formats are already configured for all territories and are automatically applied to the phone number to ensure that the number is valid for the territory.

