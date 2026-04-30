---
title: Using CrowdStrike Falcon Insight integration in Analyst Workspace
description: Use the CrowdStrike Falcon Insight integration to leverage the CrowdStrike Falcon Insight capabilities on the SIR Analyst workspace.
locale: en-US
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [CrowdStrike Falcon Insight integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Using CrowdStrike Falcon Insight integration in Analyst Workspace

Use the CrowdStrike Falcon Insight integration to leverage the CrowdStrike Falcon Insight capabilities on the SIR Analyst workspace.

## Before you begin

Role required: sn\_si.admin

Before you use CrowdStrike Falcon Insight integration on the Security Incident Response workspace, you must download it from the ServiceNow Store and configure it. For more information, see [Getting started with the CrowdStrike Falcon Insight integration](../concept/get-started-with-the-crowdstrike-falcon-insight-integration.md).

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

    1.  Select a **Configuration Item**, and choose a capability from the dropdown list.

        ![CrowdStrike Falcon Insight for CI](../../../secops-analyst-workspace/image/falcon-insight-workspace-ci.png "CrowdStrike Falcon Insight for CI")

    2.  Select the **CrowdStrike Falcon Insight** implementation, and click **Submit**.

        The Get Network Statistics capability is invoked on the CI. You can view the worknotes for the results and findings.

3.  You can use the CrowdStrike Falcon Insight capabilities on the **Endpoint Detection and Reponse \(EDR\)** related list for analysis.

    1.  In the Endpoint Detection and Reponse \(EDR\) related list, choose an EDR from the list.

    2.  Click on a particular Running Process to view the CrowdStrike Falcon Insight running process details.

    3.  To run a CrowdStrike Falcon Sighting Search on a particular running process, select the running process and click **Run CrowdStrike Sighting**.

        ![CrowdStrike Falcon Insight for Endpoint Detection and Response](../../../secops-analyst-workspace/image/falcon-insight-workspace-edr.png "CrowdStrike Falcon Insight for EDR")

    4.  Select the **CrowdStrike Falcon Insight** implementation, and click **Run Search**.

        Then a hash sighting search is run on the selected running process. You can view the worknotes for the results and findings.

4.  You can use the CrowdStrike Falcon Insight capabilities on the **Threat Intel** for analysis.

    1.  In the Threat Intel group, select an **Observable**, and choose a CrowdStrike Falcon Insight capability from the dropdown list.

    2.  Select the **CrowdStrike Falcon Insight** implementation, and click **Next**.

        ![CrowdStrike Falcon Insight for Threat Intel](../../../secops-analyst-workspace/image/falcon-insight-workspace-ti.png "CrowdStrike Falcon Insight for Threat Intel")

    3.  In the Select Date/Time pop-up, select a random value and click **Submit**.

        Then a sighting search is run on the selected observable. You can view the worknotes for the results and findings.


