---
title: Integrate CSD 2.0 with other software providers
description: Integrate CSD 2.0 with client software distribution providers, such as Casper, Altiris, or LANDesk.Identify and create tables to store discovered data from the provider server.Create subflows in Workflow Studio to discover and store data, and deploy application.Create a provider record to configure the flows.Create UI actions to discover data, create software model, create software configuration, and create catalog item.
locale: en-US
release: xanadu
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 6
breadcrumb: [Client Software Distribution 2.0 application, Integration Hub available solutions, Building integrations in Integration Hub, Integration Hub, Creating integrations with applications]
---

# Integrate CSD 2.0 with other software providers

Integrate CSD 2.0 with client software distribution providers, such as Casper, Altiris, or LANDesk.

**Note:** Extending CSD 2.0 is an advanced procedure intended for use by experienced ServiceNow AI Platform developers only.

**Parent Topic:**[Client Software Distribution 2.0 application](csd-app-2.md)

## Create provider tables

Identify and create tables to store discovered data from the provider server.

For example, Application, Collection, and Deployment tables are provided with the Microsoft Endpoint Configuration Manager spoke. Similarly, create tables to store the discovered data. You must create your application table that extends the Client Software Distribution Application \(sn\_csd\_application\) table.

-   Create a provider server table that extends the Configuration Item \[cmdb\_ci\] table.
-   Create a software configuration table that extends Client Software Distribution Software Configuration \[sn\_csd\_software\_config\] table.

## Create subflows

Create subflows in Workflow Studio to discover and store data, and deploy application.

Create these subflows in Workflow Studio as per your requirement.

-   Discover and Store Data Subflow:

    Subflow to discover the provider server, retrieve the data from provider server, and store that data in the ServiceNow instance. This data should be stored in the tables you had earlier created for storing the server data.

-   Deploy Application Subflow:

    Subflow to deploy software from the provider server. This subflow provides information to the provider regarding deploying an application requested from the service catalog.

-   Revoke Application Subflow:

    Subflow to revoke an installation from the provider server. This subflow that provides information to the provider regarding the user or device from which the application should be removed.

-   Look up Configuration Data Subflow:

    Subflow to retrieve configuration data for the specified requested item or software configuration record.


The Deploy Application Template, Look up Configuration Data Template, and Revoke Application Template subflows are provided with CSD 2.0. You can use these subflows as reference and create subflows as per your requirement.

## Create a provider record

Create a provider record to configure the flows.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **Client Software Distribution 2.0** &gt; **Providers**.

2.  Click **New**.

3.  On the form, fill these values.

    |Field|Description|
    |-----|-----------|
    |Name|Name to identify the provider record.|
    |Software configuration table|Software configuration table you had created. This table extends Client Software Distribution Software Configuration \[sn\_csd\_software\_config\] table.|
    |Provider server table|Provider server table you had created. This table extends the Configuration Item \[cmdb\_ci\] table|
    |Discovery Flow|Subflow you had created to discover the provider server, retrieve the data from provider server, and store that data in the ServiceNow instance.|
    |Deployment Flow|Subflow you had created to deploy software from the provider server.|
    |Revocation Flow|Subflow you had created to revoke an installation from the provider server.|
    |Configuration Flow|Subflow you had created to retrieve configuration data for the specified requested item or software configuration record.|
    |Source List|List of discovery sources separated by a comma.|

    ![Sample provider record.](../image/csd2-prov-casper.png "Example provider record")

4.  Click **Save**.


## Create UI actions

Create UI actions to discover data, create software model, create software configuration, and create catalog item.

### Before you begin

Role required: admin

### About this task

See [UI actions](https://www.servicenow.com/docs/access?context=c_UIActions&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US) for more information about creating a UI action.

### Procedure

1.  Create a UI action to discover data.

    1.  Navigate to **System Definition** &gt; **UI Actions**.

    2.  Click **New**.

    3.  On the form, fill these values.

<table id="table_u5l_5q1_3sb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name to identify the UI action record. For example, `Discover Now`.

</td></tr><tr><td>

Table

</td><td>

Provider server table you had created. This table extends the Configuration Item \[cmdb\_ci\] table.

</td></tr><tr><td>

Script

</td><td>

Script to run when the UI action is executed. For example, enter ```
sn_csd.CSDUtil.startDiscovery(current);
```

</td></tr></tbody>
</table>    4.  Specify other fields as per your requirements.

    5.  Click **Save**.

2.  Create a UI action to create and link software model to your provider application or software.

    1.  Navigate to **System Definition** &gt; **UI Actions**.

    2.  Click **New**.

    3.  On the form, fill these values.

<table id="table_y54_dv1_3sb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name to identify the UI action record. For example, `Create Software Model`.

</td></tr><tr><td>

Table

</td><td>

Application table you had created. This table extends the Client Software Distribution Application \(sn\_csd\_application\) table.**Note:** You can use either SAM or CSD 2.0 software model and license tables. Depending upon how the `Determines whether to use SAM plugin(SAM Foundation or SAM Professional) tables for managing software models and licensing information` system property \(**sn\_csd.useSAMPlugin**\) is configured, use the corresponding software model table.

</td></tr><tr><td>

Condition

</td><td>

Defines the conditions that restrict when the UI action appears. For example, if software model is associated with the application or software, you may want to hide this UI action. So, enter `(gs.getProperty("sn_csd.useSAMPlugin") == 'true' && current.model=="" && (GlidePluginManager().isActive("com.snc.sams") || GlidePluginManager().isActive("com.snc.samp.core"))) || (gs.getProperty("sn_csd.useSAMPlugin") == 'false'&& current.csd_model=="")`.

</td></tr><tr><td>

Script

</td><td>

Script to run when the UI action is executed. For example, enter ```
var newModel = '';
var tableName = '';
if (gs.getProperty("sn_csd.useSAMPlugin") == 'true' && current.model == "" && (GlidePluginManager().isActive("com.snc.sams") || GlidePluginManager().isActive("com.snc.samp.core"))) {
    tableName = 'cmdb_software_product_model';

} else {
    tableName = 'sn_csd_software_product_model';
}
newModel = new sn_csd.CSDModelUtil().generateModel(current, tableName);

if (newModel != '')
    gs.setRedirect(tableName + ".do?sys_id=" + newModel);
```

</td></tr></tbody>
</table>    4.  Specify other fields as per your requirements.

    5.  Click **Save**.

3.  Create a UI action to create software configuration.

    1.  Navigate to **System Definition** &gt; **UI Actions**.

    2.  Click **New**.

    3.  On the form, fill these values.

<table id="table_fdz_rx1_3sb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name to identify the UI action record. For example, `Create Software Configuration`.

</td></tr><tr><td>

Table

</td><td>

Application table you had created. This table extends the Client Software Distribution Application \(sn\_csd\_application\) table.**Note:** You can use either SAM or CSD 2.0 software model and license tables. Depending upon how the `Determines whether to use SAM plugin(SAM Foundation or SAM Professional) tables for managing software models and licensing information` system property \(**sn\_csd.useSAMPlugin**\) is configured, use the corresponding software model table.

</td></tr><tr><td>

Condition

</td><td>

Defines the conditions that restrict when the UI action appears. For example, you may want to show the UI action only if the software model is configured. So, enter `(gs.getProperty("sn_csd.useSAMPlugin") == 'true' && current.model!="" && (GlidePluginManager().isActive("com.snc.sams") || GlidePluginManager().isActive("com.snc.samp.core"))) || (gs.getProperty("sn_csd.useSAMPlugin") == 'false' && current.csd_model!="")`.

</td></tr><tr><td>

Script

</td><td>

Script to run when the UI action is executed. For example, enter ```
var softwareConfig = createConfig(current);
action.setRedirectURL(softwareConfig);

function createConfig(appGr) {
    var gr = new GlideRecord("<Provider-software-configuration-table>");
    gr.initialize();
    gr.application = appGr.sys_id;
    gr.name = appGr.display_name;
    gr.insert();
    return gr;
}
```

 In this example, replace `<Provider-software-configuration-table>` with the provider server table you had created. This table extends the Configuration Item \[cmdb\_ci\] table.

</td></tr></tbody>
</table>    4.  Specify other fields as per your requirements.

    5.  Click **Save**.

4.  Create a UI action to create catalog item.

    1.  Navigate to **System Definition** &gt; **UI Actions**.

    2.  Click **New**.

    3.  On the form, fill these values.

<table id="table_kwx_w1b_3sb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name to identify the UI action record. For example, `Create Catalog Item`.

</td></tr><tr><td>

Table

</td><td>

Application table you had created. This table extends the Client Software Distribution Application \(sn\_csd\_application\) table.**Note:** You can use either SAM or CSD 2.0 software model and license tables. Depending upon how the `Determines whether to use SAM plugin(SAM Foundation or SAM Professional) tables for managing software models and licensing information` system property \(**sn\_csd.useSAMPlugin**\) is configured, use the corresponding software model table.

</td></tr><tr><td>

Condition

</td><td>

Defines the conditions that restrict when the UI action appears. For example, you may want to show this UI action only if software model is configured and there is at least one software configuration. So, enter `sn_csd.CSDUtil.isCSDSoftwareModelAndConfigurationSet(current, "<provider software configuration table>", "<internal name of software configuration table's column that refers to provider's application table>")`.

</td></tr><tr><td>

Script

</td><td>

Script to run when the UI action is executed. For example, enter ```
var catItemHandler = new sn_csd.CSDCatItemHandler(current);
var catItem = catItemHandler.createCatalogItem(current);



//first parameter - provider's software configuration table
//second paramter - internal name of software configuration table's column that refers to the provider's application table
var sfConfig = catItemHandler.getSoftwareConfig('<provider software configuration table>', '<internal name of software configuration table's column that refers to provider's application table>);
var gr = new GlideRecord('sn_csd_cat_item_fulfilment_config');
gr.initialize();
gr.cat_item = catItem.sys_id;
gr.provider = '<provider's Sys ID from sn_csd_provider table record>'; //provider's Sys ID from sn_csd_provider table record
gr.software_config = sfConfig; //populating software configuration
gr.insert();
action.setRedirectURL(catItem);
```

</td></tr></tbody>
</table>    4.  Specify other fields as per your requirements.

    5.  Click **Save**.


