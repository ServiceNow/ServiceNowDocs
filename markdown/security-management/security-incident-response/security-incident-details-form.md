---
title: Security incident Details tab
description: This section describes all the fields of the Details tab of a security incident.
locale: en-US
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: reference
last_updated: "2025-11-17"
reading_time_minutes: 4
breadcrumb: [Security Incident Details section, Working with Security Incident Records, Use, Security Incident Response Workspace, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Security incident Details tab

This section describes all the fields of the **Details** tab of a security incident.

<table id="table_njk_y4m_3hc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

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

The location of the requester or resource. If a **Configuration Item** isn’t selected, this field is pre-filled with the location of the requester.

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

Security integration through which you ingest the alert or event data such as CarbonBlack, CrowdStrike, McAfee.

</td></tr><tr><td>

Alert Rule

</td><td>

The rule in the security product, which triggered the creation of this security incident.

</td></tr><tr><td>

Risk score

</td><td>

Displays the risk score calculated for this security incident. The value is based on the priority of the security incident, the type of security incident \(Denial of Service, Spear Phishing, or Malicious code activity\), and the number of sources that triggered a failed reputation score on an indicator. The risk score aids in prioritizing security incident work for analysts. Three security incident properties allow you to further designate a color-coded dot to appear next to the risk score in list view to make them more easily identifiable.

 If you change certain fields in the security incident, such as the **Business impact** or **Priority**, and save the record, the **Risk score** is automatically recalculated and displayed. The change is also reflected in the work notes and on the Risk Score Audits related list.

**Note:** The risk score is also recalculated when affected users are associated with a security incident, affected services, or vulnerable items.

 You can also manually enter a new **Risk score**. This can be useful if you want to keep a particular security incident at the top of the list of security incidents you’re analyzing. If you enter a new **Risk score**, the **Risk score override** check box is automatically selected. Regardless of the changes made in the security incident, a manually-entered risk score isn’t automatically recalculated.

**Note:** If you have upgraded your instance from a prior release, risk scores were calculated for all of your open security incidents. For more information, see [Understanding security incident calculators](../../security-incident-response/reference/setup-assistant-reference.md#).

</td></tr><tr><td>

Risk score override

</td><td>

Option to override the automatic update of the risk score. The override is reflected in the work notes.

</td></tr><tr><td>

External risk score

</td><td>

The calculated external risk score.

</td></tr><tr><td>

Business impact

</td><td>

Importance of this security incident to your business. The default value is Non-critical. If, after the security incident record has been saved, you change the value in the **Priority** and/or **Risk** fields, the **Business impact** is recalculated.

</td></tr><tr><td>

Functional Impact

</td><td>

The functional impact of this security incident. For example, service downtime, business disruption.Following are the options:

-   Low
-   Medium
-   High

**Note:** This field isn’t available in the base system. To add this field, see [Accessing Form Builder](https://www.servicenow.com/docs/access?context=access-form-builder&version=zurich&pubname=zurich-application-development&ft:locale=en-US).

</td></tr><tr><td>

Recoverability

</td><td>

How easily and quickly you can restore the normal operations and recover from the impact of the security incident. Following are the options:-   Regular
-   Supplemented
-   Extended
-   Not Recoverable

**Note:** This field isn’t available in the base system. To add this field, see [Accessing Form Builder](https://www.servicenow.com/docs/access?context=access-form-builder&version=zurich&pubname=zurich-application-development&ft:locale=en-US).

</td></tr><tr><td>

Information Impact

</td><td>

The data impact of the security incident. You can select all the applicable:-   Privacy Breach
-   Proprietary Breach
-   Integrity Loss

**Note:** This field is not available in the base system. To add this field, see [Accessing Form Builder](https://www.servicenow.com/docs/access?context=access-form-builder&version=zurich&pubname=zurich-application-development&ft:locale=en-US).

</td></tr><tr><td>

Priority

</td><td>

The order in which to address this security incident, based on the urgency. If this value is changed after the record is saved, it can affect the **Business impact** calculation.

</td></tr><tr><td>

Assignment group

</td><td>

The group to which this security incident is assigned.

</td></tr><tr><td>

Assigned to

</td><td>

The individual assigned to analyze this security incident. Assignments can be performed manually or automatically. For more information, see [Assigning security analysts](../../security-incident-response/reference/r_AgentAssignment.md#).

</td></tr><tr><td>

Short description

</td><td>

A brief description of the security incident.

</td></tr><tr><td>

Knowledge results

</td><td>

As you enter the short description, links to related articles from the knowledge base appear. Scanning the information could solve your issue.

</td></tr></tbody>
</table>**Parent Topic:**[Security Incident Details section](../concept/security-incident-details.md)

