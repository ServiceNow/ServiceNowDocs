---
title: Components installed with the Qualys Integration for Security Operations
description: The following roles, scheduled jobs, and tables are installed with the Qualys Integration for Security Operations.
locale: en-US
release: yokohama
product: Configuration Compliance
classification: configuration-compliance
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Configure PCRS, Qualys, Integrate, Configuration Compliance, Unified Security Exposure Management, Security Operations]
---

# Components installed with the Qualys Integration for Security Operations

The following roles, scheduled jobs, and tables are installed with the Qualys Integration for Security Operations.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see [Find components installed with an application](https://www.servicenow.com/docs/access?context=find-components&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

## View filtered lists for components installed with an application

Filter the Applications Files table so that only the roles, scheduled jobs, and tables that are installed with an application are displayed. The application you want to view these components for should be installed so that its files are loaded onto the instance and into the metadata table. Follow these steps to view filtered lists from the Applications Files table.

1.  In the filter navigator, enter **sys\_metadata.list** to navigate to the metadata table.
2.  Select the condition builder \(filter icon\), and select, **Application** &gt; **is** followed by the name of your application. For example, **Application** &gt; **is** &gt; **Vulnerability Response**.
3.  In the condition builder, to add a second filter, select **AND**, then select, **Class** &gt; **is a** and choose one of the following classes from the list: **Role**, **Scheduled job**, or **Table**.
4.  Select **Run**.

The results for the class you selected are displayed in a filtered list.

## Roles installed

<table id="table_smw_gty_dvb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

sn\_vul\_qualys.read

</td><td>

Has read access to the Qualys Vulnerability Integration records.

</td><td>

 

</td></tr><tr><td>

sn\_vul\_qualys.user

</td><td>

User for Qualys Vulnerability Integration. Can read and write records

</td><td>

sn\_vul\_qualys.read

</td></tr><tr><td>

sn\_vul\_qualys.admin

</td><td>

Administrator forQualys Vulnerability Integration. For example, you can modify integration start dates and perform some advanced configuration settings.

</td><td>

-   sn\_vul\_qualys.user
-   sn\_vul.vulnerability\_analyst

</td></tr><tr><td>

sn\_vul.configure\_qualys\_integration

</td><td>

Can configure the Qualys Vulnerability Integration

</td><td>

sn\_vul\_qualys.admin

</td></tr></tbody>
</table>## Scheduled jobs installed

<table id="table_xqx_lty_dvb"><thead><tr><th>

Scheduled job

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Qualys PC Policies

</td><td>

Retrieves Policies from Qualys. The output is stored in the sn\_vulc\_policy table. The API used in this integration does not support pagination, so all policies are downloaded on a single page.

</td></tr><tr><td>

Qualys PC Policies Detail

</td><td>

Retrieves the complete policy details, such as technologies and sections, for example.

</td></tr><tr><td>

Qualys PC Controls

</td><td>

Retrieves compliance controls information for different control IDs from Qualys.

</td></tr><tr><td>

Qualys PC Results

</td><td>

Retrieves compliance posture records from Qualys. The output of this integration is Test Results. By default, the parameter details are passed to import host information, last scan dates/times, control ID, and evidence information.

</td></tr><tr><td>

Qualys PC Comprehensive Results

</td><td>

Retrieves compliance posture records from Qualys based on the last evaluation date for the test results that are not passed. This job runs once a week.

 The output of this integration is test results. By default, the parameter details are passed to import the host information, last scan dates/times, control ID, and evidence information.

</td></tr><tr><td>

Qualys PCRS Policy Host Integration

</td><td>

Retrieves host data from Qualys and processes it in your instance.When `posture_api_version` is set to 5.0, this integration uses the Start Time value as the StatusChangedSince parameter while fetching data.

The output of this integration is policy host IDs.

 The Qualys host data is imported in this integration.

**Note:**

-   This scheduled job appears only when Configuration Compliance is installed.
-   Configure the gateway\_url and pcrs\_page\_size integration instance parameters before running this integration.

These two integrations will be inactive OOB. If you activate either one of these integrations, the PC Results integrations will get deactivated. These two integrations are added based on the new streaming APIs from Qualys.

</td></tr><tr><td>

Qualys PCRS Test Results Integration

</td><td>

Retrieves the test results for each host ID. This integration uses the Start Time parameter in the Integration Details tab.**Note:**

-   This scheduled job appears only when Configuration Compliance is installed.
-   Configure the gateway\_url and pcrs\_page\_size integration instance parameters before running this integration.
-   If you choose to run the integration manually, run Qualys PCRS Test Results Integration after Qualys PC Policies, Qualys PC Policies Detail and Qualys PCRS Policy Host Integration.

</td></tr><tr><td>

Qualys Comprehensive PCRS Policy Host Integration

</td><td>

Retrieves host data from Qualys and processes it in your instance. The output of this integration is policy host IDs.**Note:**

-   This scheduled job appears only when Configuration Compliance is installed.
-   Configure the gateway\_url and pcrs\_page\_size integration instance parameters before running this integration.
-   This integration is inactive out of the box. When you set `posture_api_version` to 5.0, activate this integration if the corresponding Qualys PCRS Policy Host Integration is also active.

</td></tr><tr><td>

Qualys Comprehensive PCRS Test Results Integration

</td><td>

Retrieves test results for each host ID. This integration uses the Start Time parameter in the Integration Details tab.**Note:**

-   This scheduled job appears only when Configuration Compliance is installed.
-   Configure the gateway\_url and pcrs\_page\_size integration instance parameters before running this integration.
-   If you run the integration manually, run Qualys PCRS Test Results Integration after Qualys PC Policies, Qualys PC Policies Detail, and Qualys PCRS Policy Host Integration

</td></tr></tbody>
</table>**Note:** The Qualys PCRS Policy Host and Qualys PCRS Test Results integrations are inactive by default. These two integrations are based on the new streaming APIs from Qualys. If you activate any one of these integrations, the PC Results integration will be deactivated and vice versa.

## Tables installed

<table id="table_thd_432_4xb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Qualys PC Result Importsn\_vul\_qualys\_pc\_result\_import

</td><td>

Table extending the import set row. Field maps transformation is skipped and the response attachment is processed directly with the onComplete script.

</td></tr><tr><td>

Policy Host Idsn\_vul\_qualys\_policy\_host\_id

</td><td>

Table storing the mapping between the Policy and the host for which this policy was scanned. This table is used in the new Qualys PCRS integration.**Note:** This table is appears only when Configuration Compliance is installed.

</td></tr><tr><td>

Qualys PCRS Policy Host Importsn\_vul\_qualys\_pcrs\_policy\_host\_import

</td><td>

Table extending the import set row. Field map transformation is skipped and the response attachment is processed directly with the onComplete script.**Note:** This table appears only when Configuration Compliance is installed.

</td></tr><tr><td>

Qualys PC Policy Importsn\_vul\_qualys\_pc\_policy\_import

</td><td>

Table extending the import set row. Field map transformation is skipped and the response attachment is processed directly with the onComplete script.

</td></tr></tbody>
</table>