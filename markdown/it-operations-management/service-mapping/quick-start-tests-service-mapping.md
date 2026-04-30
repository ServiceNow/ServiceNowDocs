---
title: Quick start tests for Service Mapping
description: After upgrades and deployments of new applications or integrations, run quick start tests to verify that Service Mapping still works. If you have customized Service Mapping, copy the quick start tests and configure them for your customizations.
locale: en-US
release: xanadu
product: Service Mapping
classification: service-mapping
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring Service Mapping, Service Mapping, ITOM Visibility, IT Operations Management]
---

# Quick start tests for Service Mapping

After upgrades and deployments of new applications or integrations, run quick start tests to verify that Service Mapping still works. If you have customized Service Mapping, copy the quick start tests and configure them for your customizations.

Service Mapping quick start tests require activating the Service Mapping \(com.snc.service-mapping\) plugin and loading the demo data.

<table id="table_lkf_nfg_h1c"><thead><tr><th>

Test

</th><th>

Description

</th><th>

Release version

</th></tr></thead><tbody><tr><td>

SM OOTB: Tests SM application visibility by roles

</td><td>

Validate the visibility of Service Mapping applications and modules for different roles. For example, the test verifies that a user logged in with the service\_mapping\_user role cannot access the Administration module under Service Mapping.

</td><td>

Madrid

</td></tr><tr><td>

SM OOTB: Service map verification

</td><td>

Use this test template to create custom tests for verifying that the topology of the most significant services is unchanged.

 Configure values under Test Run Data Sets, to identify the name of the service to test and the nodes that you expect to find in this service.

 For the node name values, enter the node attribute exactly as it appears on the map, for example, "Apache server." If the attribute name for a node is truncated or shows that a node is a CI cluster, configure this node name value to reflect the way it appears on the map, for example, "11x ExchangeF" for a group of 11 Exchange FrontEnd servers.

**Note:** You cannot use this test to verify the service content beyond the top, unexpanded level.

</td><td>

Orlando, updated Paris

</td></tr><tr><td>

SM OOTB: Check UI accessibility after an upgrade

</td><td>

Run this test to check that the Service Mapping UI is fully functional after an upgrade.

</td><td>

Orlando

</td></tr></tbody>
</table>**Related topics**  


[Run an automated test](https://www.servicenow.com/docs/access?context=atf-run-test&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US)

