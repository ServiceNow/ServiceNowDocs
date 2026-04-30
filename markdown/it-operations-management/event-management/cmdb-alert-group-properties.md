---
title: CMDB alert grouping — properties and functionality
description: Learn about the key properties and functionality of CMDB alert grouping, which facilitate efficient alert organization based on relationships and enhance the overall effectiveness of alert management.
locale: en-US
release: yokohama
product: Event Management
classification: event-management
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [CMDB based alert grouping, Alert grouping types and creation methods, Alert grouping, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# CMDB alert grouping — properties and functionality

Learn about the key properties and functionality of CMDB alert grouping, which facilitate efficient alert organization based on relationships and enhance the overall effectiveness of alert management.

## Properties for managing CMDB alert group creation

Use the properties listed in the following tables to control CMDB alert group creation. For more information, see [Configure scheduled job-based alert grouping](../task/enable-alert-grouping.md).

<table id="table_pjt_5lh_vdb"><thead><tr><th>

Property

</th><th>

Setting

</th></tr></thead><tbody><tr><td>

Enable CMDB correlation

 **sa\_analytics.agg.query\_cmdb\_correlation\_enabled**

</td><td>

Enable this property to automatically use CI relationships for alert aggregation, correlating alerts and creating CMDB alert groups.

</td></tr><tr><td>

Max number of relations between CIs in a topology that form a CMDB group

 **sa\_analytics.agg.query\_cmdb\_graph\_walk\_nodes**

</td><td>

Set the maximum number of enabled relations between CIs in a topology that form a CMDB group. For example, if you set this property to 3, a CI associated with an alert will automatically be grouped with similar CIs within three hops or less.

**Note:** This property setting impacts all types of relations used for alert aggregation. Using a value greater than 4 may negatively affect the performance of the alert aggregation job.

</td></tr><tr><td>

Use all CMDB relations for CMDB group correlation

 **evt\_mgmt.related\_cis\_get\_all\_relation\_types**

</td><td>

Set to true if you want to use all relationship types for CMDB grouping. The default setting for new users is that the option is set to true, meaning all relationship types are used for grouping. Set the property to false to filter the relations.

</td></tr></tbody>
</table>## Properties for managing automatic creation of CMDB alert groups for advanced use cases

In some use cases, you may need to ignore or exclude certain CI relationships from automatic alert group creation. In this case, the **evt\_mgmt.related\_cis\_get\_all\_relation\_types** property must be set to false, and the properties in the below table must also be configured.

**Note:** If the **evt\_mgmt.related\_cis\_get\_all\_relation\_types** property is set to false, and the relationship isn’t specified in the \[em\_suggested\_relation\_type\] table, the relationship is not considered for alert aggregation.

<table id="table_yzy_x4r_nyb"><thead><tr><th>

Property

</th><th>

Setting

</th></tr></thead><tbody><tr><td>

Enable Suggested Relations for CMDB Correlation

 **sa\_analytics.agg.query\_cmdb\_suggested\_relationship\_enabled**

</td><td>

Keep this property enabled to use any suggested relationships defined in the CMDB Group CI Relations \[em\_suggested\_relation\_type\] table when forming CMDB alert groups. To include a new relationship, add it to this table.

 This property is enabled by default.

</td></tr><tr><td>

Use CMDB relationship based on host-containment Metadata rules

 **evt\_mgmt.related\_cis\_use\_containment\_rules**

</td><td>

Containment rules specify which configuration item classes can be contained within another item through a specific relationship when creating a service template.

 Keep this property enabled when forming CMDB alert groups to use any host-containment rules defined in the Metadata Editor. For more details, see [CMDB dependent relationship rules](https://www.servicenow.com/docs/access?context=c_ServiceRulesMetadata&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

 This property is enabled by default.

</td></tr><tr><td>

Enable filtering by dependent relationship rules

 **evt\_mgmt.related\_cis\_use\_hosting\_rules**

</td><td>

Hosting rules define what classes of configuration items are hosted on other classes of configuration items.

 Keep this property enabled when forming CMDB alert groups to apply any hosting rules, which define which classes of configuration items are hosted on other classes.

 This property is hidden and enabled by default.

**Note:** If you need to change the default value, add the property, as it does not exist in the instance by default. For more information on how to create a property, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=yokohama&pubname=yokohama-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

</td></tr><tr><td>

Ignore CMDB alert groups from forming due to CI applicative flow relations

 **sa\_analytics.agg.ignore\_cmdb\_applicative\_flow**

</td><td>

Set this property to true to prevent CMDB groups from forming based on applicative flow relations for CI relations in application services.

 This property is hidden and enabled by default.

**Note:** If you need to change the default value, add the property, as it does not exist in the instance by default. For more information on how to create a property, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=yokohama&pubname=yokohama-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

</td></tr><tr><td>

**sa\_analytics.applicative\_flow\_rc\_enabled**

</td><td>

This property is hidden and enabled by default.

</td></tr></tbody>
</table>Event Management stores a map of related CIs in the Event Management CI Graph Reuse \[em\_ci\_graph\_reuse\] table for each processed CI. You can adjust the storage period by modifying the **sa\_analytics.agg.query\_cmdb\_graph\_reuse\_period** property, with the default set to one day \(86,400 seconds\). This process enhances the search performance of relations in the CMDB. To disable the storage process during advanced use-case configurations, set the property value to zero.

**Note:** If you need to change the default value, add the **sa\_analytics.agg.query\_cmdb\_graph\_reuse\_period** property, as it does not exist in the instance by default. For more information on how to create a property, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=yokohama&pubname=yokohama-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

