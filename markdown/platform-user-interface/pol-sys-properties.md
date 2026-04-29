---
title: Next Experience system properties
description: List of system properties related to the Next Experience UI.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Next Experience UI, Configure UIs and portals, Configure user experiences]
---

# Next Experience system properties

List of system properties related to the Next Experience UI.

<table id="table_yvy_5wf_2rb"><thead><tr><th>

Property

</th><th>

Type

</th><th>

Default value

</th><th>

Description

</th></tr></thead><tbody><tr><td>

glide.ui.polarisberg

</td><td>

true \| false

</td><td>

true

</td><td>

Disables the Core UI styles for lists and forms in the Next Experience.

</td></tr><tr><td>

glide.ui.polaris.core\_ui\_exclude\_dark\_mode

</td><td>

true \| false

</td><td>

true

</td><td>

Excludes dark theme in the classic environment.

</td></tr><tr><td>

glide.ui.polaris.dark\_themes\_enabled

</td><td>

true \| false

</td><td>

true

</td><td>

Enables dark theming.

</td></tr><tr><td>

glide.ui.polaris.experience

</td><td>

true \| false

</td><td>

true

</td><td>

Enables the Unified Navigation experience on platform.

</td></tr><tr><td>

glide.ui.polaris.global\_search

</td><td>

true \| false

</td><td>

true

</td><td>

Toggle the Unified Navigation search functionality in the header.

</td></tr><tr><td>

glide.ui.polaris.history.url.param\_blocklist

</td><td>

string

</td><td>

\["tinyId"\]

</td><td>

URL parameters to ignore when removing duplicate URLs from the History menu.

</td></tr><tr><td>

glide.ui.polaris.list\_style.enable\_highlighted\_value\_style

</td><td>

true \| false

</td><td>

true

</td><td>

Enable the highlighted value style on list cells. When false, a dot displays next to values in lists rather than a highlight color over the value.

</td></tr><tr><td>

glide.ui.polaris.style.hide\_empty\_list\_image

</td><td>

true \| false

</td><td>

true

</td><td>

Hide the graphic that appears when a screen with no records is selected. **Note:** This system property applies only to the Core UI.

</td></tr><tr><td>

glide.ui.polaris.menus

</td><td>

true \| false

</td><td>

true

</td><td>

Toggle the Unified Navigation menus in the header.**Note:** If false is needed, it’s recommended to hide menus from specific roles.

</td></tr><tr><td>

glide.ui.polaris.login.show\_illustrations

</td><td>

string

</td><td>

true

</td><td>

Enables the display of illustrative graphics on the default login page.

</td></tr><tr><td>

glide.ui.polaris.login.style.background

</td><td>

RGB colors

</td><td>

 

</td><td>

Changes the login background color.

</td></tr><tr><td>

glide.ui.polaris.login.style.background\_gradient\_begin

</td><td>

RGB colors

</td><td>

 

</td><td>

Changes the colors of the beginning of the login background gradient.

</td></tr><tr><td>

glide.ui.polaris.login.style.background\_gradient\_end

</td><td>

RGB colors

</td><td>

 

</td><td>

Changes the colors of the end of the login background gradient.

</td></tr><tr><td>

glide.ui.polaris.login.style.mountain\_primary

</td><td>

RGB colors

</td><td>

 

</td><td>

Changes the primary colors of the login mountain graphic.

</td></tr><tr><td>

glide.ui.polaris.login.style.mountain\_secondary

</td><td>

RGB colors

</td><td>

 

</td><td>

Changes the secondary colors of the login mountain graphic.

</td></tr><tr><td>

overview\_help.visited.navui

</td><td>

string

</td><td>

true

</td><td>

Determines if the pop-up for Onboarding appears when the user logs in to an instance using Next Experience UI for the first time.

</td></tr><tr><td>

glide.ui.polaris.nav\_filter\_accuracy\_score

</td><td>

integer

</td><td>

75

</td><td>

Controls accuracy of the filtering in the Unified Navigation menus. The higher the number, the more accurate the match must be. A value of 100 means an exact match is required.

</td></tr></tbody>
</table>**Parent Topic:**[Configuring the Next Experience UI](../concept/next-experience-ui-admin.md)

