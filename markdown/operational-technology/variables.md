---
title: Variables
description: The Variables page provides a list of currently available variable sets.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/operational-technology/variables.html
release: australia
product: Operational Technology
classification: operational-technology
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Use the Console pages, Discovery Console for Operational Technology \(OT\), Operational Technology Native Discovery components, Operational Technology Discovery, Operational Technology]
---

# Variables

The Variables page provides a list of currently available variable sets.

## Variable overview

The Variables page displays the available Variable sets on your system. It provides a Search Variables field above the variable list.

You can also create new variable sets. Variables are used for Auto Query scans and can be associated to a specific Site.

The columns on the page are:

-   The bracket dot icon \[Omitted image "bracket-icon.png"\] Alt text: and lock icon \[Omitted image "lock-icon.png"\] Alt text: appear in the row next to the variable listing. When the bracket-dot symbol appears green next to the variable's name, the variable can be used for auto queries. When white, the variable can't be used for auto queries. The green lock indicates that the variable password is encrypted.

    **Note:** Encrypted Variable values in Variable Sets are obscured.

-   Name
-   Description
-   Sites display the name of the site to which the variable is associated.

    **Note:** A Site can only be associated with a single Variable set, but a Variable set can contain many variables.

-   Variables \(number of variables\)
-   Tools
    -   Select the pencil icon \[Omitted image "edit-icon.png"\] Alt text: to edit the variable set.
    -   Select the trash can icon \[Omitted image "trash-icon.png"\] Alt text: to delete the variable set.

\[Omitted image "variable-sets-page.png"\] Alt text: Variable page

## Special Variable sets

There are the following special variable sets:

-   Custom - Global
-   Driver - Global

The Custom-Global variable set can be edited by a user while the Driver - Global is read-only. The Custom - Global variable sets can be used to override indirectly the Driver - Global variable sets.

\[Omitted image "special-variable-sets.png"\] Alt text: Special variable sets

You can use variable sets \(Custom - Global or Site-specific sets\) to override a Variable set. See [Edit a Variable set](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/editing-a-variable-set.md) or [Create a Site-specific Variable set to use with Auto Query](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/add-variable-site-auto-query.md) for more information on editing a Variable set.

## Query Behavior

During a query, the query configuration is reviewed to see which Sites are being targeted. The query then searches to see if any Site-specific variable set override is defined. If no override is defined, it then searches to see if any Custom - Global override is defined. If it doesn't find a custom override, the query uses the default variable set from the Driver - Global.

## Importing or exporting Variables sets

You can import or export variable sets. You can select either the JSON or CSV formats. Select **Actions** to import or export.

\[Omitted image "action-button-variable-sets.png"\] Alt text: Action button

When you export Variable sets in either JSON or CSV format, you are prompted to include encrypted password variables. If you select yes, the values are exported as plain text. If you select no, the export excludes encrypted password variables.

\[Omitted image "export-variable-sets.png"\] Alt text: Export prompt

If the encrypted password is exported as plain text, it is no longer hidden and secure.

**Note:** Encrypted Variable values in Variable Sets are obscured. Encrypted values display as dots when set to encrypted.

\[Omitted image "encrypted-passwords.png"\] Alt text: Encrypted values

