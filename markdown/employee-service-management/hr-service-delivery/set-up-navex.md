---
title: Set up Employee Relations integration with Navex Ethicspoint
description: Understand how to set up the Employee Relations integration with Navex Ethicspoint application for pulling and pushing employee relations case data from the Navex EthicsPoint system into the ServiceNow system.
locale: en-US
release: zurich
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Employee Relations integration with Navex Ethicspoint, Integrate with third-party systems, HR Service Delivery, Employee Service Management]
---

# Set up Employee Relations integration with Navex Ethicspoint

Understand how to set up the Employee Relations integration with Navex Ethicspoint application for pulling and pushing employee relations case data from the Navex EthicsPoint system into the ServiceNow system.

## Before you begin

Role required: sn\_hr\_navex\_ep.admin

## Procedure

1.  Install updates sets from the Supporting Links and Docs section in [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/application/fd01665053e2301095f4ddeeff7b1237/1.1.1?referer=%2Fstore%2Fsearch%3Flistingtype%3Dallintegrations%25253Bancillary_app%25253Bcertified_apps%25253Bcontent%25253Bindustry_solution%25253Boem%25253Butility%25253Btemplate%25253Bgenerative_ai%25253Bsnow_solution%26q%3Dnavex&sl=sh).

2.  Allow RCAs manually.

    Allow the Restricted Caller Access records with Status = **Requested** and Source Scope = **Employee Relations integration with Navex EthicsPoint**.

3.  For better performance, index Source field: external\_id mapped to Target field: correlation\_id in [Transform maps](../reference/transform-maps-navex.md).

    For more information, see [create a table index](https://www.servicenow.com/docs/access?context=t_CreateCustomIndex&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

4.  Set up Navex EthicsPoint spoke.

    For more information, see [Set up Navex EthicsPoint spoke](https://www.servicenow.com/docs/access?context=navex-ethics-spoke&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US).

5.  [Configure properties](prop-navex.md).

6.  [Map fields](map-fields-navex.md).


