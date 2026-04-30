---
title: Operational Technology Progress Scorecard
description: The Operational Technology \(OT\) Progress Scorecard lets you compare device and vulnerable item data between your sites.
locale: en-US
release: xanadu
product: Industrial Workspace
classification: industrial-workspace
topic_type: concept
last_updated: "2025-08-06"
reading_time_minutes: 3
breadcrumb: [Explore, Industrial Workspace, Operational Technology]
---

# Operational Technology Progress Scorecard

The Operational Technology \(OT\) Progress Scorecard lets you compare device and vulnerable item data between your sites.

## OT Progress Scorecard overview

The OT Progress Scorecard is a centralized location in the Industrial Workspace that lets you compare your site data. Site data includes both OT device data and vulnerability data. With the OT Progress Scorecard, you can track site progress and determine the sites that need attention.

You can also view the site data for the following Operational Technology applications:

-   Operational Technology Manager
-   Operational Technology Vulnerability Response
-   Operational Technology Incident Management
-   Operational Technology Change Management

You can configure the OT Progress Scorecard using the Industrial Workspace Admin Guided Setup. For more information about the setup tasks, see [Setting up the Operational Technology Progress Scorecard](setting-up-the-ot-progress-scorecard.md).

## Scorecard contents

To access the OT Progress Scorecard, navigate to **All** &gt; **Industrial Workspace** and select the **OT Progress Scorecard** \(![OT Progress Scorecard icon](../image/ot-progress-scorecard-icon.png)\) icon.

The following table describes columns in the OT Progress Scorecard.

<table id="table_tlm_fmw_qbc"><thead><tr><th>

Column

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Overall Score \(%\)

</td><td>

The progress of your site determined by the indicators on the scorecard. You can edit the weightage to control how much an indicator contributes to the overall score. For more information, see [Set the system properties for the Operational Technology Progress Scorecard](../task/set-the-system-properties-for-ot-progress-scorecard.md).

</td></tr><tr><td>

% of Expected OT Devices in CMDB

</td><td>

The percentage of your OT devices that you expect to have in the Configuration Management Database \(CMDB\).**Note:** If you see a value of -1, then one or more of the values in the % of Expected OT Devices in CMDB indicator is missing the **Expected OT Device** attribute in the OTPSC Attributes table. For information about how to configure expected OT devices see [Configure the expected OT devices for a site](../task/configure-expected-ot-devices.md).

</td></tr><tr><td>

Classified OT Devices \(%\)

</td><td>

The percentage of classed OT devices. Classified OT Devices \(%\) doesn’t include OT devices classed as cmdb\_ci\_ot.

</td></tr><tr><td>

Assigned OT Devices \(%\)

</td><td>

The percentage of OT devices with values in the following fields:-   Assigned to
-   Owned by
-   Managed by
-   Supported by
-   Approval group
-   Managed group
-   Support by
-   Change group

</td></tr><tr><td>

OT Device Data Completeness \(%\)

</td><td>

The percentage of OT devices that meet your data goals. This metric depends on the CMDB Health Dashboard - Completeness Score Calculation job and you must set the required &amp; recommended fields on the CI Class Manager. For more information, see [Set up and configure CMDB Health](https://www.servicenow.com/docs/access?context=c_CMDBHealthSetupandConfig&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).Completeness is a KPI determined by the following metrics:

-   **Required**

Measures the percentage of CIs in which fields that are defined as required, aren't populated. Missing fields are tagged as incomplete noting that for this CI some information is missing.

-   **Recommended**

Measures the percentage of CIs in which fields that are set as recommended, aren't populated.


For more information about data completeness, see [CMDB Health KPIs and metrics](https://www.servicenow.com/docs/access?context=r_CMDBHealthMetrics&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)

**Note:** If you see a value of -1, then the CMDB Health Dashboard - Completeness Score Calculation job hasn't been run yet. Or the job has been run with an incomplete status.

</td></tr><tr><td>

Mapped OT Devices \(%\)

</td><td>

The percentage of OT devices mapped to an equipment model entity.**Note:** If you see a value of 0, then no OT devices have been found.

</td></tr><tr><td>

Backed up OT Devices \(%\)

</td><td>

The percentage of OT devices with backup records created.**Note:** If you see a value of 0, then no OT devices have been found.

</td></tr><tr><td>

Assigned OT Vulnerable Items \(%\)

</td><td>

The percentage of OT vulnerable items that aren't closed and addressed.**Note:** If you see a value of 0, then no OT devices have been found.

</td></tr><tr><td>

Approved OT Change Requests \(%\)

</td><td>

The percentage of OT change requests that are submitted and approved.**Note:** If you see a value of 0, then no OT devices have been found.

</td></tr><tr><td>

OT Incidents with OT Context \(%\)

</td><td>

The percentage of OT incidents that have OT device or equipment model data.**Note:** If you see a value of 0, then no OT devices have been found.

</td></tr></tbody>
</table>**Parent Topic:**[Exploring the Industrial Workspace](exploring-industrial-workspace.md)

