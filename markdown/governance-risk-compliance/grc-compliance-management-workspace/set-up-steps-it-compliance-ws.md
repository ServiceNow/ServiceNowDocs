---
title: Configuration steps to filter IT-related data for IT Compliance Home page
description: There are three distinct steps that must be followed to segregate, associate, and display the IT-related data for the IT compliance manager to view in the IT Compliance Home page.
locale: en-US
release: xanadu
product: GRC: Compliance Management Workspace
classification: grc-compliance-management-workspace
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Configuring GRC Compliance Workspace, Performing compliance tasks in Compliance Workspace, Policy and Compliance Management, Governance, Risk, and Compliance]
---

# Configuration steps to filter IT-related data for IT Compliance Home page

There are three distinct steps that must be followed to segregate, associate, and display the IT-related data for the IT compliance manager to view in the IT Compliance Home page.

## GRC data segregation

In all the Compliance Workspace related forms, the **Functional domain** field is added in the **Settings** tab to segregate a particular data and classify it as IT related data. The user must add **IT risk and compliance** as the functional domain.

![Functional domain setting.](../image/FunctionalDomainSetting.png "Functional domain field")

The **Functional domain** field is available in all GRC compliance and audit workspace related forms such as Entity, Control, Control Objective, Policy, Authority document, Citation, Entity type, Entity class, Issue, Indicator, Indicator template, Acknowledgement campaign, Policy exception, Engagement, Test template, Test plan, Issue triage, Observation, Plan, Audit task, Milestone, Evidence request, and Evidence.

## Auto-association of the segregated data

If an audit or compliance object is identified as IT related, then all the related items associated to this object are also identified as IT related. The Functional domain configuration \[sn\_grc\_functional\_domain\_configuration\] table stores the data registry relationship between the parent object and its related child objects within the IT risk and compliance functional domain.

For example, if an entity is classified as IT related entity, then all the controls associated to this entity are auto-associated as IT-related controls. The related child object has all the configurations defined such as the parent table, the child table, and the relationship between the two.

As a system admin, you can define this configuration by navigating to **GRC Administration** &gt; **Functional domains** &gt; **Domain inheritance**. User must manually add the tag, functional domain, in the base forms such as Policy, Authority document, Entity type, Entity class, Entity, Plan, Engagement for auto-tagging the child records. When a parent table is tagged with a particular functional domain, and if the user removes the tag from one of its child records, then the removed tag is not added during auto-association. Similarly, if the user manually adds a tag, then the added tag is not removed during auto-association. The GRC functional domain user action \[sn\_grc\_functional\_domain\_user\_action\] table captures and stores all manual actions of the user in the **Functional domain** field of the record that belong to a particular table in the respective functional domain.

For more information on setting up auto-tagging, see the [IT Compliance Workspace – Setup and Configurations for auto-tagging \[KB1124058\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB1124058) article in the Now Support Knowledge Base.

![Functional domain configuration.](../image/DomainInheritance.png "Functional domain configuration")

A scheduled daily job \(GRCObjectsFunctionalDomainChanges\) runs and gathers the user's manual actions recorded in the table to read these relationships, auto-associate the child object to IT risk and compliance functional domain, and auto-populate the record in the related item of the parent table.

For more information on the tables used for IT compliance workspace, see [Components installed with Policy and Compliance Management](../../grc-policy-and-compliance/reference/r_InstallWPolAndCompl.md#).

## Display segregated data to IT compliance manager in IT Compliance Home page

The IT compliance manager is the user who can access the IT risk and compliance data in the Compliance Workspace. In the List view of the Compliance Workspace, there is a filter that restricts the display of all audit and compliance data but refines to display only the IT risk and compliance data. The filter uses the Functional domain field in the all the audit and compliance related base forms to filter and display the IT related data in the Compliance Workspace List modules.

![IT risk and compliance data filter.](../image/FilterITRelatedData.png "IT risk and compliance data filter")

**Note:** An admin or any user with both corporate compliance manager and IT compliance manager roles can view two list modules with the same name.

