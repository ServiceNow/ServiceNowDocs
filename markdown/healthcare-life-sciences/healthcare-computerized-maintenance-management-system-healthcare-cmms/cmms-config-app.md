---
title: Configuring Healthcare Computerized Maintenance Management System
description: Set up the Healthcare Computerized Maintenance Management System \(Healthcare CMMS\) application to complete activities associated with a medical device.
locale: en-US
release: yokohama
product: Healthcare Computerized Maintenance Management System \(Healthcare CMMS\)
classification: healthcare-computerized-maintenance-management-system-healthcare-cmms
topic_type: concept
last_updated: "2023-08-03"
reading_time_minutes: 2
breadcrumb: [Healthcare CMMS, Clinical Device Management, Healthcare and Life Sciences]
---

# Configuring Healthcare Computerized Maintenance Management System

Set up the Healthcare Computerized Maintenance Management System \(Healthcare CMMS\) application to complete activities associated with a medical device.

**Important:** Starting with the Xanadu release, Healthcare Computerized Maintenance Management System is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. For details on the deprecation process, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

To use maintenance and servicing workflows or inventory and management workflows, please see [Clinical Device Management](clinical-device-mgmt-overview.md).

**Note:** The Healthcare CMMS application is based on the Healthcare CMMS data model that extends the [Healthcare and Life Sciences data model](hcls-serv-mgmt-core.md) and stores all medical device cases in the Medical device case \[sn\_hcls\_cmms\_case\] table.

The following table provides an overview of the configuration tasks required for Healthcare CMMS.

<table id="table_ksw_gpr_4nb"><thead><tr><th>

Task

</th><th>

Description

</th></tr></thead><tbody><tr><td>

[Install Healthcare CMMS](../task/cmms-install-app.md).

</td><td>

Install the Healthcare CMMS application to work on medical devices.

</td></tr><tr><td>

[Assign roles for Healthcare CMMS users](../task/cmms-assign-roles.md).

</td><td>

Assign roles to control access to features, capabilities, and data in the Healthcare CMMS application.

</td></tr><tr><td>

[Use the Healthcare CMMS data model](cmms-data-model.md).

</td><td>

Use Healthcare CMMS tables to store the data related to medical devices.

</td></tr><tr><td>

[Complete the configuration tasks for medical device in-service requests](cmms-config-ob-cd-case.md).

</td><td>

Configure Healthcare CMMS to set the medical devices in-service.

</td></tr><tr><td>

[Complete the configuration tasks for the review of AEM requests](cmms-config-aem-cd-case.md).

</td><td>

Configure Healthcare CMMS for reviewing AEM requests for medical device models.

</td></tr><tr><td>

[Configure the process for reporting medical device issues](cmms-device-issue-rp.md).

</td><td>

Configure Healthcare CMMS for reporting medical device issues from a service portal of your healthcare organization.

</td></tr><tr><td>

[Configuring Healthcare CMMS to set medical devices out-of-service](cmms-configure-retiring-medical-device.md)

</td><td>

Configure Healthcare CMMS to set the medical devices out-of-service.

</td></tr></tbody>
</table>