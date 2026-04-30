---
title: Business stakeholder role for Enterprise Architecture \(formerly APM\)
description: For Enterprise Architecture users, Business Stakeholder \(com.snc.business\_stakeholder\) plugin contains the business stakeholder role for Enterprise Architecture. Users with this role can approve, view or read records of tables that are used to retrieve data for reports and dashboards. Customers can assign this role to any user who is a business stakeholder to review and approve reports.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Reference, Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Business stakeholder role for Enterprise Architecture \(formerly APM\)

For Enterprise Architecture users, Business Stakeholder \(com.snc.business\_stakeholder\) plugin contains the business stakeholder role for Enterprise Architecture. Users with this role can approve, view or read records of tables that are used to retrieve data for reports and dashboards. Customers can assign this role to any user who is a business stakeholder to review and approve reports.

## Upgrade information

-   **Upgrade customer**

    If you are upgrading to Zurich, the business stakeholder role for Enterprise Architecture is available only when you activate Read only roles for Enterprise Architecture \(com.snc.apm\_read\_roles\) plugin.

-   **New customer**

    If new customer, the Read only roles for Enterprise Architecture \(com.snc.apm\_read\_roles\) plugin is activated on zBoot. However, the business stakeholder role for Enterprise Architecture is available only when you install Enterprise Architecture plugin.


## Why business stakeholder read-only role

Analyst \(sn\_apm.apm\_analyst\) role in Enterprise Architecture is a licensable role that requires subscription. Users with this role can access all Enterprise Architecture PA dashboards and this role contains Enterprise Architecture administrator role who has different levels of access not only to read but to approve and update information data. Organizations procure this licensable role in limited numbers as it comes with a price. Business stakeholder role comes with a similar function but access is controlled at read-only level. Users with this role can access reports to review and approve only.

## Share dashboards with business stakeholder read-only users

Enterprise Architecture users with Business stakeholder role for Enterprise Architecture \(sn\_apm.apm\_read\) role have read-only access to dashboards and reports and all the underlying tables of the dashboards.

The base system provides access to users with this role to view **Application Landscape**, **Application 360**, and **Application Assessments** dashboards. You can also access all the tables from where the data are retrieved for these dashboard reports.

However, you can also configure your custom-created dashboards and reports to provide users with business stakeholder role. To provide read-only access to a business stakeholder, follow the steps in [Share a responsive dashboard](https://www.servicenow.com/docs/access?context=t_ControlAccessToADashboard&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US)

## Share widgets in dashboards with business stakeholders

To share individual widgets in the dashboard with the user who has the business stakeholder read-only role,

1.  Navigate to **Enterprise Architecture** &gt; **Application Portfolio Analysis** &gt; **Dashboard**
2.  Click the add widgets icon.
3.  Click the edit content icon of the widget that you want to share.
4.  Click the sharing icon.
5.  Click the **Share** option in the Sharing section.
6.  Search for business\_stakeholder in the search field and click to add the role in the Sharing settings window.
7.  Click **OK**.

## Enterprise Architecture tables accessible to users with business stakeholders role

Users with Business stakeholder role for Enterprise Architecture can access the following tables that store the data to load the widgets in the Enterprise Architecture dashboards:

|Label|Table name|
|-----|----------|
|Business Application|cmdb\_ci\_business\_app|
|Business Capability|cmdb\_ci\_business\_capability|
|CMDB Relationship|cmdb\_rel\_ci|
|CI Score|apm\_app\_score|
|Indicator Score|apm\_app\_indicator\_score|
|Indicators|apm\_metric|
|Fiscal Year|fiscal\_period|
|Business Process|cmdb\_ci\_business\_process|
|Application Family|apm\_application\_family|
|Application Category|apm\_application\_category|
|Application Category Groups|apm\_application\_category\_group|
|Scoring Profiles|apm\_application\_profile|
|Portfolio|pm\_portfolio|

**Parent Topic:**[Enterprise Architecture \(formerly Application Portfolio Management\) reference](apm-reference.md)

