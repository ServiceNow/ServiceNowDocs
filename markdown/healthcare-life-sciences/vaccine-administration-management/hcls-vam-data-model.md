---
title: Vaccine Administration Management data model
description: The Vaccine Administration Management application provides a data model that is used in the vaccine administration workflows.
locale: en-US
release: australia
product: Vaccine Administration Management
classification: vaccine-administration-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Reference, Vaccine Administration Management, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Vaccine Administration Management data model

The Vaccine Administration Management application provides a data model that is used in the vaccine administration workflows.

The Vaccine Administration Management data model extends the Healthcare and Life Sciences data model.

The Vaccine Administration Management data model uses a combination of tables to store data:

-   Tables that are included within the Vaccine Administration Management application.
-   Tables that are included within the Healthcare and Life Sciences Service Management Core application.
-   Tables that are from the Customer Service Management \(CSM\) application.
-   Tables that are from the ServiceNow AI Platform application.

You can install the Vaccine Administration Management application to use its data model.

The following diagram shows the tables and their relationships that comprise the Vaccine Administration Management data model.

![Infographic displaying the Vaccine Administration Management data model . For the text description, refer to the Vaccine Administration Management application tables section.](../image/hcls-vam-data-model.png "Vaccine Administration Management data model")

The Vaccine Administration Management data model uses the following tables included within the Vaccine Administration Management application to store data.

<table id="table_p3d_b42_ppb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Active Program Center \[sn\_vaccine\_sm\_st\_active\_program\_center\]

</td><td>

Stores the list of vaccination centers that are a part of a vaccine program and still in use.

</td></tr><tr><td>

Dosage \[sn\_vaccine\_sm\_dosage\]

</td><td>

Stores the details of vaccine dosages for a vaccination method.

</td></tr><tr><td>

Mass Booking Config \[sn\_vaccine\_sm\_mass\_booking\_config\]

</td><td>

Stores the list of configurations used to mass schedule vaccinations.

</td></tr><tr><td>

Mass Booking Job \[sn\_vaccine\_sm\_mass\_booking\_job\]

</td><td>

Stores mass booking job records including total number of booked appointments in the job, total vaccination tasks, and failed bookings when a mass appointment booking request is generated.

</td></tr><tr><td>

Method \[sn\_vaccine\_sm\_method\]

</td><td>

Stores the details of the methods available to vaccinate someone within a vaccination program.

</td></tr><tr><td>

Personal information \[sn\_vaccine\_sm\_personal\_info\]

</td><td>

Stores the information captured from the user during the vaccination sign-up process including occupation, demography, address, and identity document.

</td></tr><tr><td>

Phase \[sn\_vaccine\_sm\_phase\]

</td><td>

Stores the stages of a release that a vaccine program is in and when it’s available to administer. Includes the start date, end date, and additional eligibility criteria.

</td></tr><tr><td>

Program \[sn\_vaccine\_sm\_program\]

</td><td>

Stores the list of available programs used to administer vaccinations.

</td></tr><tr><td>

Program Center \[sn\_vaccine\_sm\_program\_center\_mtom\]

</td><td>

Stores the list of vaccination centers that are a part of a vaccine program.

</td></tr><tr><td>

Test result case \[sn\_vaccine\_sm\_test\_result\_case\]

</td><td>

Stores the details of a test result case including patient name, test date, expiration date, details of a vaccination program, and test result status.

</td></tr><tr><td>

Vaccination Appointment Booking Lock \[sn\_vaccine\_sm\_apptmnt\_booking\_lock\]

</td><td>

Stores the records that act as locks on appointment slots during the appointment booking procedure. The records are automatically deleted and locks are released for a slot when the appointment booking is completed

</td></tr><tr><td>

Vaccination Appointment Configuration \[sn\_vaccine\_sm\_appointment\_config\]

</td><td>

Stores configurations used for vaccination appointments.

</td></tr><tr><td>

Vaccination Center \[sn\_vaccine\_sm\_center\]

</td><td>

Stores details on vaccination centers, the vaccination center location, contact information, and the vaccination center stockroom.

</td></tr><tr><td>

Vaccination Questionnaire \[sn\_vaccine\_sm\_questionnaire\]

</td><td>

Stores the responses to a questionnaire sent to users who have booked a vaccination appointment.

</td></tr><tr><td>

Vaccination Request \[sn\_vaccine\_sm\_request\]

</td><td>

Stores all vaccination requests and the associated vaccination task number including who the request is for, the vaccination and program, and status.

</td></tr><tr><td>

Vaccination Schedule \[sn\_vaccine\_sm\_schedule\]

</td><td>

Stores all vaccination schedule details within an appointment.

</td></tr><tr><td>

Vaccination Task \[sn\_vaccine\_sm\_task\]

</td><td>

Stores all vaccination tasks included in vaccination requests.

</td></tr><tr><td>

Vaccine \[sn\_vaccine\_sm\_consumable\]

</td><td>

Stores the details on vaccine stock including information about the model, quantity, and availability.

</td></tr><tr><td>

Vaccine Availability \[sn\_vaccine\_sm\_supply\_availability\]

</td><td>

Stores the details on the availability of a vaccine including the center and date that the vaccine is available from, vaccine model, and allocated, booked,used, and wasted doses.

</td></tr><tr><td>

Vaccine Availability By Lot \[sn\_vaccine\_sm\_supply\_availability\_by\_batch\]

</td><td>

Stores the details about the supply lot associated with the vaccine availability including the date vaccine is available from and allocated doses.

</td></tr><tr><td>

Vaccine case \[sn\_vaccine\_sm\_case\]

</td><td>

Stores the vaccine cases.

</td></tr><tr><td>

Vaccine Management Diagnostic Reports \[sn\_vaccine\_sm\_diagnostic\_reports\]

</td><td>

Stores a list of registered users without any vaccination records. The table is populated when the **Vaccination management - Registered users without vaccination requests** scheduled job is run. By default, the scheduled job is inactive.

</td></tr><tr><td>

Vaccine Model \[sn\_vaccine\_sm\_product\_model\]

</td><td>

Stores the model of the vaccine including type, manufacturer, and model number.

</td></tr><tr><td>

Vaccine Status Information \[sn\_vaccine\_sm\_vaccine\_status\_information\]

</td><td>

Stores the vaccine status information including status of the vaccine, dosages administered, vaccine method, patient name, and proof key.

</td></tr><tr><td>

Vaccine Supply Lot \[sn\_vaccine\_sm\_supply\_batch\]

</td><td>

Stores the details about the lot for a vaccine added to the inventory including type, number of doses, and expiration date.

</td></tr></tbody>
</table>The Vaccine Administration Management data model uses the following tables included within the Healthcare and Life Sciences Service Management Core, and ServiceNow AI Platform, Customer Service Management \(CSM\) applications to store data.

<table id="table_ygf_fbl_drb"><thead><tr><th>

Table

</th><th>

Description

</th><th>

Application

</th></tr></thead><tbody><tr><td>

Appointment \[sn\_hcls\_appointment\]

</td><td>

Provides the appointment booking details for a patient.

</td><td>

Healthcare and Life Sciences Service Management Core

</td></tr><tr><td>

Consumable \[alm\_consumable\]

</td><td>

Provides assets associated with a vaccine.

</td><td>

ServiceNow AI Platform

</td></tr><tr><td>

Consumable model \[cmdb\_consumable\_product\_model\]

</td><td>

Provides descriptions of consumable product models.

</td><td>

ServiceNow AI Platform

</td></tr><tr><td>

Consumer \[csm\_consumer\]

</td><td>

Provides patient records associated with consumer records.

</td><td>

CSM

</td></tr><tr><td>

Healthcare case \[sn\_hcls\_case\]

</td><td>

Supports the healthcare case types including vaccine cases.

</td><td>

Healthcare and Life Sciences Service Management Core

</td></tr><tr><td>

Immunization \[sn\_hcls\_immunization\]

</td><td>

Provides the information about an event of a patient being administered a vaccine.

</td><td>

Healthcare and Life Sciences Service Management Core

</td></tr><tr><td>

Location \[cmn\_location\]

</td><td>

Provides addresses associated with a patient.

</td><td>

ServiceNow AI Platform

</td></tr><tr><td>

Patient \[sn\_hcls\_patient\]

</td><td>

Provides the details of a patient associated with vaccine records.

</td><td>

Healthcare and Life Sciences Service Management Core

</td></tr><tr><td>

Record Producer \[sc\_cat\_item\_producer\]

</td><td>

Provides the record producers for a vaccination program.

</td><td>

ServiceNow AI Platform

</td></tr><tr><td>

Schedule \[sn\_cmn\_schedule\]

</td><td>

Provides the holiday schedules in days and times to exclude from the appointment availability for a vaccine schedule.

</td><td>

ServiceNow AI Platform

</td></tr><tr><td>

Task \[task\]

</td><td>

Provides a series of standard task fields used on each of the tables that extend it.

</td><td>

ServiceNow AI Platform

</td></tr><tr><td>

User \[sys\_user\]

</td><td>

Provides a series of standard user fields used on each of the tables that extend it.

</td><td>

ServiceNow AI Platform

</td></tr></tbody>
</table>To learn about Healthcare and Life Sciences Service Management Core, ServiceNow AI Platform, and CSM tables, see [Healthcare and Life Sciences data model](../../healthcare-life-sciences/concept/hcls-serv-mgmt-core-1.md), [Industry data model tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/csm-data-model-tables.md), and [Tables installed with Customer Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/r_TIWCustomerService.md).

