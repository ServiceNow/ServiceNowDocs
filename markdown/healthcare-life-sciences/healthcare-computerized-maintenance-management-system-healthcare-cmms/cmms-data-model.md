---
title: Healthcare Computerized Maintenance Management System data model
description: The Healthcare Computerized Maintenance Management System \(Healthcare CMMS\) application provides a data model for use in the Healthcare CMMS workflow.
locale: en-US
release: xanadu
product: Healthcare Computerized Maintenance Management System \(Healthcare CMMS\)
classification: healthcare-computerized-maintenance-management-system-healthcare-cmms
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring Healthcare CMMS, Healthcare CMMS, Clinical Device Management, Healthcare and Life Sciences]
---

# Healthcare Computerized Maintenance Management System data model

The Healthcare Computerized Maintenance Management System \(Healthcare CMMS\) application provides a data model for use in the Healthcare CMMS workflow.

**Important:** Starting with the Xanadu release, Healthcare Computerized Maintenance Management System is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. For details on the deprecation process, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

To use maintenance and servicing workflows or inventory and management workflows, please see [Clinical Device Management](clinical-device-mgmt-overview.md).

The Healthcare CMMS data model extends the Healthcare and Life Sciences data model.

The Healthcare CMMS data model uses the Medical device case \[sn\_hcls\_cmms\_case\] table to store medical device cases for medical device in-service, reviewing the AEM request for a medical device model, resolving a medical device issue, or medical device out-of-service.

You can install the Healthcare CMMS application to use its data model.

The following diagram shows the tables and their relationships that comprise the Healthcare CMMS data model.

![Data model displaying how tables within Healthcare CMMS and Healthcare and Life Sciences Service Management Core interact.](../image/cmms-data-model.png "Healthcare CMMS data model")

The Healthcare CMMS data model uses the following tables included within the Healthcare CMMS application to store data.

<table id="table_p3d_b42_ppb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Medical device case \[sn\_hcls\_cmms\_case\]

</td><td>

Stores the medical device cases.

</td></tr></tbody>
</table>The Healthcare CMMS data model uses the following tables included within the Healthcare and Life Sciences Service Management Core application.

<table id="table_ygf_fbl_drb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Healthcare case \[sn\_hcls\_case\]

</td><td>

Supports the healthcare case types.

</td></tr></tbody>
</table>For more information, see [Healthcare and Life Sciences data model](hcls-serv-mgmt-core.md).

