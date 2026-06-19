---
title: Using CrowdStrike Falcon Insight integration in Analyst Workspace
description: Use the CrowdStrike Falcon Insight integration to leverage the CrowdStrike Falcon Insight capabilities on the SIR Analyst workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/security-incident-response/using-crowdstrike-falcon-host-integration-aws.html
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [CrowdStrike Falcon Insight integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Using CrowdStrike Falcon Insight integration in Analyst Workspace

Use the CrowdStrike Falcon Insight integration to leverage the CrowdStrike Falcon Insight capabilities on the SIR Analyst workspace.

## Before you begin

Role required: sn\_si.admin

Before you use CrowdStrike Falcon Insight integration on the Security Incident Response workspace, you must download it from the ServiceNow Store and configure it. For more information, see [Getting started with the CrowdStrike Falcon Insight integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/get-started-with-the-crowdstrike-falcon-insight-integration.md).

## About this task

You can use the CrowdStrike Falcon Insight integration to make remediation actions on the endpoints in real time, use profiles to gather details about the host, and make specific queries or actions on the endpoint using the Security Incident Response workspace.

The CrowdStrike Falcon Insight integration enables analysts to use the following CrowdStrike Falcon Insight capabilities on the Security Incident Response Analyst workspace:

-   **Get Host Details**
-   **Get Logged On Users**
-   **Get Network Statistics**
-   **Get Running Processes**
-   **Get Running Services**
-   **Isolate Host**
-   **Remove Isolation**
-   **Get File**

## Procedure

1.  In the SIR workspace, open the required security incident and select the **Related Records** tab.

2.  You can use the CrowdStrike Falcon Insight capabilities on the Business Impact related list for analysis.

    1.  Select a **Configuration Item**, and choose a capability from the drop down list.

    2.  Select the **CrowdStrike Falcon Insight** implementation, and select **Submit**.

        The Get Network Statistics capability is invoked on the CI. You can view the work notes for the results and findings.

3.  You can use the CrowdStrike Falcon Insight capabilities on the **Endpoint Detection and Reponse \(EDR\)** related list for analysis.

    1.  In the Endpoint Detection and Reponse \(EDR\) related list, choose an EDR from the list.

    2.  Select on a particular Running Process to view the CrowdStrike Falcon Insight running process details.

    3.  To run a CrowdStrike Falcon Sighting Search on a particular running process, select the running process and select **Run CrowdStrike Sighting Search**.

    4.  Select the **CrowdStrike Falcon Insight** implementation, and select **Run Search**.

        Then a hash sighting search is run on the selected running process. You can view the worknotes for the results and findings.

4.  You can use the CrowdStrike Falcon Insight capabilities on the **Threat Intel** for analysis.

    1.  In the Threat Intel group, select an **Observable**, and choose a CrowdStrike Falcon Insight capability from the drop down list.

    2.  Select the **CrowdStrike Falcon Insight** implementation, and select **Next**.

    3.  In the Select Date/Time pop-up, select a random value and select **Submit**.

        Then a sighting search is run on the selected observable. You can view the worknotes for the results and findings.


