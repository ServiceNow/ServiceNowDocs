---
title: Configure boundary hierarchy
description: Establish parent-child relationships between authorization boundaries to improve boundary management, visibility, and organizational structure within Continuous Authorization and Monitoring. You can assign a parent boundary and associate multiple child boundaries to authorization boundary.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/governance-risk-compliance/grc-continuous-authorization-and-monitoring-workspace/add-child-boundary.html
release: zurich
product: GRC: Continuous Authorization and Monitoring Workspace
classification: grc-continuous-authorization-and-monitoring-workspace
topic_type: task
last_updated: "2025-11-24"
reading_time_minutes: 1
breadcrumb: [View authorization boundary details, CAM Workspace, Use, Continuous Authorization and Monitoring, Governance, Risk, and Compliance]
---

# Configure boundary hierarchy

Establish parent-child relationships between authorization boundaries to improve boundary management, visibility, and organizational structure within Continuous Authorization and Monitoring. You can assign a parent boundary and associate multiple child boundaries to authorization boundary.

## Before you begin

Role required: sn\_irm\_cont\_auth.system\_owner, sn\_irm\_cont\_auth.info\_system\_sec\_officer, sn\_irm\_cont\_auth.system\_owner, sn\_irm\_cont\_auth.admin, sn\_irm\_cont\_auth.system\_user, sn\_irm\_cont\_auth.info\_system\_sec\_officer

## Procedure

1.  Navigate to **All** &gt; **CAM Workspace** and then select the lists icon \(\[Omitted image "ws-list-icon.png"\] Alt text: Lists icon.\).

2.  From the Authorization boundaries under the Risk Management Framework \(RMF\) list, select an authorization boundary record.

3.  To add a parent boundary, select the **Parent boundary** from the **Details** list in the authorization boundary.

    \[Omitted image "auth-bound-parent-boundary.png"\] Alt text: Adding parent boundary.

4.  To add a child boundary, select the **Child Boundaries** related list and perform the following steps:

    1.  Select **Add** to add child boundaries.

        \[Omitted image "child\_auth\_boundary\_add1.png"\] Alt text: Adding a child boundary.

    2.  Select one or more authorization boundaries and select **Add**.

        \[Omitted image "child\_auth\_boundary\_add.png"\] Alt text: Adding Child Authorization Boundary.

        You can add multiple child authorization boundaries.


## Result

You can view the child boundaries in the **Highlighted details** panel under the **Boundary hierarchy** section.

\[Omitted image "child\_auth\_boundary\_add2.png"\] Alt text: Viewing child boundary hierarchy.

**Parent Topic:**[View authorization boundary details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/grc-continuous-authorization-and-monitoring-workspace/auth-bound-overview-ws.md)

