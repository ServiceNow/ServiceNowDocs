---
title: Using McAfee ePO integration in Analyst Workspace
description: Use the McAfee ePO integration to leverage the McAfee ePO capabilities on the SIR Analyst workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/security-management/security-incident-response/using-mcafee-integration-aws.html
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [McAfee ePO integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Using McAfee ePO integration in Analyst Workspace

Use the McAfee ePO integration to leverage the McAfee ePO capabilities on the SIR Analyst workspace.

## Before you begin

Role required: sn\_si.admin

Before you use McAfee ePO integration on the Security Incident Response workspace, you must download it from the ServiceNow Store and configure it. For more information, see [Set up your ServiceNow AI Platform instance for the McAfee ePO integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/security-incident-response/mcaffee-epo-setup-now.md).

## About this task

You can use the McAfee ePO integration to make remediation actions on the endpoints in real-time, use profiles to gather details about the host, and make specific queries or actions on the endpoint using the Security Incident Response workspace.

The McAfee ePO integration enables analysts to use the following McAfee ePO capabilities on the Security Incident Response Analyst workspace:

-   **Get Host Details**
-   **Isolate Host**
-   **Remove Isolation**
-   **Run Additional Action\(s\) on Endpoint**

## Procedure

1.  To open the security incident in the SIR workspace, click **Switch to SIR Workspace** on the security incident.

2.  In the SIR workspace, select the **Related Records** tab.

3.  Select any **Configuration Item**, and choose a McAfee ePO capability to trigger from the related list drop down action.

    For example, Get Host Details.

4.  In the Get Host Details pop-up, select the **McAfee ePO** implementation.

5.  Select **Submit**.

    The Get Host Details capability is invoked on the CI. You can view the worknotes for the results and findings.

6.  To view the data for the triggered capability, select the **Investigation** tab.

7.  Select the **Configuration Item**, and click the **View Associated Info** action.

8.  Select the **Configuration Item** to view the host details.

    Similarly, you can try using the other McAfee ePO capability for you security incidents on the SIR Analyst Workspace.

9.  You can use the McAfee ePO capabilities on the **Endpoint Detection and Reponse \(EDR\)** related list for analysis.

10. Browse and select a profile from the list of available profiles.

    The list of available profiles are Get Host Details, Isolate Host machine, and Remove Isolation. For example, let's select Get Host Details.

11. Select the **McAfee ePO** implementation, and click **Submit**.


**Parent Topic:**[McAfee ePO integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/security-incident-response/mcaffee-epo-overview-arch.md)

**Previous topic:**[Trigger additional actions in McAfee ePO integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/security-incident-response/configure-additional-actions-mcafee.md)

**Next topic:**[Test security incidents to initiate malware scan](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/security-incident-response/mcafee-epo-test-incident-malscan.md)

