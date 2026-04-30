---
title: Create a security incident from the Security Incident list
description: In addition to automatic methods for creating security incidents, you can create them manually, as needed.
locale: en-US
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 6
breadcrumb: [Security incident manual creation, Security incident creation, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Create a security incident from the Security Incident list

In addition to automatic methods for creating security incidents, you can create them manually, as needed.

This video shows a visual overview of how you could create a security incident from the Security Incident list.

Create a security incident from the Security Incident list

## Before you begin

Role required: sn\_si.basic

## Procedure

1.  Navigate to any security incident list \(for example, **All** &gt; **Security Incident** &gt; **Incidents** &gt; **Show All Incidents**\).

    ![Security incident lists](../image/SiList.png)

2.  Select **New**.

    ![New security incident](../image/SiForm.png)

3.  On the form, fill in the fields.

<table id="table_vks_thr_ns"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Select security tag

</td><td>

If needed, select a [Security tag](../../security-operations-common/task/create-class-group-and-tags.md) to add metadata to the record or identify who should have access to this security incident record. This field appears only after the security incident has been saved.**Note:** Manual tags are preserved when automatic tags are applied.

</td></tr><tr><td>

Number

</td><td>

\[Read only\] The security incident number.

</td></tr><tr><td>

Requested by

</td><td>

The person requesting the work to be performed.

</td></tr><tr><td>

Configuration Item

</td><td>

The server, computer, router, or other configuration item affected by the security issue.

</td></tr><tr><td>

Affected user

</td><td>

The person affected by the security issue.

</td></tr><tr><td>

Location

</td><td>

The location of the requester or resource. If a **Configuration Item** is not selected, this field is pre-filled with the location of the requester.

</td></tr><tr><td>

Category

</td><td>

The category that identifies the type of security issue.If a category is selected, a workflow for analyzing this issue is executed when the record is saved. For example, if you select **Denial of Service**, the Security Incident - Denial of Service - Template workflow is executed.

 For more information, see [Security Incident Response workflow templates](../../security-incident-response-orchestration/concept/sir-orch-workflow-templates.md).

</td></tr><tr><td>

Subcategory

</td><td>

The subcategory that further defines the issue.

</td></tr><tr><td>

Opened

</td><td>

\[Read only\] Displays the date and time the incident was opened.

</td></tr><tr><td>

State

</td><td>

The current state of the security incident. Upon security incident creation, this field defaults to **Draft**.

</td></tr><tr><td>

Substate

</td><td>

Identifies whether the security incident includes a pending problem or change.

</td></tr><tr><td>

Source

</td><td>

Identifies the source of the security incident, such as email, a phone call, or network monitoring.

</td></tr><tr><td>

Alert Sensor

</td><td>

Security integration through which you ingest the alert or event data such as CarbonBlack, CrowdStrike, McAfee, and so on.

</td></tr><tr><td>

Alert Rule

</td><td>

The rule in the security product which triggered the creation of this security incident.

</td></tr><tr><td>

Risk score

</td><td>

Displays the risk score calculated for this security incident. The value is based on the priority of the security incident, the type of security incident \(Denial of Service, Spear Phishing, or Malicious code activity\), and the number of sources that triggered a failed reputation score on an indicator. The risk score aids in prioritizing security incident work for analysts. Three security incident properties enable you to further designate a color-coded dot to appear next to the risk score in list view to make them more easily identifiable.

 If you change certain fields in the security incident, such as the **Business impact** or **Priority**, and save the record, the **Risk score** is automatically recalculated and displayed. The change is also reflected in the work notes and on the Risk Score Audits related list.

**Note:** The risk score is also recalculated when affected users are associated with a security incident, affected services, or vulnerable items.

 You can also manually enter a new **Risk score**. This can be useful if you want to keep a particular security incident at the top of the list of security incidents you are analyzing. If you enter a new **Risk score**, the **Risk score override** check box is automatically selected. Regardless of the changes made in the security incident, a manually-entered risk score is not automatically recalculated.

**Note:** If you have upgraded your instance from a prior release, risk scores were calculated for all of your open security incidents. For more information, see [Understanding security incident calculators](../reference/setup-assistant-reference.md#).

</td></tr><tr><td>

Risk score override

</td><td>

Select this check box to override the automatic update of the risk score. The override is reflected in the work notes.

</td></tr><tr><td>

Business impact

</td><td>

Select the importance of this security incident to your business. The default value is Non-critical. If, after the security incident record has been saved, you change the value in the **Priority** fand/or **Risk** fields, the **Business impact** is recalculated.

</td></tr><tr><td>

Priority

</td><td>

Select the order in which to address this security incident, based on the urgency. If this value is changed after the record is saved, it can affect the **Business impact** calculation.

</td></tr><tr><td>

Assignment group

</td><td>

The group to which this security incident is assigned.

</td></tr><tr><td>

Assigned to

</td><td>

The individual assigned to analyze this security incident. Assignments can be performed manually or automatically. For more information, see [Assigning security analysts](../reference/r_AgentAssignment.md#).

</td></tr><tr><td>

Short description

</td><td>

A brief description of the security incident.

</td></tr><tr><td>

Knowledge results

</td><td>

As you type the short description, links to related articles from the knowledge base appear. Scanning the information could solve your issue.

</td></tr></tbody>
</table>4.  Right-click in the record header and select **Save**.

    If you added a new CI to the security incident, the following integration workflows are automatically executed:

    -   [Security Operations - Get Running Processes Flow](../../security-operations-integrations/concept/secops-integration-get-running-processes-workflow.md). This workflow retrieves a list of running processes on a configuration item \(CI\) from a host or endpoint.
    -   [Security Incident Response - Get Running Services workflow](../../security-incident-response-orchestration/task/get-running-services-workflow.md). This workflow retrieves a list of running services from Windows-based CIs.
    -   [Security Operations Integrations - Get Network Statistics flow](../../security-operations-integrations/task/secops-integration-get-network-stats-workflow.md). This workflow retrieves a list of active network connections from a host or endpoint.
5.  To view the information retrieved by these workflows, click the **Show Enrichment Data** related link, and then click any of the indicated tabs.

    ![Security Incident enrichment](../image/enrichment-data.png)

    **Note:** Additional workflows are executed based on the third-party integrations you have activated as follows [Security Operations Carbon Black Integration - Get Running Processes Flow](../../security-operations-integrations/concept/secops-integration-cb-get-running-processes-workflow.md)


**Related topics**  


[Security Incident Response setup](../concept/setup-sir.md)

