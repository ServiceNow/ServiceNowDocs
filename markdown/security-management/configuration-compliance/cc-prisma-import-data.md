---
title: Data mapping
description: The data from Prisma Cloud is imported in the Configuration Compliance module of the ServiceNow instance.
locale: en-US
release: xanadu
product: Configuration Compliance
classification: configuration-compliance
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Understanding the Vulnerability Response Integration with Palo Alto Prisma Cloud, Configuration Compliance integrations, Configuration Compliance, Unified Security Exposure Management, Security Operations]
---

# Data mapping

The data from Prisma Cloud is imported in the Configuration Compliance module of the ServiceNow instance.

**Note:** Starting with v14.9 of Configuration Compliance, the following terms have been renamed:

|Terminology prior to v14.9|Terminology v14.9 onwards|
|--------------------------|-------------------------|
|Test Result Group|Remediation Task|
|Group Rules|Remediation Task Rules|
|Policy|Test group|

The data from Prisma Cloud is imported with a different name in Configuration Compliance as mentioned in the table.

|Prisma Cloud|Configuration Compliance|
|------------|------------------------|
|Policy|Test|
|Alert|Test result|
|Compliance standard|Authoritative source|
|Sections|Citation|
|Asset|Discovery item/ Configuration item \(CI\)|

## Tests

A policy in Prisma Cloud is imported as a test in Configuration Compliance. Policies are related to authoritative documents and test records, and they can be modified to meet the needs of your organization. You can view the tests by navigating to **Configuration Compliance** &gt; **Tests**.

If **Vulnerability Response Integration with Palo Alto Prisma Cloud** is installed, the integration job, **Prisma Policy Integration** retrieves the tests. You can view this integration job by navigating to **All** &gt; **Prisma Cloud Integrations** &gt; **Prisma Policy Integration**.

## Test Results

An alert in Prisma Cloud is imported as a test result in Configuration Compliance. Alerts are remediated using **Remediation Tasks**. You can view the test results by navigating to **Configuration Compliance** &gt; **Test Results**.

The Configuration Compliance imports test results as part of a third-party integration. After they’re viewable on the Configuration Compliance application, they are remediated using Remediation Tasks.

If **Vulnerability Response Integration with Palo Alto Prisma Cloud** is installed, the integration job **Prisma Alert Integration** retrieves the test results. You can view this integration job by navigating to **All** &gt; **Prisma Cloud Integration** &gt; **Integrations** &gt; **Prisma Alert Integration**.

The **Prisma Alert Integration** is an integration job that runs daily and pulls the test results with status change after the time that is defined in the **Start Time** field in the **Integration** tab.

**Note:** If you run the integration job, **Prisma Alert Integration** manually, run it after you run the integration job, **Prisma Policy Integration**.

When the **Prisma Alert Integration** completes importing the data, an event is started to trigger end-of-import calculations. If the alert fails continuously for the past few days, the integration won’t fetch the alerts as there’s no status change for the alert. So, to keep the test results data up to date with the Prisma alerts, a new integration job, **Prisma Comprehensive alert Integration** is added which pulls the alerts that are updated in the past seven days. It runs weekly and pulls all the test results, which aren’t passed.

## Authoritative Sources

Configuration Compliance uses authoritative sources and citations when generating vulnerability alerts for tests. Authoritative sources usually map to sections of published industry standards, such as ISO 27001 and PCI DSS 3.2.1.

These source records contain references to information about known software and hardware configuration issues from experts in the field of computer security. The references define requirements for security policies and procedures. Navigate to **Configuration Compliance** &gt; **Authoritative Sources** to view the authoritative sources.

## Assets

If the Vulnerability Response Integration with Palo Alto Prisma Cloud is installed, the scheduled job **Prisma Alerts Integration** captures the alert related information in the Discovered Items module or table. You can view this scheduled job by navigating to **Prisma Cloud Integration** &gt; **Integrations**.

The Prisma Alerts integration imports additional types of information, such as resource tags and cloud attributes that are stored in tables. This information is displayed in the Discovered items form.  

-   Host tags: A resource can have multiple tags. The host tags are available in key value pair format. For example, the operating system is Windows 10 and the Java version is 1.8.
-   Cloud attributes for assets: The following cloud attributes are available:
    -   Cloud account: Provides the account ID from the integration. The information is populated from the Cloud Accounts \[sn\_sec\_cmn\_cloud\_account.LIST\] table.
    -   Cloud region: Provides the location where the resource has been hosted. The information is populated from the Cloud Regions \[sn\_sec\_cmn\_region.LIST\] table.
    -   Cloud resource type: Provides information on the type of resource such as whether it is a virtual machine or a database instance, and so on. The information is populated from the Cloud Resource Type \[sn\_sec\_cmn\_cloud\_resource\_type.LIST\] table.
    -   Cloud service provider: Provides information on the cloud service provider whether it’s Amazon Web Services \(AWS\), Oracle Cloud, and so on. The information is populated from the Cloud Service Provider \[sn\_sec\_cmn\_cloud\_service\_provider.LIST\] table.
    -   Cloud account groups: Provides information on the account groups. The information is populated from the Cloud Account Groups \[sn\_vul\_prismacloud\_account\_group.list\] table.

        **Note:** The Cloud account groups attribute is available only for Prisma.


## CI lookup rules

The base system CI lookup rules are available for Resource ID, Name, and S3 Bucket. For more information on the CI lookup rules, see [CI lookup rules for Microsoft Defender for Cloud Integration for Security Operations and Palo Alto Prisma Cloud](../../../vulnerability-config-compliance/reference/cloud-ci-look-up-for-ms-paloalto.md).

**Parent Topic:**[Understanding the Vulnerability Response Integration with Palo Alto Prisma Cloud](prisma-cloud-overview.md)

