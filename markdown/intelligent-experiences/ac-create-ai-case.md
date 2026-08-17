---
title: Create an AI case
description: Open an AI case to investigate and document an incident affecting an AI asset, such as a suspected breach, data exposure, or policy violation.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/ac-create-ai-case.html
release: zurich
topic_type: task
last_updated: "2026-07-16"
reading_time_minutes: 3
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [AI cases, Manage tasks and approvals, Address action items, AI Control Tower, Enable AI experiences]
---

# Create an AI case

Open an AI case to investigate and document an incident affecting an AI asset, such as a suspected breach, data exposure, or policy violation.

## Before you begin

Role required: sn\_ai\_governance.ai\_steward or sn\_ai\_asset\_mgmt.ai\_asset\_owner

## About this task

An AI case documents an incident that needs investigation, such as a suspected security breach, a data exposure, or a policy violation involving an AI asset. Creating a case starts a structured investigation that can include a breach determination, a root cause analysis, and a remediation plan.

## Procedure

1.  Navigate to **All** &gt; **AI Control Tower** &gt; **Home** &gt; **Activity Center** &gt; **Work** &gt; **Assigned to you**.

2.  Select the **Cases** sub-tab.

3.  Select **New**.

4.  Fill in the fields that describe the case.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the case.|
    |Description|Description of the case.|
    |Type|Type of case. Defaults to **AI case**.|
    |Sub-type|Subcategory of the case type, if applicable.|
    |State|Current state of the case. Defaults to **New**.|
    |Priority|Priority of the case.|
    |Requester|User requesting the case. Defaults to you.|
    |Requested on behalf of|User the case is being requested for, if different from the requester.|

    **Note:** The **Primary entity** and **Entity owner** fields populate automatically and aren't set when you create the case.

5.  In the Assignment section, specify who should work the case.

    |Field|Description|
    |-----|-----------|
    |Assignment group|Group responsible for working the case.|
    |Watch list|Users who want to stay informed about the case.|
    |Case analyst|User assigned to analyze the case.|
    |Accountable executive|Executive or executives accountable for the case outcome.|

6.  In the Primary origin section, describe where the case originated.

    |Field|Description|
    |-----|-----------|
    |Location|Location where the case originated.|
    |Sub-location|More specific location within the primary location.|
    |Impacted business unit|Business unit affected by the case.|
    |Impacted department|Department affected by the case.|
    |Additional source|Additional context about how the case was identified.|

    **Note:** The **Source** field is set automatically based on how the case originated \(such as manually, or from an email or a security incident\) and isn't set when you create the case.

7.  In the Schedule section, record the dates relevant to the case.

    |Field|Description|
    |-----|-----------|
    |Date of occurrence|Date the underlying event occurred.|
    |Date of discovery|Date the case was discovered. Defaults to the current date.|
    |Case closure SLA|Target date and time for closing the case.|
    |Investigation planned start|Planned start date for the investigation.|
    |Investigation planned end|Planned end date for the investigation.|
    |Investigation actual start|Actual start date of the investigation.|
    |Investigation actual end|Actual end date of the investigation.|
    |Remediation planned start|Planned start date for remediation.|
    |Remediation planned end|Planned end date for remediation.|
    |Remediation actual start|Actual start date of remediation.|
    |Remediation actual end|Actual end date of remediation.|

    **Note:** The **Reported date** field is set automatically to when you create the case.

8.  In the Breach analysis section, record whether the case involves a breach.

    |Field|Description|
    |-----|-----------|
    |Breach status|Whether the case involves a data or security breach. Defaults to **To be determined**.|
    |Reporting status|Whether the case has been reported to regulators. This field is set automatically based on the regulations associated with the case. Defaults to **To be determined**.|

9.  In the Root cause analysis section, document your findings and any remediation.

    |Field|Description|
    |-----|-----------|
    |Overall observations|Findings from your review of the case.|
    |Remediation taken|Whether remediation measures have been taken to address the case. Options are **Yes** and **No**.|
    |Overall preventive measures|Steps to prevent the issue from recurring.|

    **Note:** The **Primary cause** and **Primary consequence** fields populate based on further analysis and aren't set when you create the case.

10. In the Activity section, add any supporting notes or comments.

    |Field|Description|
    |-----|-----------|
    |Work notes \(Private\)|Internal notes about the case that aren't visible to the customer.|
    |Additional comments \(Customer visible\)|Comments about the case that are visible to the customer.|

11. Save the case.


## Result

The case is created and appears in the **Cases** sub-tab, where you and the assigned case analyst can track the investigation through to closure.

