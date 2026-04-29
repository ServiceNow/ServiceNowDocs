---
title: Quick start tests for Universal Request
description: Validate that Universal Request still works after you make any configuration change such as apply an upgrade or develop an application. Copy and customize these quick start tests to pass when using your instance-specific data.
locale: en-US
release: australia
product: Universal Request for HR Service Delivery
classification: universal-request-for-hr-service-delivery
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Universal Request, Employee Service Management]
---

# Quick start tests for Universal Request

Validate that Universal Request still works after you make any configuration change such as apply an upgrade or develop an application. Copy and customize these quick start tests to pass when using your instance-specific data.

Universal Request quick start tests require activating the Universal Request \(com.snc.universal\_request\), Universal Request: Integration for Incident management \(com.snc.incident.universal\_request\), and Human Resources Scoped App: Core \(com.sn\_hr\_core\) plugins.

<table id="table_ubx_4ry_nnb"><thead><tr><th>

Test

</th><th>

Description

</th><th class="filter">

Release version

</th></tr></thead><tbody><tr><td>

UR: Transferring an HR case to an Incident

</td><td>

Validate if an HR case is transferred to an incident and an incident is created.

</td><td>

Quebec

</td></tr><tr><td>

UR: Restrict or Unrestrict universal request

</td><td>

Validates the following:-   The fields are restricted and hidden when a routing agent restricts a UR.
-   Only agents with **sensitiveinfo\_agent** role are allowed to unrestrict the request.
-   And, after the request is unrestricted all fields are visible.
-   sys-audit log access is available for agents.

</td><td>

Yokohama

</td></tr><tr><td>

UR: Universal Request creation with RITM

</td><td>

Verifies a catalog request for any item from self-service can be created when Universal Request Certified is enabled.

</td><td>

San Diego

</td></tr></tbody>
</table>**Parent Topic:**[Universal Request](../../../product/universal-request/concept/ur-landing-limitedaccess.md)

