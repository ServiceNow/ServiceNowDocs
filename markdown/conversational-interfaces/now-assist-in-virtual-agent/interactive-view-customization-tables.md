---
title: Interactive view customization tables
description: Make your own user interface applicable to the interactive view with some customization in the following two tables: Now Canvas Definition \[sn\_now\_canvas\_definition.list\] and Now Canvas Configuration \[sn\_now\_canvas\_configuration.list\].
locale: en-US
release: australia
product: Now Assist in Virtual Agent
classification: now-assist-in-virtual-agent
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Now Assist in Virtual Agent reference, Now Assist in Virtual Agent, Conversational Interfaces]
---

# Interactive view customization tables

Make your own user interface applicable to the interactive view with some customization in the following two tables: Now Canvas Definition \[sn\_now\_canvas\_definition.list\] and Now Canvas Configuration \[sn\_now\_canvas\_configuration.list\].

## Interactive view customization tables overview

You must first work with the Now Canvas Definition table \[sn\_now\_canvas\_definition.list\] before working with the Now Canvas Configuration table \[sn\_now\_canvas\_configuration.list\] because the configuration table relies upon data found in the definition table. The Now Canvas Definition table \[sn\_now\_canvas\_definition.list\] defines the user interfaces and the Now Canvas Configuration table \[sn\_now\_canvas\_configuration.list\] serves as the action of when to call the interactive view for the defined user interface. The Now Canvas Definition table \[sn\_now\_canvas\_definition.list\] only has one default definition: iframe.

The following tables list the fields that you must work with to create those customized interactive views. Some of these fields may not be available upon default. For more information about how to add or remove fields from the form layout, see Configuring the form layout.

|Field|Description|
|-----|-----------|
|Name|Name of the user interface that is going to use the interactive view.|
|Definition type|Select either UX macroponent or UX component. Depending on this selection, either the **UX Component Definition** field or **UX Macroponent Definition** field displays.|
|UX Component Definition|Name of the independent seismic component.|
|UX Macroponent Definition|Name of the UXF page that uses UI builder.|

<table id="table_qgp_vls_hhc"><thead><tr><th>

 

</th><th>

 

</th></tr></thead><tbody><tr><td>

Canvas ID

</td><td>

Name of the user interface that is pulled from the Now Canvas Definition table \[sn\_now\_canvas\_definition.list\].

</td></tr><tr><td>

Active

</td><td>

Status of whether this is an active or non-active interactive view.

</td></tr><tr><td>

Related Table Name

</td><td>

Related table can be one of the following:-   AI Agent
-   Generative AI skill
-   Tool
-   Topic
-   Use case

</td></tr><tr><td>

Related Record

</td><td>

Related record associated with the related table.

</td></tr><tr><td>

M2M Canvas Configuration Deployment Channels related list

</td><td>

Related list that displays the name of the active or in-active deployment channel associated with this interactive view. Select **New** to associate this interactive view configuration with a deployment channel. You must do this to complete the interactive view association with the intended deployment channel. Searching at the **Deployment Channel** field level opens up the Now Assist Deployment Channels \[sys\_now\_assist\_deployment\_channel\_list.do\] table to select a channel.

</td></tr></tbody>
</table>