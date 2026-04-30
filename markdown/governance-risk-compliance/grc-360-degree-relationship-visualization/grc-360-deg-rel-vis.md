---
title: 360° Relationship Visualization
description: The 360° Relationship Visualization application allows you to visually explore the relationships between the different types of critical data that affect your business, such as controls, risks, and issues. The visualization also facilitates quick actions upon the information, such as adding a relationship, closing an issue, or approving a policy exception.
locale: en-US
release: zurich
product: GRC: 360 Degree Relationship Visualization
classification: grc-360-degree-relationship-visualization
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Common GRC features, Governance, Risk, and Compliance]
---

# 360° Relationship Visualization

The 360° Relationship Visualization application allows you to visually explore the relationships between the different types of critical data that affect your business, such as controls, risks, and issues. The visualization also facilitates quick actions upon the information, such as adding a relationship, closing an issue, or approving a policy exception.

Before you can use the 360° Relationship Visualization application, you must set up the data registry to define the kinds of relationships to be viewed and to configure the views of the data to be shown in the 360º View.

## Who uses the 360° Relationship Visualization

360° Relationship Visualization is used by GRC practitioners, such as compliance managers and analysts, risk managers and analysts, and auditors. 360° Relationship Visualization helps GRC practitioners to understand the critical data that affects their business. It also aids in effectively communicating the relationships and their impacts to C-suite executives or business users such as application or business service owners.

This table contains the responsibilities of all stakeholders involved with the 360º Relationship Visualization application and the Data Registry.

<table id="table_qjn_2q1_blb"><thead><tr><th>

Role title

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Data registry administrator \[`sn_data_registry.admin`\]

</td><td>

The data registry administrator has CRUD access to all records in the 360º views.

</td><td>

csn\_data\_registry.reader

</td></tr><tr><td>

Data registry reader \[`sn_data_registry.reader`\]

</td><td>

The data registry reader role must be granted to all GRC users \(for example, compliance managers and analysts, risk managers and analysts, and auditors\) who are working on 360° Relationship Visualization-enabled GRC forms.

</td><td>

-   canvas\_user
-   workspace\_user

</td></tr></tbody>
</table>-   **[Download and activate the GRC: 360° Relationship Visualization and Data Registry applications](../task/download_activate-360.md)**  
Before you can run the GRC: 360º Relationship Visualization \(com.servicenow\_sn\_grc\_360\_degree\_visualization\) and Data Registry \(com.sn\_app\_grc\_data\_registry\) applications in your instance, you must download them from the ServiceNow Store.
-   **[Setting up the 360º views](set-up-360-data-reg.md#)**  
To effectively use the 360° Relationship Visualization application, you must register existing relationships between the types of data you want to view, and then configure how the 360º view displays that data.
-   **[Exploring the 360º view](understanding-360-view.md#)**  
After you have successfully set up your data registries for the tables you use, you can use the 360º view feature to view the relationships between a selected record and related objects, such as controls, risks, and entity types.

**Parent Topic:**[Common Governance, Risk, and Compliance features](../../grc-common/concept/common-grc-features.md)

