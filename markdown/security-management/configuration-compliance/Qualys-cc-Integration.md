---
title: Qualys integration with Configuration Compliance
description: The Qualys Policy Compliance collects the data and automatically sends it to the Qualys application, which continuously analyzes and correlates the information. It easily integrates as the Qualys Integration for Security Operations to map configuration findings to CIs and business services to determine the impact and priority of potential misconfigurations.
locale: en-US
release: zurich
product: Configuration Compliance
classification: configuration-compliance
topic_type: concept
last_updated: "2025-12-04"
reading_time_minutes: 3
breadcrumb: [Integrate, Configuration Compliance, Unified Security Exposure Management, Security Operations]
---

# Qualys integration with Configuration Compliance

The Qualys Policy Compliance collects the data and automatically sends it to the Qualys application, which continuously analyzes and correlates the information. It easily integrates as the Qualys Integration for Security Operations to map configuration findings to CIs and business services to determine the impact and priority of potential misconfigurations.

If you have multiple deployments of the Qualys Cloud Platform application, you can add an integration for each deployment. Assets, identified by multiple third-party deployments and their vulnerabilities, are consolidated and reconciled with your CMDB. This consolidation happens even when scan processes overlap between the multiple deployments. Data sourced from each deployment is identified and available in a single instance of Vulnerability Response.

**Note:** You cannot delete the original vulnerability integration, but you can disable it. Integrations created from inactive templates are disabled by default.

## Host tags

All host tags are imported as part of the Qualys Host List integration. Host tags are used primarily for filtering in Vulnerability Response Assignment and Remediation Task Rules. They are displayed in the Discovered Item form.

**Note:** The Qualys Host List integration should be run prior to creating the Assignment or Remediation Task Rules in Vulnerability Response so that all tags can be present in the rules and before vulnerable items are imported and grouped.

-   Tag storage is not case-sensitive. If a **San Diego** tag is created, then a **SAN DIEGO** tag cannot be stored in the Host tag table. “San Diego” and “SAN DIEGO” are considered to be the same host tag. Whichever tag was imported first wins.
-   Using host tags as a Group Key in a Remediation Task Rule can have unexpected results. Host tags are intended for use only in the condition builder.
-   Host tags are controlled by the global system property **sn\_vul.import\_host\_tags**. This property is set to true by default. Turning off tags turns them off across all instances.

Host tags \(also called asset tags\) are used for organizing and tracking the assets in your organization. You can assign tags to your host assets. Then, when launching scans, you can select tags associated with the hosts you want to scan. The Host Tags module enables you to download host tag data from Qualys to your instance on a scheduled basis.

## Associating a Test with its Test Group

To populate the Test group field on a Test form, enable the **sn\_vulc.add\_policy\_as\_key** system property. For more information on how a test is associated to its test group, impact of enabling this system property and post-requisites, see [KB1644268](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1644268) article.

**Warning:** You cannot disable the **sn\_vulc.add\_policy\_as\_key** system property once it is enabled. So, review the Impact section in the [KB1644268](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1644268) article before you enable this system property.

When you enable this system property, after the next ingestion, the **Test group** field is added on the Test table and it populates the test group to which a test belongs to. Therefore, you can easily:

-   identify the Test Group to which a Test Result belongs to by dot-walking from Test to Test Group.
-   differentiate Test records with same Test id that are associated with different Test Groups.

## Integrating Qualys with the ServiceNow® Configuration Compliance application

Ignore passed test results

Starting with v15.2.5 of Configuration Compliance, the ignore\_passed\_result integration instance parameter for the Qualys Integration for Security Operations has been added.This parameter is set to `false` by default so that passed test results imported by Qualys are not ignored.

-   Set the parameter to `true` to ignore passed test results on import.
-   If activated, this parameter does not impact the closure of the test results.

    For example, if you activate the parameter, and a failed test result from a previous import has since passed, it will be closed correctly.


API credentials

If the Qualys Vulnerability Integration is already installed on your system, and your API credentials are different than the ones you want to use for Configuration Compliance, go into Setup Assistant \(in Vulnerability Response\) and assign them to each **Qualys PC** integration.

Navigate to **All** &gt; **Qualys Vulnerability Integration** &gt; **Primary Integrations** and edit the **Qualys API Credentials** field under the **Qualys REST Details** tab.

