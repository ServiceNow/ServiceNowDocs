---
title: Configure Operational Resilience properties
description: Configure main properties of the Operational Resilience so that you can set up and fetch data into the application for reporting purposes.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Operational Resilience, Governance, Risk, and Compliance]
---

# Configure Operational Resilience properties

Configure main properties of the Operational Resilience so that you can set up and fetch data into the application for reporting purposes.

## Before you begin

Role required: sn\_oper\_res.admin

## About this task

Configurations and customizations: When you update an application property, it's considered a configuration. If a function change needs modifications to the code in  Operational Resilience, like the script include, it's classified as a customization.

## Procedure

1.  Navigate to **All** &gt; **System Properties** &gt; **All Properties**.

2.  Filter the properties for GRC: Operational Resilience application.

    The properties for GRC: Operational Resilience application are displayed. For a list of the properties, see [Properties installed with Operational Resilience](../reference/props-installed-with-or.md).

3.  Update the values of Dependency pillars in the **sn\_oper\_res.dependency\_pillars** property by adding the sys\_ids of the pillars to the **Value** field.

    You can add the sys\_ids separated by commas such as e4f77de4537310108722ddeeff7b1263,ab5c78b0533112105806ddeeff7b126f,9c38fde4537310108722ddeeff7b12d0,a5187de4537310108722ddeeff7b127a,c4c775e4537310108722ddeeff7b12d7,2fad3034533112105806ddeeff7b123f. Refer to the following pillars and their corresponding sys\_ids:

    -   Application Service: e4f77de4537310108722ddeeff7b1263
    -   People: ab5c78b0533112105806ddeeff7b126f
    -   Data: 9c38fde4537310108722ddeeff7b12d0
    -   Suppliers: a5187de4537310108722ddeeff7b127a
    -   Technology: c4c775e4537310108722ddeeff7b12d7
    -   Facilities: 2fad3034533112105806ddeeff7b123f
4.  Update the **sn\_oper\_res.max\_top** property.

    This property is used for the 'Top vulnerabilities to be fixed' section on the Home page. If the property value is set to 5, records are generated for the top 5 vulnerabilities which have most impacted entities, and they are displayed in the ''Top vulnerabilities to be fixed' report on the Home page.

5.  Configure the **sn\_oper\_res.top\_class\_name** property to designate any class as the top class in the dashboard.

    Starting with Operational Resilience Release 21.0.x, this property is updated so that any node, such as business service, business process, or application service, can be the top node. This property is applicable only for the dashboards and not for the Workspace forms. For information on configuring the property, see [Using the flexible data model](../concept/flexible-data-model-changes.md).

6.  Select **Update**.

    The updated properties are saved.


