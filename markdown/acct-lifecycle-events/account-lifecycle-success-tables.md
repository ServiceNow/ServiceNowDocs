---
title: Customer success management tables
description: This section includes the Customer Success Management tables.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Reference, Customer Success Management]
---

# Customer success management tables

This section includes the Customer Success Management tables.

|Table|Description|
|-----|-----------|
|Engagement|As a provider, delivering value to an enterprise customer \[account\] is not a ‘one-time’’ event, it is a journey with multiple activities, both internal and external during its lifecycle.|
|Success objective|Success objectives represents the value that the provider has sold to an enterprise customer. This value can be defined for one or more products.|
|Success outcome|Success outcomes are measurable components of success objectives. They can be monitored through analytics within the ServiceNow AI Platform or through a third-party integration tool.|
|Success initiative|Success initiatives are a planned set of actions \(workflows\) that the provider and enterprise customer agree to take and complete on the customer's value realization journey.|
|Customer play|Customer plays are an unplanned set of actions a provider takes to support a customer engagement activity.|
|Success task|Success tasks are planned or unplanned actions that either the provider or enterprise customer must complete in support of a success initiative \(planned\) or a customer play \(unplanned\).|
|Touchpoint|A touchpoint captures and supports conversations such as scheduling calls, sharing reports, and presentation material.|
|Touchpoint Applicable Records|Used to link the multiple records to a single touchpoint.|
|Internal play|Internal plays are planned or unplanned actions tied to the engagement lifecycle. Internal plays often require internal sub-tasks and follow a playbook with pre-defined activities.|
|Internal play task|Internal play tasks are actions that are created as result of a specific internal plays being created. These tasks must have a clear purpose and if possible, must be created through playbook automation \[automatic, optional, or conditional\].|
|Risk signal and issue|Risk signals and issues are a way of recording and managing risks tied to an engagement or onboarding so that the provider can take appropriate actions.|
|Definition record|The Customer Success definition record is used to specify categories that can be used to launch success play workflows that can create records and trigger playbooks automatically.|
|Success launcher notifier|The success launcher notifier tracks the status of the success play.|
|Data source|Specifies whether an external source or performance indicators are used to collect data to calculate the health or risk score.|
|Context|Used to associate the data being collected with an engagement or success outcome table.|
|Context engine mapper|Specifies the record for which the data source will be applicable.|
|Context engine data|Based on the data source and context engine mapper, when the scheduled jobs are run, the collected data is stored in the context engine data table.|
|Engagement health definition|Used to set up the health definition. You can define a global health definition or an engagement specific health definition.|
|Health metric configuration|Used to specify the metrics used to calculate the health score and the weight given to each metric.|
|Engagement risk definition|If the type is metric, specifies the metric, threshold condition, threshold and applicable engagements. If the type is table, the risk records are created for the records matching table and conditions specified.|
|Risk threshold override|If you want to override a risk threshold value, you can define additional conditions in this table.|
|Risk occurrence|Records risk occurrence if an active risk exists for the category, source record and engagement.|
|Color banding|Configure the color bands for health score either at the global level or for specific metrics.|
|Applicable sold products|Associates the applicable sold products with an engagement.|
|Applicable entitlements|Associates applicable entitlements with an engagement.|
|Applicable team members|Associates team members with an engagement.|
|Applicable customer team|Associate a customer team with an engagement.|

**Parent Topic:**[Customer Success Management reference](account-lifecycle-reference.md)

