---
title: Components installed with Vaccine Administration Management
description: Several types of components are installed with Vaccine Administration Management, including user roles and tables.
locale: en-US
release: australia
product: Vaccine Administration Management
classification: vaccine-administration-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Reference, Vaccine Administration Management, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Components installed with Vaccine Administration Management

Several types of components are installed with Vaccine Administration Management, including user roles and tables.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see [Find components installed with an application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/find-components.md).

## Roles installed

<table id="table_jd3_lkx_h4b"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Vaccine Administration Management admin

 \[sn\_vaccine\_sm.admin\]

</td><td>

Application-specific admin for Vaccine Administration Management.

**Important:** By default, the admin role contains the sn\_vaccine\_sm.admin role. The sn\_vaccine\_sm.admin role should be reassigned to another user and then removed from the admin role. This process protects sensitive application data by restricting access to the application.

</td><td>

-   sn\_vaccine\_sm.clinician
-   sn\_vaccine\_sm.manager
-   sn\_apptmnt\_booking.appointment​\_booking\_manager

</td></tr><tr><td>

Clinician

 \[sn\_vaccine\_sm.clinician\]

</td><td>

Can create, read, and update vaccination requests, vaccination tasks, and vaccination questionnaires.

</td><td>

-   sn\_vaccine\_sm.viewer
-   agent\_workspace\_user
-   sn\_apptmnt\_booking.appointment​\_booking\_manager
-   sn\_hcls.practitioner

</td></tr><tr><td>

Vaccine Administration Management manager

 \[sn\_vaccine\_sm.manager\]

</td><td>

Can create, read, and update vaccination programs, phases, centers, methods, and dosages.

</td><td>

-   sn\_vaccine\_sm.viewer
-   sn\_vaccine\_sm.model\_manager
-   agent\_workspace\_user
-   sn\_apptmnt\_booking.appointment​\_booking\_admin

</td></tr><tr><td>

Vaccine Administration Management model manager

 \[sn\_vaccine\_sm.model\_manager\]

</td><td>

Can create, read, and update vaccine models and vaccine consumables.

</td><td>

-   sn\_vaccine\_sm.model\_viewer

</td></tr><tr><td>

Vaccine Administration Management model viewer

 \[sn\_vaccine\_sm.model\_viewer\]

</td><td>

Read-only access to vaccine models and vaccine consumables.

</td><td>

None

</td></tr><tr><td>

Vaccine Administration Management viewer

 \[sn\_vaccine\_sm.viewer\]

</td><td>

Read-only access to vaccination programs, phases, centers, methods, and dosages.

</td><td>

sn\_vaccine\_sm.model\_viewer

</td></tr><tr><td>

Vaccine Administration Management self-service portal user

 \[sn\_vaccine\_sm.user\]

</td><td>

Can request a vaccination and manage appointments.

</td><td>

sn\_apptmnt\_booking.appointment\_booking\_user

</td></tr><tr><td>

Vaccine Administration Management dashboard manager

 \[sn\_vaccine\_sm.report\_manager\]

</td><td>

Can read and edit the appointment dashboard.

</td><td>

sn\_vaccine\_sm.report\_viewer

</td></tr><tr><td>

Vaccine Administration Management dashboard viewer

 \[sn\_vaccine\_sm.report\_viewer\]

</td><td>

Can read the appointment dashboard.

</td><td>

None

</td></tr><tr><td>

Vaccine Administration Management inventory manager

 \[sn\_vaccine\_sm.inventory\_manager\]

</td><td>

Can maintain vaccine supply information and distribution.

</td><td>

sn\_vaccine\_sm.inventory\_viewer

</td></tr><tr><td>

Vaccine Administration Management inventory viewer

 \[sn\_vaccine\_sm.inventory\_viewer\]

</td><td>

Can read the vaccine inventory management tables.

</td><td>

None

</td></tr></tbody>
</table>## Tables installed

<table id="table_kks_2gc_34b"><thead><tr><th>

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
</table>