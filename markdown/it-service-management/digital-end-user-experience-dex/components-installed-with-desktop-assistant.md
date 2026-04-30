---
title: Components installed with Desktop Assistant
description: Several types of components are installed with activation of the Desktop Assistant \[sn\_dex\_desktop\] plugin, including user roles and tables.
locale: en-US
release: yokohama
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [DEX Desktop Assistant reference, Reference, Digital End-User Experience, IT Service Management]
---

# Components installed with Desktop Assistant

Several types of components are installed with activation of the Desktop Assistant \[sn\_dex\_desktop\] plugin, including user roles and tables.

## Roles installed

<table id="table_jlk_jw3_dxb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Desktop Assistant administrator\[sn\_dex\_desktop.admin\]

</td><td>

Responsible for managing configurations and resolving any issues that may arise within the application.

</td><td>

sn\_dex\_desktop.user

</td></tr><tr><td>

Desktop Assistant user\[sn\_dex\_desktop.user\]

</td><td>

Responsible for using Desktop Assistant. They do not have the ability to configure any items within the application.

</td><td>

-   sn\_incident\_read
-   sn\_change\_read

</td></tr></tbody>
</table>## Tables installed

<table id="table_nlk_jw3_dxb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Desktop Assistant\[sn\_dex\_desktop\_app\]

</td><td>

Registry of the application. Administrators can go to this table to update the title of Desktop Assistant.

</td></tr><tr><td>

Desktop Assistant Card\[sn\_dex\_desktop\_app\_card\]

</td><td>

Records the card that is shown on Desktop Assistant. This is a base table for all card types.

</td></tr><tr><td>

Desktop Assistant Section\[sn\_dex\_desktop\_app\_section\]

</td><td>

Defines a section of the UI that acts as a container for the cards.

</td></tr><tr><td>

Desktop Assistant Tab\[sn\_dex\_desktop\_app\_tab\]

</td><td>

Defines different tabs that are present on the UI app, where each tab contains multiple sections.

</td></tr><tr><td>

Desktop Assistant App to Tab Mapping\[sn\_dex\_desktop\_app\_to\_tab\_mapping\]

</td><td>

Records a mapping between application and tabs.

</td></tr><tr><td>

Desktop Assistant Installation\[sn\_dex\_desktop\_exp\]

</td><td>

Records information about installation and usage of the Desktop Assistant application.

</td></tr><tr><td>

Hyperlink Card\[sn\_dex\_desktop\_hyperlink\_card\]

</td><td>

Card type to define hyperlinks.

</td></tr><tr><td>

Records View Card\[sn\_dex\_desktop\_records\_view\_card\]

</td><td>

Card type to define what records to view.

</td></tr><tr><td>

Record Creator Card\[sn\_dex\_desktop\_record\_creator\_card\]

</td><td>

Card type to define record creator with intended fields.

</td></tr><tr><td>

Section to Card Mapping\[sn\_dex\_desktop\_section\_to\_card\_mapping\]

</td><td>

Specifies all the cards in the given section.

</td></tr><tr><td>

Tab to Section Mapping\[sn\_dex\_desktop\_tab\_to\_section\_mapping\]

</td><td>

Specifies all the sections with in a page in a tab content.

</td></tr></tbody>
</table>**Parent Topic:**[DEX Desktop Assistant reference](dex-desktop-experience-reference.md)

