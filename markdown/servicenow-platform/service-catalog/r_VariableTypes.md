---
title: Types of service catalog variables
description: Variables allow you to specify questions for a catalog item. Several types of service catalog variables are provided. Some variable types accept variable attributes.
locale: en-US
release: yokohama
product: Service Catalog
classification: service-catalog
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Service catalog variables, Service Catalog Reference, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Types of service catalog variables

Variables allow you to specify questions for a catalog item. Several types of service catalog variables are provided. Some variable types accept variable attributes.

See the following sections for more details on each variable type. For details on creating a variable, see [Create a service catalog variable](../task/t_CreateAVariableForACatalogItem.md). You can also provide help text for any service catalog variable. For information on defining help information, see [Define help information for a service catalog variable](../task/t_DefineHelpInformation.md).

## Support in various channels

Service Catalog variables are supported in various channels. For information on their availability, see [Variable support in various channels](variables-availability.md).

-   **[Attachment](attachment.md)**  
When submitting a catalog item request, this variable lets you upload an attachment for a question of the item.
-   **[Break](break.md)**  
The break variable displays a horizontal line across the form.
-   **[Check box](check-box.md)**  
The check box variable lets you enable and disable options by selecting and clearing it.
-   **[Container start, container split, and container end](contain-start-split-end.md)**  
The container start, container split, and container end variables define a layout for a container that can hold more variables.
-   **[Date, Date and time, and Duration](date.md)**  
The date variable creates a widget with a field and calendar to select a date.
-   **[Email](email.md)**  
The email variable creates a widget to enter and select an email address.
-   **[HTML](html.md)**  
The HTML variable lets you provide content with advanced formatting, including images, for a catalog item.
-   **[IP Address](ip-address.md)**  
Use the IP address variable to specify the IPv4 and IPv6 data for a catalog item.
-   **[Label](label.md)**  
The label variable displays a label across the form. Labels are formatting elements. No data is collected.
-   **[List collector](list-collector.md)**  
The list collector variable creates an interface that lets you select and add multiple records from a table.
-   **[Lookup multiple choice](lookup-multiple-choice.md)**  
The lookup multiple choice variable creates radio buttons using data from a table. Its functionality is similar to the lookup select box variable, which creates a choice list from queried data.
-   **[Lookup select box](lookup-select-box.md)**  
The lookup select box variable creates a choice list using data queried from a table. Its functionality is similar to the lookup multiple choice variable, which creates radio buttons from queried data.
-   **[Custom and Custom with label](custom.md)**  
The custom variable inserts a UI macro into the catalog item. Custom with label variable inserts a UI macro with a label.
-   **[Masked](masked.md)**  
The masked variable inserts a field that masks the text entered.
-   **[Multi-line text](multi-line.md)**  
The multi-line text variable creates a field that lets you enter multiple lines of text.
-   **[Multiple choice](multiple-choice.md)**  
The multiple choice variable creates radio buttons for question choices.
-   **[Numeric scale](numeric-scale.md)**  
The numeric scale variable creates a set of radio buttons for a range of options, like a Likert scale.
-   **[Reference](reference.md)**  
A reference variable references a record in another table. For example, a variable named point\_of\_contact references the User \[sys\_user\] table.
-   **[Requested for](requested-for.md)**  
Before submitting a catalog item request, this variable helps you specify who this request can be submitted for.
-   **[Rich Text Label](rich-text-label.md)**  
This variable displays a formatted label on a catalog item form.
-   **[Select box](select-box.md)**  
The select box variable creates a list from predefined question choices.
-   **[Single-line text](single-line-text.md)**  
The single-line text variable creates a field to enter a single line of text.
-   **[UI page](ui-page.md)**  
The UI page variable inserts a UI page into the catalog item.
-   **[URL](url.md)**  
The URL variable creates a widget for users to enter URLs.
-   **[Wide single-line text](wide-single-line-text.md)**  
The wide single-line text variable creates a field that spans the form, letting users enter longer lines of text.
-   **[Yes/No](yes-no.md)**  
The Yes or No variable creates a choice list with **Yes** and **No** as options.
-   **[Variable support in various channels](variables-availability.md)**  
Service Catalog variables are supported in various channels.

**Parent Topic:**[Service catalog variables](../concept/c_ServiceCatalogVariables.md)

