---
title: User hierarchy
description: With a user hierarchy, your managers can see the records of those users who report to them.
locale: en-US
release: zurich
product: GRC Common Functions
classification: grc-common-functions
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Common GRC features, Governance, Risk, and Compliance]
---

# User hierarchy

With a user hierarchy, your managers can see the records of those users who report to them.

The user hierarchy is based on the configuration in the sys\_user table. The user hierarchy is stored separately for the GRC tables.

To understand how a user hierarchy works, let's look at the following example. Users Abel and Jack report to Adam. Adam reports to Daniel. With a user hierarchy, Adam can view the work performed by Abel and Jack. Similarly, Daniel can view the work performed by Adam, Abel, and Jack.

Let's see another example of a manager and a user hierarchy.

![Managers and their users' hierarchy.](../image/manager-user-hierarchy.png "Manager and user hierarchy")

In this example, the sales manager can see the data that the sales team has submitted. The VP of sales can see the data or reports that are submitted by the sales managers and the sales team.

The VP of service can see the data that is submitted by the service managers and the support team. The CEO of the organization can see the work performed by both sales and service teams.

## Enabling the properties for the user hierarchy functionality

As a GRC administrator, you can enable the following properties under the GRC properties module in an instance.

<table id="table_lvx_byr_xsb"><thead><tr><th>

Property

</th><th>

Action

</th></tr></thead><tbody><tr><td>

**Enable user hierarchy access control**

</td><td>

Enable the user hierarchy functionality by selecting the **Yes** option on the **Enable user hierarchy access control** property. This property is turned off by default. After you enable this property, you can also turn it off again.

</td></tr><tr><td>

**Frequency of user hierarchy recalculation**

</td><td>

Use the **Frequency of user hierarchy recalculation** property to calculate the user hierarchy for all the records in the sn\_grc\_user\_hierarchy\_configuration table. The property is set to **Weekly** by default.

 To calculate the user hierarchy for the records at different intervals, select **sn\_grc.user\_hierarchy\_sync\_frequency** and change the schedule from **Weekly** to **Daily** or **Monthly**.

</td></tr><tr><td>

**Maximum batch size while recalculating hierarchy for user hierarchy records**

</td><td>

Use the **Maximum batch size while recalculating hierarchy for user hierarchy records** property to process the records in a maximum batch size so that you can recalculate the user hierarchy of the records. This property is set to 1000 by default.

 To recalculate the user hierarchy of the records, select the property and update the maximum batch size to an integer value.

</td></tr></tbody>
</table>**Note:** After you enable the user hierarchy properties, the user hierarchy functionality is supported only in certain sets of tables. You can learn more about these tables in the next section.

## Tables that are used to support the user hierarchy functionality

The following tables are used to support the user hierarchy functionality.

|Table|Description|
|-----|-----------|
|sn\_grc\_hierarchy|Table that maintains the hierarchy of the users.|
|sn\_grc\_user\_hierarchy|Table that displays the name of the user, the managerial hierarchy, and the last synchronized details. As a user with the sn\_grc.user\_hierarchy\_reader role, you can read the records in this table. No other user can manually create, update, or delete the records in this table.|
|sn\_grc\_user\_hierarchy\_configuration|Table that contains a separate record for each table where the user hierarchy access control is enabled. As a GRC administrator, you can manually create and delete the records in this table. As a user with the sn\_grc.user\_hierarchy\_admin role, you can also read or update the records in this table.|

## User hierarchy configurations module

The User hierarchy configuration module is displayed in your instance only after you enable the user hierarchy properties. The User hierarchy configuration module, which is shown in the following example, lists the tables on which you have enabled the user hierarchy functionality.

![User hierarchy configuration module.](../image/user-hierarchy-configuration.png "User hierarchy configuration module")

Access control lists \(ACLs\): By default, a few access control lists are shipped with the GRC application, and they are stored in the sys\_security\_acl table. You can define a filter condition to check if the user hierarchy access control is enabled. You can create your own access control lists depending on your configuration and requirements.

For information on how to configure the user hierarchy access control on your custom tables, see [KB1095957](https://support.servicenow.com/nav_to.do?uri=%2Fkb%3Fid%3Dkb_article_view%26sysparm_article%3DKB1095957).

**Note:** You must log in to Now Support to view the Knowledge Base articles.

-   **[Create a user hierarchy configuration record](../task/configure-a-new-user-hierarchy-configuration-record.md)**  
Create a user hierarchy configuration record for a table so that you can enable your managers to view the records of the users who report to them.

**Parent Topic:**[Common Governance, Risk, and Compliance features](common-grc-features.md)

