---
title: Configuration Compliance imported data
description: The Configuration Compliance application imports policies, tests, authoritative sources, and test results from third-party integrations and stores them in modules for viewing.
locale: en-US
release: zurich
product: Configuration Compliance
classification: configuration-compliance
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 7
breadcrumb: [Explore, Configuration Compliance, Unified Security Exposure Management, Security Operations]
---

# Configuration Compliance imported data

The Configuration Compliance application imports policies, tests, authoritative sources, and test results from third-party integrations and stores them in modules for viewing.

**Note:** Starting with v14.9 of Configuration Compliance, the following terms have been renamed:

|Terminology prior to v14.9|Terminology v14.9 onwards|
|--------------------------|-------------------------|
|Test Result Group|Remediation Task|
|Group Rules|Remediation Task Rules|
|Policy|Test group|

## Supported integrations

Third-party integrations import configuration assessment findings, test groups, tests, technologies, authoritative sources, and test results into the Configuration Compliance application. Vulnerability managers or vulnerability analysts can use this data to identify and respond to the configuration-related vulnerabilities on your assets.

For more information about supported integrations, see [Configuration Compliance integrations](vuln-config-compl-integrations.md).

## Test groups

Test Groups are related to authoritative documents and test records. A group of configuration tests define Test Groups. Test Groups typically align to a technology class, for example, Windows, Oracle databases, Cisco IOS, and are often derived from the primary industry standard. Test Groups can be modified to meet the needs of the organization. A single Configuration Test can belong to multiple test groups.

<table id="simpletable_rpq_snp_kqb"><thead><tr><th>

Integration

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Qualys Vulnerability Integration

</td><td>

Test groups are retrieved and Control IDs are populated by the scheduled job, **Qualys PC Policies** at 1:00AM.You can view the scheduled job by navigating to **Qualys Vulnerability Integration** &gt; **Primary Integrations** &gt; **Qualys PC Policies**.

**Note:** If you choose to run the integration manually, run **Qualys PC Policies** first.

</td></tr><tr><td>

Tenable Vulnerability Integration

</td><td>

The scheduled job Tenable.io Compliance Results Integration imports policies. If you choose to run the integrations manually, run the integrations in the following order until you reconcile any ignored assets with assessment data:

-   Tenable.io Assets Integration
-   Tenable.io Compliance Results Integration
-   Tenable.io Compliance Results Backfill Integration
-   Tenable.io Assets Integration
-   Tenable.io Compliance Results Backfill Integration

 To view the policy record, navigate to **All** &gt; **Configuration Compliance** &gt; **Test Groups**.

 To correctly identify and create the test group records, audit information for test groups is imported and displayed in the **Short description** field.

</td></tr></tbody>
</table>## Tests

Tests are libraries of data records that organize scans of computing assets. Configuration tests define how a class of technology assets should be governed.

A Configuration Compliance test is the mechanism third-party integration applications use to group assets by vulnerability type. Some third-party VA scanning solutions such as Qualys have very large libraries of tests \(as many as 8,000\) that are mapped to policies and "frameworks" of authoritative sources.

A Test can have many values, one-to-many, expected vs. actual, and so on. A test is anything that can be used to identify a class of software or hardware asset that is out of compliance. For example, a release or hardware number.

<table id="table_att_3pp_kqb"><thead><tr><th>

Integration

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Qualys Vulnerability Integration

</td><td>

The scheduled job, **Qualys PC Controls**, retrieves the tests. You can view the scheduled job by navigating to **Qualys Vulnerability Integration** &gt; **Primary Integrations** &gt; **Qualys PC Controls**.**Note:** If you choose to run the integration manually, run **Qualys PC Controls** after **Qualys PC Policies**.

</td></tr><tr><td>

Tenable Vulnerability Integration

</td><td>

The scheduled job Tenable.io Compliance Results Integration imports configuration tests \(Tests\). If you choose to run the integrations manually, run the integrations in the following order until you reconcile any ignored assets with assessment data:

-   Tenable.io Assets Integration
-   Tenable.io Compliance Results Integration
-   Tenable.io Compliance Results Backfill Integration
-   Tenable.io Assets Integration
-   Tenable.io Compliance Results Backfill Integration

 To view the Configuration Test record, navigate to **Configuration Compliance** &gt; **Tests**. On the record, imported data is displayed in the **Short description** field and Remediation Status, Description, and Remediation tabs. Data is also displayed on the **Citations**, **Policies**, and **Test Results** Related Links.

</td></tr></tbody>
</table>## Technologies

One of the techniques used by third-party vulnerability scanners to create test groups of software and hardware configuration items for analysis is to organize them by technology. Technologies are an imported library of OSes, network devices, databases, and apps that are associated with policies. Tests have multiple implementations for different technologies. Remediation is technology-specific, as well.

You can [view the applicable technologies](../task/view-vlun-config-compl-technologies.md) for a test, to better understand what kinds of software or hardware assets the control can be applied to. Examples of technologies that can be applied to controls include CentOS 7.x, Windows 8.1, Windows 2016 Server, and so on. The list of technologies is read-only and match the technologies defined in the Qualys Cloud Platform application.

Technologies are imported for database-related configuration assessments only. The **db\_type** \(if not empty\) in the import is used to create a technology. View technologies populated on the Technologies section on configuration test records, test result records, policy records and at **Configuration Compliance** &gt; **Supporting Data** &gt; **Technologies**.

## Authoritative sources

Configuration Compliance uses Authoritative sources and citations when generating vulnerability alerts for tests. Authoritative sources usually map to sections of published industry standards, such as "NIST 800-53 version 3 \(2009\) 3: 2009, SA-4".

**Note:** In the Qualys Vulnerability Integration, this combination is referred to as framework.

Authoritative sources and citations \(also known as mandates\) are imported from the third-party vulnerability scanners.

Authoritative source records contain references to information about known software and hardware configuration issues from experts in the field of computer security. They define requirements for security policies and procedures. Configuration tests can reference multiple authoritative sources through citations. Authoritative sources can report on compliance for a given standard in preparation for an audit.

<table id="table_shz_rrn_4qb"><thead><tr><th>

Integration

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Qualys Vulnerability Integration

</td><td>

The scheduled job, **Qualys PC Policies Detail**, retrieves the authoritative sources and citations. You can view this scheduled job by navigating to **Qualys Vulnerability Integration** &gt; **Primary Integrations** &gt; **Qualys PC Policies Detail**.**Note:** If you choose to run the integration manually, run **Qualys PC Policies Detail** after **Qualys PC Policies**.

</td></tr><tr><td>

Tenable Vulnerability Integration

</td><td>

The scheduled job Tenable.io Compliance Results Integration imports authoritative sources as part of Citations data.If you choose to run the integrations manually, run the integrations in the following order until you reconcile any ignored assets with assessment data:

-   Tenable.io Assets Integration
-   Tenable.io Compliance Results Integration
-   Tenable.io Compliance Results Backfill Integration
-   Tenable.io Assets Integration
-   Tenable.io Compliance Results Backfill Integration

 Data is displayed on the **Citations** related link on configuration test records.

</td></tr></tbody>
</table>## Test results

Configuration Compliance does not calculate the test results, but imports them as part of a third-party integration. Once they are viewable in Configuration Compliance, they are remediated using **Remediation Tasks**. See [Configuration Compliance correlation](vuln-config-compl-correlation.md) for more information.

<table id="table_e5z_grp_kqb"><thead><tr><th>

Integration

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Qualys Vulnerability Integration

</td><td>

You can retrieve the test results in one of the following ways:

 The scheduled job, **Qualys PC Results**, retrieves the test results. You can view this scheduled job by navigating to **Qualys Vulnerability Integration** &gt; **Primary Integrations** &gt; **Qualys PC Results**.

 **Note:** If you choose to run the integration manually, run **Qualys PC Results** after **Qualys PC Policies** and **Qualys PC Policies Detail**.

 The **Qualys PC Results** import uses the **Start Time** parameter in the **Integration Details** tab. All other Configuration Compliance imports bring in all available data regardless of **Start Time**.

 When the **Qualys PC Results** import is complete, an event is fired to trigger end-of-import calculations. For more information see, [Configuration Compliance states](vuln-config-compl-states.md).

 Alternatively, starting from V14.5, you can also run the following integrations to retrieve the test results:

-   Qualys PCRS Policy Host Integration - Retrieves the host IDs for each policy. To view this scheduled job, navigate to: Qualys Vulnerability Integration &gt; Primary Integrations &gt; Qualys PCRS Policy Host Integration.

**Note:** If you choose to run the integration manually, run Qualys PCRS Policy Host Integration after Qualys PC Policies and Qualys PC Policies Detail.

After this scheduled job is complete, it automatically triggers the Qualys PCRS Test Results Integration.

-   Qualys PCRS Test Results Integration - Retrieves the test results for each host ID. To view this scheduled job, navigate to Qualys Vulnerability Integration &gt; Primary Integrations &gt; Qualys PCRS Test Results Integration.

**Note:** If you choose to run the integration manually, run Qualys PCRS Test Results Integration after Qualys PC Policies, Qualys PC Policies Detail and Qualys PCRS Policy Host Integration.

This integration uses the Start Time parameter in the Integration Details tab.


</td></tr><tr><td>

Tenable Vulnerability Integration

</td><td>

The scheduled job Tenable.io Compliance Results Integration imports Test Results. If you choose to run the integrations manually, run the integrations in the following order until you reconcile any ignored assets with assessment data:

-   Tenable.io Assets Integration
-   Tenable.io Compliance Results Integration
-   Tenable.io Compliance Results Backfill Integration
-   Tenable.io Assets Integration
-   Tenable.io Compliance Results Backfill Integration

 To view the Configuration Test record, navigate to **Configuration Compliance** &gt; **Tests Results**. On the record, imported data is displayed in the**Test**, and **Configuration Item** fields. Data is also displayed on the **Expected Values**, **Actual Values**, and **Remediation** tabs. The **Remediation Tasks** and **Test Result History** Related Links are populated.

</td></tr></tbody>
</table>