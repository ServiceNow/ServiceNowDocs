---
title: View availability results in Service Portfolio Management
description: View availability calculations for commitments on service offerings and application services. After the commitments are set up in Service Portfolio Management, you can view the results by an automated report that you set up.
locale: en-US
release: australia
product: Service Portfolio Management
classification: service-portfolio-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Use, Service Portfolio Management, IT Service Management]
---

# View availability results in Service Portfolio Management

View availability calculations for commitments on service offerings and application services. After the commitments are set up in Service Portfolio Management, you can view the results by an automated report that you set up.

After an availability commitment is added to a service offering or to an application service, Service Portfolio Management generates a year of availability records for that item and commitment, starting from the previous year. Service availability is based on the availability of the offerings, rolled up to the service. If an outage is updated, then the related availability records are updated as well so you can assess outage impacts and manage outage records.

Service Portfolio Management runs a daily job to generate the commitment availability reports and uses the system time zone.

For information on adding availability commitments, see [Add a commitment to a service offering](../task/define-SPM2-service-commitments.md).

## Availability calculator

Starting with the Australia release, you can use an availability calculator **\[com.snc.availability.v2\]** for improved performance, calculations, and maintenance.

The availability calculator is redesigned from its predecessor to ensure that you see the most updated and accurate availability data in the period that you want.

Service Portfolio Management creates availability records on the first of the period so you can see the availability as the period progresses. This real-time data is especially valuable when you’ve committed to a specific level of availability for your customers.

Also, the improved calculator updates the record as outages are created. For example, you can start off with 100% availability, and then when an outage happens, it updates to 99.95% based on the outage duration. You and your customers can rely on accurate availability data during outages, without repeated outage recalculations with no end date \(as with the previous calculator\).

Here are the availability period options that you can choose from when using the updated availability calculator:

-   Daily
-   Weekly
-   Monthly
-   Annually
-   Last 7 Days
-   Last 30 Days
-   Last 12 Months

New customers automatically get the updated availability calculator, but existing customers must set the property to 'true' to opt in.

To set the updated system property to 'true,' admins must do the following:

-   Type `sys_properties.list` in the Filter navigator, and then press **Enter**.
-   Select the **for text** search option.
-   Type **availability** in the **Search** field, and then press **Enter**.
-   Find the **\[com.snc.availability.v2\]** option, and then set its value to true.

## Availability reporting for application services

To view availability reporting for application services, you must create and map availability commitments to an application service using the **\[cmdb\_ci\_service\_auto table\]**.

In the **\[cmdb\_ci\_service\_auto table\]**, use the **cmdb\_ci** field in the **service\_offering\_commitment** field to associate an application service to an availability commitment.

## Generate availability results

To view availability results, navigate to **All** &gt; **Service Portfolio Management** &gt; **Availability**, and then select the related record from the list.

<table id="table_rzf_qk3_rtb"><thead><tr><th>

Field

</th><th>

Description

</th><th>

Calculations

</th></tr></thead><tbody><tr><td>

Display name

</td><td>

Name of the configuration item \(CI\) and the availability for the commitment. You can't edit this field.

</td><td>

Not applicable.

</td></tr><tr><td>

Service offering

</td><td>

The affected offering for this availability.

</td><td>

Not applicable.

</td></tr><tr><td>

Service commitment

</td><td>

The affected commitment for this availability.

</td><td>

Not applicable.

</td></tr><tr><td>

Start

</td><td>

Start of the availability interval. Mouse device pointing over this field displays the duration.

</td><td>

Not applicable.

</td></tr><tr><td>

End

</td><td>

End of the availability interval. Mouse device pointing over this field displays the duration.

</td><td>

Not applicable.

</td></tr><tr><td>

Committed uptime

</td><td>

Total expected service availability for this commitment, given in days, hours, minutes, and seconds.

</td><td>

Period end to period start.

</td></tr><tr><td>

Acceptable downtime

</td><td>

Acceptable amount of downtime against the commitment's schedule for this interval, given in days, hours, minutes, and seconds.

</td><td>

Scheduled period end to scheduled period start, multiplied by commitment percentage.

</td></tr><tr><td>

Total downtime

</td><td>

Wall clock downtime \(independent of the schedule\), given in days, hours minutes, and seconds.

</td><td>

Outage end to outage start.

</td></tr><tr><td>

Total availability %

</td><td>

Availability percentage for the entire interval \(independent of the schedule\).

</td><td>

\(Available uptime minus the total downtime\) divided by the available uptime.

</td></tr><tr><td>

Total outages

</td><td>

Total number of outage periods in this interval \(independent of the schedule\).

 **Note:** If an unplanned outage \(in full or in part\) overlaps with a planned outage, then the unplanned outage time that overlaps doesn't count toward the total outage time. This logic applies to the CI and affected CIs on the outage record.

</td><td>

Number of outages.

</td></tr><tr><td>

Commitment availability %

</td><td>

Availability within this commitment’s schedule.

</td><td>

\(Committed uptime minus commitment downtime\) divided by the committed uptime.

</td></tr><tr><td>

Commitment downtime

</td><td>

Downtime that counts against this commitment’s schedule, given in days, hours, minutes, and seconds.

</td><td>

\(Outage start minus outage end\) in scheduled up time.

</td></tr><tr><td>

Commitment outages

</td><td>

Number of outage periods against this commitment’s schedule in this interval.

</td><td>

Number of outages in scheduled uptime.

</td></tr><tr><td>

Met commitment

</td><td>

When checked, indicates that the availability commitment has been met.

</td><td>

True or false depending on if commitment availability percentage is higher than the service commitment.

</td></tr><tr><td>

Mean time between failures \(MTBF\)

</td><td>

Average time between commitment outages for a CI.

</td><td>

Basic formula: Total uptime in period divided by the number of outages in period \(Commitment outage periods\), where total uptime in period = \(Committed uptime minus Committed downtime\).

</td></tr><tr><td>

Mean time to restore service \(MTRS\)

</td><td>

Average duration of commitment outages for a CI.

</td><td>

Basic formula: Total duration \(Commitment downtime\) divided by the number of outages in period \(Commitment outage periods\).

</td></tr><tr><td colspan="3">

**Note:** For more information about calculations for MTBF and MTRS, see [KB1505841](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1505841).

</td></tr></tbody>
</table>## Archival rules for better performance

Starting with the Vancouver release, archival rules are activated by default. Service Portfolio Management uses a scheduled job called table cleaner to archive older records from tables in the instance to keep table sizes and query performance manageable. To ensure you get quicker data results, Service Portfolio Management uses the table cleaner job to archive availability data that is older than three years.

**Parent Topic:**[Using Service Portfolio Management](SPM2-using.md)

