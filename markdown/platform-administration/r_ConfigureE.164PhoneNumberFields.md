---
title: E.164 phone number field configuration
description: Administrators can use the phone number system properties and dictionary attributes to do certain things.By default, phone number fields require that a phone number match the display format of the selected territory.By default, users can enter phone numbers in their territory's local format and do not have to format the number for international dialing.By default, an E.164 phone number field always displays phone numbers in an international format.A property controls how territory labels are displayed.A property is available to control the display of prefixes.By default, an E.164 phone number field always displays the phone territory that is associated with the phone number.Several properties are available to configure E.164 phone number fields.You can override the global system property with certain dictionary attributes.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 11
breadcrumb: [Phone number field type, Field types reference, Field administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# E.164 phone number field configuration

Administrators can use the phone number system properties and dictionary attributes to do certain things.

The system properties apply the configuration option to all phone number fields that do not have a comparable dictionary attribute. The dictionary attributes apply the configuration only to the phone number field it is added to. Since dictionary attributes take precedence over system properties, administrators can set a global configuration with a property and then apply exceptions on a field-by-field basis.

**Note:** Alpha numeric characters are not allowed and is not considered as a valid phone number.

## Requiring territory format validation

By default, phone number fields require that a phone number match the display format of the selected territory.

By default, phone number fields require that a phone number match the display format of the selected territory. If a phone number does not match this format, the input box displays a red line underneath the phone number or the whole box turns red, and users are prevented from saving it.

![](../image/PhoneE164Strict.png "Phone e164 strict")

Setting the **glide.phone\_number\_e164.strict** system property to **false** or adding the **pn\_strict** dictionary attribute allows the phone number input box to display a green line underneath numbers that do not match the territory format listed for the selected territory or the whole box turns green. You can use the **Other / Unknown** territory to store otherwise invalid phone numbers.

![](../image/PhoneE164NoStrict.png "Phone e164 not strict")

**Warning:** Switching from optional territory format validation to required territory format validation may result in some phone numbers failing validation altogether. In such cases, the E.164 phone number field displays an error message.

## Requiring entry of international format

By default, users can enter phone numbers in their territory's local format and do not have to format the number for international dialing.

The phone number field automatically formats local phone numbers into E.164-compliant international phone numbers when the user finishes editing the field. As long as the phone number entered matches the territory's format for a local number, users can save the phone number.

![](../image/PhoneE164EntryLocal.png "Phone e164 entry local")

![](../image/PhoneE164DisplayInternational.png "Phone e164 display international")

Changing the **glide.phone\_number\_e164.allow\_national\_entry** system property or adding the **pn\_allow\_national\_entry** dictionary attribute requires users to enter a phone number in the territory's international format, which starts with the plus \(+\) character. Users cannot save a locally formatted phone number, and the phone number input box displays a red line underneath phone numbers without the proper international formatting.

## Configure the display of the local format

By default, an E.164 phone number field always displays phone numbers in an international format.

![North American phone number displaying in local format.](../image/PhoneE164DisplayInternational.png "Phone e164 display international")

Change the E.164 phone number to use the local format in certain circumstances by [adding the following system property](../../reference-pages/reference/r_AvailableSystemProperties.md#):

<table id="simpletable_xsy_m3x_vz"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**glide.phone\_number\_e164.display\_national**

</td><td>

-   **Type**: string
-   **Default value**: false
-   **Other possible values**:
    -   **true or form**: Displays phone numbers in a local format on forms, but displays an international format on lists.
    -   **all**: Always displays phone numbers in a local format.
    -   **user**: Only displays phone numbers in a local format when the phone number matches the local setting of the current user.
    -   **false**: Does not display phone numbers in local format.

</td></tr></tbody>
</table>Select one of the possible values to determine how the system handles the E.164 phone number.

You can also [add the following dictionary attribute](../../data-dictionary-tables/task/t_ModifyADictionaryEntryFromAForm.md) to a specific field to override the system property:

<table id="simpletable_nn2_x3x_vz"><thead><tr><th>

Dictionary attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**pn\_display\_national**

</td><td>

Overrides the **glide.phone\_number\_e164.display\_national** property setting for how an E.164 phone number field displays phone numbers. Available values are identical to those described for the **glide.phone\_number\_e164.display\_national** property.-   Type: string
-   Default value: false
-   Example:pn\_display\_national=all

</td></tr></tbody>
</table>## Configure the display of territory labels

A property controls how territory labels are displayed.

You can display territory labels next to the number in an E.164 phone number field by setting the system property or adding the dictionary attribute. This display is useful if the territory selector choice list is turned off and you want the user to see the territory for the entered phone number.

![Phone display with the phone number +44 01733 753363 and the territory label United Kingdom.](../image/E164PhoneDisplayTerritoryLabels.png "E164 phone display territory labels")

Enabling territory labels also displays the phone territory in lists.

[Add the following system property](../../reference-pages/reference/r_AvailableSystemProperties.md#) to display the territory label next to the number in an E.164 phone number.

<table id="simpletable_xsy_m3x_vz"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**glide.phone\_number\_e164.display\_territory\_text**

</td><td>

Determines when an E.164 phone number field displays a territory label.-   **__Type__**: string
-   **Default value**: read-only
-   **Other possible values**:
    -   **all**: Displays the territory label.
    -   **national**: Displays the territory label only if the phone number is in local format.
    -   **read-only**: Displays the territory label in read-only mode, regardless of whether the number is in local or international format.
    -   **read-only-national**: Displays the territory label in read-only mode only if the number is in local format.
    -   **list**: Displays the territory label in a list.
    -   **list-national**: Displays the territory label in a list if the number is in national format.
    -   **none**: Does not display the territory label.

</td></tr></tbody>
</table>You can also [add the following dictionary attribute](../../data-dictionary-tables/task/t_ModifyADictionaryEntryFromAForm.md) to a specific field to override the system property:

<table id="simpletable_nn2_x3x_vz"><thead><tr><th>

Dictionary attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**pn\_display\_territory\_text**

</td><td>

Overrides the **glide.phone\_number\_e164.display\_territory\_text** property that defines when a phone number field displays a territory label. Available values are identical to those described previously for the **glide.phone\_number\_e164.display\_territory\_text** property.-   Type: string
-   Default value: read-only
-   Example:pn\_display\_territory\_text=all

</td></tr></tbody>
</table>## Configure the international direct dialing prefixes

A property is available to control the display of prefixes.

You can enable the display of the international direct dialing prefix, which appears between the territory selector choice list and the input box for an E.164 phone number field on forms, by setting the system property or adding the dictionary attribute.

![Phone display with the international direct dialing prefix before the phone number field](../image/E164PhoneDisplayIdd.png "E164 phone display idd")

[Add the following system property](../../reference-pages/reference/r_AvailableSystemProperties.md#) to display the international direct dialing prefix.

<table id="simpletable_xsy_m3x_vz"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**glide.phone\_number\_e164.display\_users\_idd**

</td><td>

Determines whether to display the international direct dialing prefix between the territory selector choice list and the input box on forms.-   Type: true \| false
-   Default value: false

</td></tr></tbody>
</table>You can also [add the following dictionary attribute](../../data-dictionary-tables/task/t_ModifyADictionaryEntryFromAForm.md) to a specific field to override the system property:

<table id="simpletable_nn2_x3x_vz"><thead><tr><th>

Dictionary attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**pn\_display\_users\_idd**

</td><td>

Overrides the **glide.phone\_number\_e164.display\_users\_idd** property that determines whether to display the international direct dialing prefix between the territory selector choice list and the input box on forms. Available values are identical to those described above for the **glide.phone\_number\_e164.display\_users\_idd** property.-   Type: true \| false
-   Default value: false
-   Example:pn\_display\_users\_idd=false

</td></tr></tbody>
</table>### Configure the phone territory selector choice list

By default, an E.164 phone number field always displays the phone territory that is associated with the phone number.

Changing the system property or adding the dictionary attribute hides the territory selector choice list. If the territory selector choice list is hidden, users can only enter a local or national number.

![Number field with no selector displayed.](../image/PhoneE164HideSelector.png "Phone e164 hide selector")

[Add the following system property](../../reference-pages/reference/r_AvailableSystemProperties.md#) to show or hide the territory selector choice list.

<table id="simpletable_xsy_m3x_vz"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**glide.phone\_number\_e164.display\_territory\_selector**

</td><td>

Determines whether to display the territory selector choice list. Hiding the territory selector choice list restricts users to entering only local or national phone numbers.-   Type: true \| false
-   Default value: true

</td></tr></tbody>
</table>You can also [add the following dictionary attribute](../../data-dictionary-tables/task/t_ModifyADictionaryEntryFromAForm.md) to a specific field to override the system property:

<table id="simpletable_nn2_x3x_vz"><thead><tr><th>

Dictionary attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**pn\_display\_territory\_selector**

</td><td>

Overrides the **glide.phone\_number\_e164.display\_territory\_selector** property setting that determines whether to display the territory selector choice list. Available values are identical to those described above for the **glide.phone\_number\_e164.display\_territory\_selector** property.-   Type: true \| false
-   Default value: true
-   Example: pn\_display\_territory\_selector=false

</td></tr></tbody>
</table>## E.164 phone number field system properties

Several properties are available to configure E.164 phone number fields.

**Note:** To open the System Properties \[sys\_properties\] table, enter `sys_properties.list` in the navigation filter.

<table id="table_jlx_ny3_3r"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

glide.phone\_number\_e164.strict

</td><td>

Determines whether all phone number fields must match the display format for the selected territory. When the value is **true**, the phone number input field displays a red line underneath the phone numbers that do not match the format for the selected territory. Users cannot save the phone number.

 When the value is **false**, the phone number input field displays a green line underneath phone numbers that do not match the format for the selected territory. Users can save the phone number. The territory selector choice list offers the option to select an **Other / Unknown** territory format.

 -   Type: true \| false
-   Default value: true
-   Location: [Add](../../reference-pages/reference/r_AvailableSystemProperties.md#) to the System Properties \[sys\_properties\] table.

</td></tr><tr><td>

glide.phone\_number\_e164.allow\_national\_entry

</td><td>

Determines whether users can enter phone numbers in the local format or whether they must enter phone numbers in international format. When **true**, users can enter phone numbers in the local format for the selected territory. When **false**, users must enter phone numbers in the international format for the selected territory.

 -   Type: true \| false
-   Default value: true
-   Location: [Add](../../reference-pages/reference/r_AvailableSystemProperties.md#) to the System Properties \[sys\_properties\] table.

</td></tr><tr><td>

glide.phone\_number\_e164.display\_national

</td><td>

Determines whether to display E.164 phone numbers in local format.-   Type: string
-   Default value: false
-   Other possible values:
    -   **true or form**: Displays phone numbers in a local format on forms, but displays an international format on lists.
    -   **all**: Always displays phone numbers in a local format.
    -   **user**: Only displays phone numbers in a local format when the phone number matches the local setting of the current user. The local setting of the current user is determined by the location associated with the [user record](../../users-and-groups/task/t_CreateAUser.md).
    -   **false**: Does not display phone numbers in local format.
-   Location: [Add](../../reference-pages/reference/r_AvailableSystemProperties.md#) to the System Properties \[sys\_properties\] table.

</td></tr><tr><td>

glide.phone\_number\_e164.display\_territory\_selector

</td><td>

Determines whether to display the territory selector choice list. Hiding the territory selector choice list restricts users to entering only local or national phone numbers.-   Type: true \| false
-   Default value: true
-   Location: [Add](../../reference-pages/reference/r_AvailableSystemProperties.md#) to the System Properties \[sys\_properties\] table.

</td></tr><tr><td>

glide.phone\_number\_e164.display\_territory\_text

</td><td>

Determines when an E.164 phone number field displays a territory label.-   Type: string
-   Default value: read-only
-   Other possible values:
    -   **all**: Always displays the territory label.
    -   **national**: Displays the territory label only if the phone number is in local format.
    -   **read-only**: Displays the territory label in read-only mode, regardless of whether the number is in local or international format.
    -   **read-only-national**: Displays the territory label in read-only mode only if the number is in local format.
    -   **list**: Displays the territory label in a list.
    -   **list-national**: Displays the territory label in a list if the number is in national format.
    -   **none**: Does not display the territory label.
-   Location: [Add](../../reference-pages/reference/r_AvailableSystemProperties.md#) to the System Properties \[sys\_properties\] table.

</td></tr><tr><td>

glide.phone\_number\_e164.display\_users\_idd

</td><td>

Determines whether to display the international direct dialing prefix between the territory selector choice list and the input field on forms.-   Type: true \| false
-   Default value: false
-   Location: [Add](../../reference-pages/reference/r_AvailableSystemProperties.md#) to the System Properties \[sys\_properties\] table.

</td></tr></tbody>
</table>## E.164 phone number field dictionary attributes

You can override the global system property with certain dictionary attributes.

<table id="table_rrg_nhj_3r"><thead><tr><th>

Dictionary attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

pn\_strict

</td><td>

Overrides the **glide.phone\_number\_e164.strict** property setting that requires all phone number entries match the format for the selected territory. Available values are identical to those described for the **glide.phone\_number\_e164.strict** property.-   Type: true \| false
-   Default value: true
-   Example:pn\_strict=false

</td></tr><tr><td>

pn\_allow\_national\_entry

</td><td>

Overrides the **glide.phone\_number\_e164.allow\_national\_entry** property setting that determines whether users can enter phone numbers in the local format or whether they must enter phone numbers in international format. Available values are identical to those described for the **glide.phone\_number\_e164.allow\_national\_entry** property.-   Type: true \| false
-   Default value: true
-   Example:pn\_allow\_national\_entry=false

</td></tr><tr><td>

pn\_display\_national

</td><td>

Overrides the **glide.phone\_number\_e164.display\_national** property setting for how an E.164 phone number field displays phone numbers. Available values are identical to those described for the **glide.phone\_number\_e164.display\_national** property.-   Type: string
-   Default value: false
-   Example:pn\_display\_national=all

</td></tr><tr><td>

pn\_display\_territory\_selector

</td><td>

Overrides the **glide.phone\_number\_e164.display\_territory\_selector** property setting that determines whether to display the territory selector choice list. Available values are identical to those described for the **glide.phone\_number\_e164.display\_territory\_selector** property.-   Type: true \| false
-   Default value: true
-   Example: pn\_display\_territory\_selector=false

</td></tr><tr><td>

pn\_display\_territory\_text

</td><td>

Overrides the **glide.phone\_number\_e164.display\_territory\_text** property that defines when a phone number field displays a territory label. Available values are identical to those described for the **glide.phone\_number\_e164.display\_territory\_text** property.-   Type: string
-   Default value: read-only
-   Example:pn\_display\_territory\_text=all

</td></tr><tr><td>

pn\_display\_users\_idd

</td><td>

Overrides the **glide.phone\_number\_e164.display\_users\_idd** property that determines whether to display the international direct dialing prefix between the territory selector choice list and the input box on forms. Available values are identical to those described for the **glide.phone\_number\_e164.display\_users\_idd** property.-   Type: true \| false
-   Default value: false
-   Example:pn\_display\_users\_idd=false

</td></tr></tbody>
</table>