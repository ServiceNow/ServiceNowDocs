---
title: Customize Firewall Audits and Reporting
description: Configure default policy owner and approval groups for firewall rule change requests to reduce manual data entry.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/discovery/customize-firewall-audit-reporting.html
release: brazil
product: Discovery
classification: discovery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Visibility to Firewall inventory, Configure, Firewall Audits and Reporting, ITOM Visibility, IT Operations Management]
---

# Customize Firewall Audits and Reporting

Configure default policy owner and approval groups for firewall rule change requests to reduce manual data entry.

## Before you begin

Role required: discovery\_admin or admin

## About this task

When users submit firewall rule change requests, each request requires assignment to a policy owner group and an approval group. Without default values, administrators must manually populate these fields for every request. Configuring default groups streamlines the request process by automatically populating these fields.

Set these defaults during initial Firewall Audits and Reporting setup or when your organization's security team structure changes. For more information on properties, see [Discovery properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery/r_DiscoveryProperties.md).

## Procedure

1.  Navigate to **All** &gt; **Discovery Definition** &gt; **Properties**.

2.  Configure the firewall rule change management groups.

    1.  In the sn\_disco\_firewall.default.rule.task.policy.owner.group property, enter the name of the group responsible for implementing firewall rule changes.

    2.  In the sn\_disco\_firewall.default.rule.task.approval.group property, enter the name of the group responsible for approving firewall rule changes.

    These groups are automatically assigned as the policy owners for new firewall rule requests.


## Result

When users submit new firewall rule change requests, the policy owner group and approval group fields automatically populate with the configured default values.

**Parent Topic:**[Visibility to Firewall inventory](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery/use-firewall-audit-rep.md)

