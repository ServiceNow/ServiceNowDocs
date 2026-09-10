---
title: Components installed with ServiceNow AI Lens
description: Several types of components are installed with the activation of the ServiceNow AI Lens plugin, including user roles.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/servicenow-lens/components-installed-sn-lens.html
release: australia
product: ServiceNow Lens
classification: servicenow-lens
topic_type: reference
last_updated: "2026-08-04"
reading_time_minutes: 3
keywords: [Components installed with ServiceNow Lens, Roles installed with ServiceNow Lens, Tables installed with ServiceNow Lens, ServiceNow Lens roles, ServiceNow Lens tables]
breadcrumb: [Reference, ServiceNow AI Lens, Enable AI experiences]
---

# Components installed with ServiceNow AI Lens

Several types of components are installed with the activation of the ServiceNow AI Lens plugin, including user roles.

## Roles installed

|Role title \[name\]|Description|Contains roles|
|-------------------|-----------|--------------|
|Lens user \[lens\_user\]|Enables you to use ServiceNow AI Lens.|sn\_nowassist\_admin.user|
|Lens admin \[lens\_admin\]|Enables you to configure lens actions.|lens\_user|

## Tables installed

<table id="table_fbz_45z_vdb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Lens Execution \(lens\_execution\)

</td><td>

Whenever a record is created or updated by using ServiceNow AI Lens, a record is created in the execution table. This record includes details such as the table from which the UI action is clicked and the editable fields on the form, which are then passed to the Lens app.**Note:** You can view only records created for or assigned to your user account.

</td></tr><tr><td>

Lens Transaction \(lens\_transaction\)

</td><td>

If a user performs the analyze action on the ServiceNow AI Lens app, the response received from the large language model \(LLM\) is stored in the transaction table.**Note:** You can view only records created for or assigned to your user account.

</td></tr></tbody>
</table>## System properties installed

These properties exist in the System Properties \[sys\_properties\] table. The admin role is necessary to set system properties.

**Note:**

To open the System Properties \[sys\_properties\] table, enter `sys_properties.list` in the navigation filter.

<table id="table_oj2_25n_lkc"><thead><tr><th>

System property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_app\_lens\_core.lens\_enable\_auto\_login

</td><td>

If true, ServiceNow AI Lens automatically signs in users using their previous token. If false, users are prompted to sign in each time they launch the application.-   Type: Boolean
-   Default value: false

</td></tr><tr><td>

sn\_app\_lens\_core.sn\_lens\_repository\_url

</td><td>

Repository URL for downloading ServiceNow AI Lens-   Type: String
-   Default value: `https://install.service-now.com/glide/distribution/builds/package/app-signed/`

</td></tr><tr><td>

sn\_app\_lens\_core.show\_lens\_action\_on\_all\_tables

</td><td>

Property to show or hide the **Create with Lens** or **Update with Lens** button on all tables, depending on whether it’s set to True or False. If True, includes all tables except those that are specified in the **sn\_app\_lens\_core.lens\_exclusion\_table\_list** property. If False, includes all tables that are specified in the **sn\_app\_lens\_core.lens\_inclusion\_table\_list** property.-   Type: Boolean
-   Default value: true

</td></tr><tr><td>

sn\_app\_lens\_core.lens\_inclusion\_table\_list

</td><td>

Property to specify the tables that will display the **Create with Lens** or **Update with Lens** button. This list will be considered when the **sn\_app\_lens\_core.show\_lens\_action\_on\_all\_tables** property is set to False. To specify the names of multiple tables, separate the table names with commas.-   Type: String
-   Default value: None

</td></tr><tr><td>

sn\_app\_lens\_core.lens\_exclusion\_table\_list

</td><td>

Property to specify the tables that will not display the **Create with Lens** or **Update with Lens** button. This list will be considered when the **sn\_app\_lens\_core.show\_lens\_action\_on\_all\_tables** property is set to true. To specify the names of multiple tables, separate the table names with commas.-   Type: String
-   Default value: None

</td></tr><tr><td>

sn\_app\_lens\_core.show\_lens\_action\_on\_all\_catItems

</td><td>

Property to show or hide the **Create with Lens** or **Update with Lens** button on all catalog items, depending on whether it’s set to True or False. If True, includes all catalog items except those that are specified in the **sn\_app\_lens\_core.lens\_exclusion\_catItem\_list** property. If False, includes all catalog items that are specified in the **sn\_app\_lens\_core.lens\_inclusion\_catItem\_list** property.-   Type: Boolean
-   Default value: true

</td></tr><tr><td>

sn\_app\_lens\_core.lens\_inclusion\_catItem\_list

</td><td>

Property to specify the catalog items that will display the **Create with Lens** or **Update with Lens** button. This list will be considered when the **sn\_app\_lens\_core.show\_lens\_action\_on\_all\_catItems** property is set to False. To specify the names of multiple catalog items, separate the catalog item names with commas.-   Type: String
-   Default value: None

</td></tr><tr><td>

sn\_app\_lens\_core.lens\_exclusion\_catItem\_list

</td><td>

Property to specify the catalog items that will not display the **Create with Lens** or **Update with Lens** button. This list will be considered when the **sn\_app\_lens\_core.show\_lens\_action\_on\_all\_catItems** property is set to true. To specify the names of multiple catalog items, separate the catalog item names with commas.-   Type: String
-   Default value: None

</td></tr></tbody>
</table>**Parent Topic:**[ServiceNow AI Lens reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/servicenow-lens/servicenow-lens-reference.md)

