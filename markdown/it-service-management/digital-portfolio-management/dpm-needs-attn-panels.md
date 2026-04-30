---
title: Work with Needs attention panels in Digital Portfolio Management
description: Digital Portfolio Management \(DPM\) enables you to view items that need attention in the context of your solutions. Categories in each Needs attention panel differ based on the solution type. You may not act on an item that needs attention, but you can see its status and severity to make data-driven decisions about your solutions.
locale: en-US
release: yokohama
product: Digital Portfolio Management
classification: digital-portfolio-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 6
breadcrumb: [Work with solution data in Digital Portfolio Management, Digital Portfolio Management, IT Service Management]
---

# Work with Needs attention panels in Digital Portfolio Management

Digital Portfolio Management \(DPM\) enables you to view items that need attention in the context of your solutions. Categories in each Needs attention panel differ based on the solution type. You may not act on an item that needs attention, but you can see its status and severity to make data-driven decisions about your solutions.

Each DPM Workspace page has a Needs attention panel that presents items that need attention in the context of the page. You can search items that need attention on the DPM home page but it's more useful to search while viewing a portfolio or a solution.

**Important:** This topic applies to Standard Needs attention panels.

Standard Needs attention panels were introduced in the Utah release \(May 2023\). The Standard version is more flexible than its legacy counterpart. The Standard system property is set to true by default. Existing customers can set it to false to return to the former Needs attention functionality. There isn't a limit to changing the value from true to false \(and back\). New customers can't set the system property to false, so they only see the Standard version.

## Standard Needs attention panels system property

Admins update the system property with the DPM admin \[sn\_dpm.dpm\_admin\] role.

-   Navigate to **All** &gt; **Digital Portfolio Management** &gt; **Administration** &gt; **Settings**.
-   Enter `*needs` in the **System Properties Name** search field, and then press **Enter**.
-   Select the system property \[sn\_dpm.standard\_needs\_attention\].
-   Release the record to edit it, and then set the property to false or true.
-   Select **Update**.

## Problems option in the Needs attention panel

To see problems in the Needs attention panel, you must be using the DPM August 2024 release or a later release.

You can identify problems on the following solutions.

-   Services and service offerings. Problems are related to the service offering via the service offering record on the form, impacted services related list, and on the affected CIs related list. Problems are then rolled up to the parent service and should be deduplicated at the parent service level.
-   Business applications. Problems are related to the application service via the configuration item field on the form. Problems are then rolled up from the application service to the business application and should be deduplicated at the parent service level.
-   Application services. Problems are related to the application service via the configuration item field on the form.

## Application service considerations

Prior to the November 2024 Store release, you could see the records of incidents, problems, and changes in the Needs attention panel only if the application service is added to the Configuration item field of a related item \(for example, to an incident record\).

As of the November 2024 Store release, items or records are reflected in the Needs attention panel when an incident, problem, or change includes the application service in the Impacted services or the Affected CIs related list, in addition to the Configuration item field.

After the application services are added to the Configuration item field, Impacted services, or the Affected CIs related list, you can see them under the Needs attention section in the base level \(application service\). The data also rolls up to the following levels in the DPM Workspace:

-   Business application
-   Taxonomy node
-   Portfolio

Also, after the application services are added, the data is rolled up in the following areas when you:

-   Select **View details** on any affected solution page.
-   View the Run tab of any solution page to view the key performance indicators \(KPIs\).

This functionality applies to enterprise business application portfolios, enterprise application service portfolios, and to any business application or application service added to your personal portfolios.

## Panel attributes and icons

Even though the Needs attention panel categories differ for each portfolio and solution, the basic navigation is the same. All panels enable you to search, see a list of Needs attention cards, paginate through the cards, and drill down to a record from the card list.

![Needs attention panel example.](../image/dpm-needs-attn-example-app-service.png "Needs attention panel example using an application service")

-   Each Needs attention category includes a number that indicates the number of items in that category. If there are no Needs attention items in a category, then the number is zero \(0\).
-   Select the forward arrow \(&gt;\) next to a number in the category to see a list of record cards that need attention. From the card list, you can select a card to access its record. You can also go back by selecting the Needs attention back arrow \(&lt;\).
-   The Needs attention **Search** field enables you to enter a number, a part of a word, or a whole word to find Needs attention items that contain your search criteria. After you view and open a record that needs attention, you can return to the **Search** field. Your search criteria remain in the **Search** field until you clear the field.

    The following table shows the Needs attention panel icons that display for each solution type.

<table id="table_c5g_2nq_cbc"><thead><tr><th>

Solution type

</th><th>

Needs attention panel icons

</th></tr></thead><tbody><tr><td>

Services and service offerings

</td><td>

-   Needs attention icon \(![Needs attention icon](../../../administer/on-call-scheduling/image/icon-information.png)\) to show or hide the Needs attention panels. This toggle isn't on the DPM Workspace home page.
-   Contacts icon \(![Contacts icon.](../image/contacts.png)\) to view team members and the all the teams that support the service offering.
-   Knowledge articles icon\(![Knowledge articles icon.](../image/dpm-kb-icon.png)\) to search for related knowledge articles.
-   Attachments icon \(![Attachments icon.](../image/attachment.png)\) to view and add attachments to the record.
-   Catalog items icon \(![Catalog items icon.](../image/catalog-items.png)\) to search for catalog items on a service or service offering record.


</td></tr><tr><td>

Business applications and application services

</td><td>

-   Needs attention icon \(![Needs attention icon](../../../administer/on-call-scheduling/image/icon-information.png)\) to show or hide the Needs attention panels. This toggle isn't on the DPM Workspace home page.
-   Contacts icon \(![Contacts icon.](../image/contacts.png)\) to view team members and all the teams that support the business application or the application service.
-   Attachments icon \(![Attachments icon.](../image/attachment.png)\) to view and add attachments to the record.


</td></tr></tbody>
</table>
## Service considerations

-   A record is linked to the offering and rolled up to the service. You can see incidents, outages, and changes when the incident is linked directly to the service \(not to the offering\).
-   An incident, outage, or change can impact multiple offerings.
-   A record is first displayed on the offering, and then it's rolled up to the parent service.
-   An incident displays once \(not twice\) if two offerings are added to an incident and they roll up to the same service.

## Service offering considerations

Critical incidents, outages, and changes are linked to the offering to display in the Needs attention panel when the offering is:

-   Listed in the service offering field on the incident record or the change record.
-   Included in the affected services or the affected CI related lists, or both.
-   Rolled up to the parent service level when an incident or change is related to an offering \(via a related list or directly on the form\).

**Note:** By default, you see critical incidents. To see critical and major incidents, the Major Incident Management plugin \(com.snc.incident.mim\) must be installed.

## Panel options for each DPM solution

Records included on each DPM solution page are the ones created "today."

<table id="table_mh3_4gl_rwb"><thead><tr><th>

Services and service offerings

</th><th>

Application services

</th><th>

Business applications

</th></tr></thead><tbody><tr><td>

-   Critical and major incidents
-   Outages
-   Changes

 For new and zBoot customers, all the above plus Audit and Risks.

</td><td>

-   Critical and major incidents
-   Outages
-   Changes
-   Alerts
-   Risks

 For new and zBoot customers, all the above plus Audits.

</td><td>

-   Critical and major incidents
-   Changes
-   Risks
-   Audits

</td></tr><tr><td colspan="3">

**Note:**

To see Risk data, you must have the Technology Portfolio Management plugin installed \[sn\_apm\_tpm\]. This plugin has two dependency plugins:

-   Application Portfolio Management \[com.snc.apn\]
-   Software Asset Management \[com.snc.sams\]

</td></tr></tbody>
</table>**Parent Topic:**[Work with solution data in Digital Portfolio Management](../reference/dpm-working-with.md)

**Related topics**  


[Configure Needs attention panels in Digital Portfolio Management](../task/dpm-configure-needs-attention.md)

