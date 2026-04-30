---
title: View affected items for a security incident
description: You can view affected items, such as CIs, affected users, and affected services associated with a security incident.
locale: en-US
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-04-29"
reading_time_minutes: 2
breadcrumb: [View information in a security incident, Managing security incidents and inbound requests, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# View affected items for a security incident

You can view affected items, such as CIs, affected users, and affected services associated with a security incident.

## Before you begin

Role required: sn\_si.basic

## Procedure

1.  If it is not already open, open the security incident for which you want to view affected items.

2.  Click the **Show Affected Items** related link.

3.  Click any of the related lists to view or add information for the security incident.

<table id="table_hng_51r_yy"><thead><tr><th>

Tab

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration Items

</td><td>

Affected configuration items \(CI\). After affected CIs are identified, you can manually add affected resources from this related list.

</td></tr><tr><td>

Affected Users

</td><td>

After affected users are identified, you can manually add affected users from this related list.

</td></tr><tr><td>

Affected Services

</td><td>

View or add business services associated with the security incident. **Note:** If an affected CI is added after the security incident is opened, it is a good idea to right-click in the form header and select **Refresh Impacted Services**.

</td></tr></tbody>
</table>    **Note:** If the [Security Operations Integration - Get Running Processes](../../security-operations-common/concept/get-running-processes-capability.md) integration capability is active, and you add a CI to a security incident, the [Get Running Processes](../../security-operations-integrations/concept/secops-integration-get-running-processes-workflow.md) workflow runs and retrieves a list of running processes on the CI.

    If the [Security Operations Integration - Isolate Host](../../security-operations-common/concept/isolate-host-capability.md) integration capability is active, you can select one or more CIs and restrict their system connections to other devices. To do this, select the check boxes for the CIs and click **Isolate Host** from the **Actions on selected rows** choice list.

4.  Click any of the following related links to further update the security incident:

    -   [Show Related Items](show-related-items-for-si.md)
    -   [Show IoC](show-ioc-info-for-si.md)
    -   [Show Enrichment Data](show-enrich-data-for-si.md)
    -   [Show Response Tasks](show-response-tasks-for-si.md)
5.  When you have completed your entries, click **Submit**.


