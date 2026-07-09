---
title: Components installed with AI Security Exposure Management
description: Components installed with the AI Security Exposure Management application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/security-management/installed-with-aisecmanagement.html
release: zurich
topic_type: reference
last_updated: "2026-07-06"
reading_time_minutes: 1
breadcrumb: [Using the AI guardrails helper skill and agentic workflow, AI Security Exposure Management, Use, Unified Security Exposure Management, Security Operations]
---

# Components installed with AI Security Exposure Management

Components installed with the AI Security Exposure Management application.

## Roles

|Role title \[name\]|Description|
|-------------------|-----------|
|sn\_sec\_ai.read\_risk\_score\_configuration|Views risk score Calculators, risk rules and vulnerability Rollup Calculators.|
|sn\_sec\_ai.write\_all|Updates all AI Security Exposure Management findings and remediation tasks.|
|sn\_sec\_ai.remediation\_owner|Reads and updates AI Security Exposure Management findings and remediation tasks assigned to the user or their groups.|
|sn\_sec\_ai.write\_assigned|Updates AI Security Exposure Management scan findings and remediation tasks assigned to me or my groups.|
|sn\_sec\_ai.vulnerability\_analyst|Views and update all AI Security Exposure Management scan findings and remediation tasks.|
|sn\_sec\_ai.vulnerability\_admin|Administrative access to all AI Security Exposure Management findings, scans, and remediation tasks.|
|sn\_sec\_ai.read\_all|Views all AI Security Exposure Management scan findings and remediation tasks.|
|sn\_sec\_ai.read\_assigned|Views AI Security Exposure Management scan findings and remediation tasks assigned to me or my groups.|
|sn\_sec\_ai.exception\_approver|Approves exceptions and deferrals of AI Security Exposure Management scan findings.|

## Scheduled jobs

<table id="table_pgq_yss_tjc"><thead><tr><th>

 

</th><th>

 

</th></tr></thead><tbody><tr><td>

Model validation findings schedule job

</td><td>

Collects the AI validation findings-related metrics shown on the AISEM dashboard on the Home page in the AI exposures module. Scheduled to run daily.

</td></tr><tr><td>

Model scan findings schedule job

</td><td>

Collects the AI vulnerability findings-related metrics shown on the AISEM dashboard on the Home page in the AI exposures module. Scheduled to run daily.

</td></tr><tr><td>

AI posture findings schedule job and Posture findings schedule job

</td><td>

Together these two jobs collect the AI posture findings-related metrics shown on the AISEM dashboard on the Home page in the AI exposures module. Scheduled to run daily.

</td></tr><tr><td>

\[PA VR AISEC\] Daily collection job for findings

</td><td>

Calls the model, scan and posture findings jobs. This job runs the PA indicators and that refresh the metrics on the dashboard. Scheduled to run daily.

</td></tr><tr><td>

AISEM guardrail skill scheduled job

</td><td>

**Note:** This job is installed only if you install Now Assist for Vulnerability Response. Sorts the AI validation findings imported from third-party integrations and tries to match them with the appropriate guardrails reported by third-party integrations in your environment.

</td></tr></tbody>
</table>See the [AI security exposure management](https://www.servicenow.com/community/secops-articles/reduce-ai-attack-surface-with-ai-security-exposure-management/ta-p/3563696) article in the Security Operations Community for more information about AI Security Exposure Management.

**Parent Topic:**[Using the AI guardrails helper skill and agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/ai-security-exposure-skill-agent.md)

