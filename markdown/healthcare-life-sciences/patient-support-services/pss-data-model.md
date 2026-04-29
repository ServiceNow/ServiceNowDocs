---
title: Patient Support Services data model
description: The Patient Support Services application provides a data model for use in the Patient Support Services workflow.
locale: en-US
release: australia
product: Patient Support Services
classification: patient-support-services
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Patient Support Services, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Patient Support Services data model

The Patient Support Services application provides a data model for use in the Patient Support Services workflow.

**Important:**

Starting with the Yokohama release, Patient Support Services is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported.

For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support knowledge base.

The Patient Support Services data model extends the Healthcare and Life Sciences data model.

The Patient Support Services data model uses a combination of tables to store data:

-   Tables that are included within the Patient Support Services application.
-   Tables that are included within the Healthcare and Life Sciences Service Management Core application.

You can install the Patient Support Services application to use its data model.

The Patient Support Services data model uses the following tables included within the Patient Support Services application to store data.

<table id="table_p3d_b42_ppb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Enrollment case \[sn\_patientservice\_enroll\_case\]

</td><td>

Stores the enrollment cases.

 The **Patient** field is mandatory for an enrollment case.

</td></tr><tr><td>

Patient service task \[sn\_patientservice\_task\]

</td><td>

Base task table from which Program Task \[sn\_patientservice\_program\_task\] and Program service item \[sn\_patientservice\_program\_service\_item\] tables are extended. Extends the Healthcare Task \[sn\_hcls\_task\] table.

</td></tr><tr><td>

Patient service training \[sn\_patientservice\_training\_task\]

</td><td>

Stores the details of the training tasks associated with a program task.

</td></tr><tr><td>

Program service item \[sn\_patientservice\_program\_service\_item\]

</td><td>

Stores the details of the program service item tasks associated with a program service.

</td></tr><tr><td>

Program Task \[sn\_patientservice\_program\_task\]

</td><td>

Stores the details of the program tasks created to fulfill services requested by a patient.

</td></tr></tbody>
</table>The Patient Support Services data model uses the following tables included within the Healthcare and Life Sciences Service Management Core application.

<table id="table_ygf_fbl_drb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Attribute \[sn\_hcls\_characteristic\_attribute\]

</td><td>

Stores the characteristics options associated with a program or program service selected by a patient when submitting an enrollment request.

</td></tr><tr><td>

Appointment \[sn\_hcls\_appointment\]

</td><td>

Stores the appointment booking details for a patient in your healthcare organization.

</td></tr><tr><td>

Healthcare case \[sn\_hcls\_case\]

</td><td>

Supports the healthcare case types.

</td></tr><tr><td>

Healthcare Task \[sn\_hcls\_task\]

</td><td>

Supports the healthcare tasks.

</td></tr><tr><td>

Program \[sn\_hcls\_program\]

</td><td>

Supports the program and training tasks.

</td></tr><tr><td>

Program service \[sn\_hcls\_program\_service\]

</td><td>

Supports the program service tasks.

</td></tr></tbody>
</table>For more information, see [Healthcare and Life Sciences data model](hcls-serv-mgmt-core-1.md).

