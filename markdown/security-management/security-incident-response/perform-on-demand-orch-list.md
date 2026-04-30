---
title: Perform on-demand orchestration from the Security Incident list
description: On-demand orchestration can be invoked from the Security Incident list, as well as from related lists in Security Incident Response.
locale: en-US
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Manage on-demand orchestration, Managing security incidents and inbound requests, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Perform on-demand orchestration from the Security Incident list

On-demand orchestration can be invoked from the Security Incident list, as well as from related lists in Security Incident Response.

## Before you begin

Role required: sn\_si.write

## Procedure

1.  Navigate to **All** &gt; **Security Incident** &gt; **Incidents** &gt; **Show Open Incidents**.

2.  Select the check box next to the security incident for which you want to run a workflow.

3.  Click the **Actions on selected rows** choice list at the bottom of the screen, and click **Run Orchestration**.

    The **Run Orchestration** dialog box opens. The appearance of the dialog box depends on the setting of the [sn\_sec\_cmn.use\_on\_demand\_tbl\_as\_whitelist](../concept/on-demand-orchestration.md) property in Security Support Common.

    ![Run Orchestration](../image/run-orch.png)

4.  Click the lookup icon and select the workflow you want to run.

    The selected workflow runs. For details, see [Security Incident Response Orchestration flows and actions](../../security-incident-response-orchestration/concept/sec-inc-resp-orchestration-workflows.md).


