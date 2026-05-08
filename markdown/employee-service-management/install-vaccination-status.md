---
title: Install Vaccination Status
description: You can install Vaccination Status if you have the admin role.Several types of components are installed with Vaccination Status, including user roles and tables.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Vaccination Status, Safe Workplace, Health and Safety, Employee Service Management]
---

# Install Vaccination Status

You can install Vaccination Status if you have the admin role.

## Before you begin

Vaccination Status requires the ServiceNow® Employee Readiness Core and Emergency Outreach applications.

Role required: admin

<table id="table_kxr_yz3_blb"><thead><tr><th>

Type

</th><th>

Instructions

</th></tr></thead><tbody><tr><td>

Commercial on-premise

</td><td>

Visit the ServiceNow® Store to download and install the application.

</td></tr><tr><td>

Federal hosted

</td><td>

See the [Federal downloads for the Emergency Response Management and Safe Workplace suite apps \[KB0030260\]](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030260) article in the Store Help Center for more information.

</td></tr><tr><td>

Federal on-premise

</td><td>

If you are a federal on-premise customer and you would like to install this application, reach out to your sales representative or open a Now Support or HIWAVE ticket. In the ticket, request to be routed to the SHOT team.

 See the [Federal downloads for the Emergency Response Management and Safe Workplace suite apps \[KB0030260\]](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030260) article in the Store Help Center for more information.

</td></tr><tr><td>

On-premise

</td><td>

See the [Commercial downloads for the Emergency Response Management and Safe Workplace suite apps \[KB0030258\]](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030258) article in the Store Help Center for more information.

</td></tr></tbody>
</table>If you've subscribed to the Safe Workplace suite and you already have some of the apps installed, refer to the following order of installation for the remaining apps.

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

## Procedure

1.  Navigate to **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Search for `Vaccination Status`.

3.  Click **Install**.

    The Application installation dialog box opens.

4.  Click **Activate**.


**Parent Topic:**[Vaccination Status](../concept/vaccination-status.md)

## Components installed with Vaccination Status

Several types of components are installed with Vaccination Status, including user roles and tables.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see Find components installed with an application.

### Roles installed

<table id="table_u1t_gb1_wdb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Vaccination Status admin\[sn\_imt\_vaccine.admin\]

</td><td>

Application-specific admin for Vaccination Status.Can approve COVID-19 health test results in Health and Safety Testing. **Important:** By default, the System Administrator \[admin\] role contains the sn\_imt\_vaccine.admin role. The sn\_imt\_vaccine.admin role should be reassigned to another user and then removed from the admin. This process protects sensitive application data by restricting access to the application.

</td><td>

sn\_imt\_vaccine.profile\_reader

</td></tr><tr><td>

Vaccine profile reader\[sn\_imt\_vaccine.profile\_reader\]

</td><td>

Read-only access to the Vaccine profile \[sn\_imt\_vaccine\_vaccine\_profile\] table. Required to view vaccination status in contact tracing visualization.

</td><td>

None

</td></tr></tbody>
</table>### Tables installed

<table id="table_udb_2hn_2mb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Vaccine profile\[sn\_imt\_vaccine\_vaccine\_profile\]

</td><td>

Shows which users received a COVID-19 vaccine. Users are not considered fully vaccinated until 14 days after receiving their vaccination \(single-dose vaccine\) or their final dose \(multi-dose vaccine\).

 **Note:** The COVID-19 vaccine completed column has a value of **false** until the 14-day vaccination period is complete.

 Organizations can make the vaccine complete status dependent on whether a user reported receiving a vaccine booster when it became due. If the **\[sn\_imt\_vaccine.enforce\_vaccination\_complete\_for\_booster\]** property is enabled and a booster is due, the COVID-19 vaccine completed column has a value of **false** for users who have not reported receiving their booster after the due date.

</td></tr><tr><td>

Vaccine response\[sn\_imt\_vaccine\_vaccine\_response\]

</td><td>

Contains a history of all reported vaccination statuses for each user. Users can review their previously submitted vaccines in **My vaccinations**.

 Vaccine responses and their attachments are stored for the duration set by your organization's data retention policies. If the vaccine responses are deleted before the expiration date, the reported statuses and attachments are also deleted.

**Note:** Any historical data saved for use in the Vaccination Status dashboard is count data only. Any personally identifying information is removed by default and is deleted based on your organization's policy.

</td></tr><tr><td>

Vaccine response definition\[sn\_imt\_vaccine\_vaccine\_response\_definition\]

</td><td>

List of vaccines, including the type, manufacturer, and number of doses required. By default, this table contains several generic COVID-19 vaccines. A Vaccination Status admin can add and remove records to reflect the vaccines that are currently available to users.

</td></tr><tr><td>

Campus vaccine summary\[sn\_imt\_vaccine\_campus\_vaccine\_summary\]

</td><td>

Stores vaccination data to map against data provided by the COVID-19 Global Health Data Set in the Safe Workplace Dashboard Vaccination Widget. User vaccination data is pulled from the Vaccine response table and entries are created daily based at midnight \(00:00\) instance time.

</td></tr><tr><td>

Vaccine exemption requests\[sn\_imt\_vaccine\_vaccine\_exemption\]

</td><td>

Lists of vaccine exemption requests, their status, the exemption type, expiration date, and their status. Vaccine exemption requests without an expiration date do not expire. Vaccine exemption requests are inactive by default.

 Managers may view the exemption requests for their direct reports in **My Employee's exemptions** if this ability is enabled by their organization.

 For more information, see [Set up Vaccination Status properties](config-vaccination-properties.md).

</td></tr><tr><td>

Validator service\[sn\_imt\_vaccine\_validator\_service\]

</td><td>

Stores information for validator services, such as CommonTrust Network, used to verify submitted vaccine responses and their attachments.

</td></tr><tr><td>

Vaccine response attachment type\[sn\_imt\_vaccine\_vaccine\_response\_attachment\_type\]

</td><td>

List of attachment types available for users to specify the type of upload they are providing. For example, the SMART health card attachment type is used with the CommonTrust Network when performing validations.

</td></tr><tr><td>

Vaccine code systems\[sn\_imt\_vaccine\_vaccine\_code\_system\]

</td><td>

Lists common vaccine systems and standards used with vaccine codes to confirm the vaccine manufacturer of a user's submitted dose.

</td></tr><tr><td>

Vaccine codes\[sn\_imt\_vaccine\_vaccine\_code\]

</td><td>

Lists valid vaccine codes, such as CVX codes, obtained from the Center for Disease Control and Prevention \(CDC\) used to validate the manufacturer of a vaccine in a user's vaccine response. For a complete list of codes, see [COVID-19 Vaccine Related Codes](https://www.cdc.gov/vaccines/programs/iis/COVID-19-related-codes.html).**Note:** Vaccination Status provides some codes as part of the base system.

</td></tr></tbody>
</table>