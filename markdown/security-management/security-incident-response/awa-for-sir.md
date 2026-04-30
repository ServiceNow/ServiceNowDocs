---
title: Advanced Work Assignment for Security Incident Response
description: Advanced Work Assignment \(AWA\) intelligently routes and assigns security incidents to security analysts on the basis on their availability, capacity, and skills.
locale: en-US
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2025-11-25"
reading_time_minutes: 1
breadcrumb: [Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Advanced Work Assignment for Security Incident Response

Advanced Work Assignment \(AWA\) intelligently routes and assigns security incidents to security analysts on the basis on their availability, capacity, and skills.

AWA streamlines the assignment process, ensuring that critical incidents are handled by the most appropriate and available analysts. AWA improves overall response times and efficiency in security operations.

The ability to make configuration changes requires the AWA admin role \(awa\_admin\), which isn’t provided by default with SIR Workspace. For more information, see [Components installed with Security Incident Response](../../security-incident-response/reference/installed-with-sir.md).

## Key features

-   AWA uses service channels to route requests. Security incidents are placed in queues. You can create multiple queues for different priorities or groups. Routing conditions like priority or state determine which queue an incident enters.
-   AWA admins must configure assignment eligibility by adding groups and rules. Only eligible analysts receive assignment notifications.
-   AWA admins can set how many security incidents a security analyst can handle at once. The default value is 1.
-   AWA analysts can set their availability. Based on the AWA configuration, security analysts can either manually accept or reject incoming security incidents or you can choose to have security incidents be auto-assigned to security analysts.

**Note:**

You can’t use multiple security incident assignment methods simultaneously. For more information, see [Assigning security analysts](https://www.servicenow.com/docs/bundle/zurich-security-management/page/product/security-incident-response/reference/r_AgentAssignment.html).

