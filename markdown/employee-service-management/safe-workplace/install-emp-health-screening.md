---
title: Install Employee Health Screening
description: You can install the Employee Health Screening application if you have the admin role. This application includes demo data and installs the related store applications and plugins if they are not already installed.Roles and tables are installed with the Employee Health Screening application.
locale: en-US
release: australia
product: Safe Workplace
classification: safe-workplace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Employee Health Screening, Safe Workplace, Health and Safety, Employee Service Management]
---

# Install Employee Health Screening

You can install the Employee Health Screening application if you have the admin role. This application includes demo data and installs the related store applications and plugins if they are not already installed.

## Before you begin

Ensure that the application and all of its associated store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).

If you've subscribed to the Safe Workplace suite and you already have some of the apps installed, refer to the following order of installation for the remaining apps.

-   Emergency Outreach \(sn\_imt\_checkin\)
-   Employee Health Screening \(sn\_imt\_monitoring\)
-   Workplace PPE Inventory Management \(sn\_imt\_ppe\)
-   Employee Readiness Surveys \(sn\_imt\_readiness\)
-   COVID-19 Global Health Data Set \(sn\_imt\_c19datafeed\)
-   Contact Tracing \(sn\_imt\_tracing\)
-   Emergency Self Report \(sn\_imt\_quarantine\)
-   Workplace Core \(sn\_wsd\_core\)
-   Safe Workplace Dashboard \(sn\_imt\_dashboard\)
-   Emergency Response Management for Now Mobile \(sn\_imt\_mobile\)
-   Employee Travel Safety \(sn\_imt\_travel\)
-   Health and Safety Testing \(sn\_imt\_health\_test\)
-   Vaccination Status \(sn\_imt\_vaccine\)

Role required: admin

## Procedure

1.  Navigate to **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the application using the filter criteria and search field.

    You can search for the application by its name or ID. If you cannot find an application, you may have to request it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release note information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

3.  Click **Install**.

4.  In the Application installation dialog box, review the application dependencies.

    If your application requires other applications, install them first if they are not already installed.

    Installing your application also automatically installs the dependent applications or plugins if they are not installed already.

5.  If demo data is available and you want to install it, click **Load demo data**.

    Some applications include demo data, which are sample records that describe application features for common use cases. Load demo data when you first install the application on a development or test instance.

    **Note:** If you don't load the demo data for a store application during installation, it's not available to load later.

6.  Click **Install**.


**Parent Topic:**[Employee Health Screening](../concept/employee-health-screening.md)

## Components installed with Employee Health Screening

Roles and tables are installed with the Employee Health Screening application.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see Find components installed with an application.

Demo data is available for this feature.

### Roles installed

<table id="table_u1t_gb1_wdb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Health monitor\[sn\_imt\_monitoring.monitoring\_user\]

</td><td>

Use the health screening page to record returning employee details. View employee health and safety status.

</td><td>

-   report\_user
-   sn\_imt\_core.reader

</td></tr><tr><td>

Health monitor administrator\[sn\_imt\_monitoring.monitoring\_admin\]

</td><td>

Configure properties and temperature overrides and view the dashboard.

</td><td>

-   report\_user
-   sn\_imt\_monitoring.monitoring\_user

</td></tr></tbody>
</table>### Tables installed

<table id="table_ftt_nrn_2mb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Request for Entry\[sn\_imt\_monitoring\_request\_for\_entry\]

</td><td>

Results of employee health screening events. If the **sn\_imt\_monitoring.auto\_create\_request** property is enabled, the table also includes results from health monitors looking up an employee's health and safety status. For results from a health screening, the **Source** field is set to **Health screen**. For results from a status lookup, the **Source** field is set to **Auto-checkin**.

</td></tr><tr><td>

Location Override\[sn\_imt\_monitoring\_temperature\_override\]

</td><td>

Locations where temperature thresholds for employees are different from the system property threshold.

</td></tr><tr><td>

Employee Health Verification\[sn\_imt\_monitoring\_health\_verification\]

</td><td>

All health verifications submitted by employees.

</td></tr><tr><td>

Visitor Request For Entry\[sn\_imt\_monitoring\_visitor\_request\_for\_entry\]

</td><td>

Results of visitor health screening events.

</td></tr><tr><td>

Visitor Location Override\[sn\_imt\_monitoring\_visitor\_temperature\_override\]

</td><td>

Locations where temperature thresholds for visitors are different from the system property threshold.

</td></tr><tr><td>

Information Messages\[sn\_imt\_monitoring\_information\_message\]

</td><td>

Messages provided to specific types of users \(determined by their audience\) when they attempt to enter a location.

</td></tr></tbody>
</table>