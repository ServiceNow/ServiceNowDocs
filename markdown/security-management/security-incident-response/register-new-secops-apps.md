---
title: Register new Security Operations applications for on-demand orchestration
description: In the base system, Security Operations applications are automatically registered when they are activated. Registration allows the workflows associated with the applications to be available for on-demand orchestration requests. If needed, you can define new applications and associate workflows with them for on-demand orchestration.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/security-management/security-incident-response/register-new-secops-apps.html
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Define new on-demand orchestrations, Managing security incidents and inbound requests, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Register new Security Operations applications for on-demand orchestration

In the base system, Security Operations applications are automatically registered when they are activated. Registration allows the workflows associated with the applications to be available for on-demand orchestration requests. If needed, you can define new applications and associate workflows with them for on-demand orchestration.

## Before you begin

Role required: sn\_si.write

## Procedure

1.  Navigate to **All** &gt; **Security Operations** &gt; **Utilities** &gt; **SecOps Application Registry**, and select **Register Application**.

    The Security Operations Application screen appears.

    \[Omitted image "secops-apps.png"\] Alt text: Security Operations application registration

2.  In the **Application** field, select the lookups \(magnifying glass\) icon.

    The Applications screen appears.

    \[Omitted image "applications.png"\] Alt text: Applications screen

3.  Select **New**.

    The Application Creator screen appears.

    \[Omitted image "app-creator.png"\] Alt text: Application creator

    **Note:** The options that display depend on the applications you have activated. For detailed information on creating new applications, see .

4.  After the application has been generated, you can create scripts for setting up on-demand orchestration.

    **Note:** Setting up on-demand orchestration for new applications requires advanced technical knowledge of scripting and creating triggers for the scripts \(business rules, UI action, workflows, and so on\). For more information, contact ServiceNow Professional Services.


