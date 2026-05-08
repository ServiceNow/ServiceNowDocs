---
title: Redox Electronic Health Record Spoke
description: Enable communications with your customers using the Redox platform from your ServiceNow instance. Also reuse this short description in the release notes.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Redox Electronic Health Record Spoke

Enable communications with your customers using the Redox platform from your ServiceNow instance.

**Important:**

Starting with the Yokohama release, Redox Electronic Health Record Spoke is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported.

For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support knowledge base.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

Redox Electronic Health Record Spoke v1.0.3 is the current version.

## Key features

The Redox Electronic Health Record Spoke enables a hospital, payer \(insurance\), or life sciences company to:

-   Enable interoperability with an electronic medical record \(EMR\) or another healthcare system by leveraging the ServiceNow Healthcare and Life Sciences data model that is based on the Health Insurance Portability and Accountability Act \(HIPAA\) and the Health Level Seven International \(HL7\) industry standards. For more information, see Healthcare and Life Sciences data model.
-   Improve patient care and reduce cost by reducing data duplicity and entry.
-   Connect to the healthcare ecosystem by enabling patient-centric workflows.

## Spoke requirements

-   Administrator access to the Redox Dashboard.
-   **API Key** and **Source Secret**. You can find these values in the dashboard of your Redox account. For more information, see [Authenticate an API key](https://docs.redoxengine.com/how-to/send-and-manage-requests/authenticate-an-api-key) in the [Redox documentation](https://docs.redoxengine.com/).

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   ServiceNow Integration Hub Runtime \(com.glide.hub.integration.runtime\)
-   ServiceNow IntegrationHub Action Step - REST \(com.glide.hub.action\_step.rest\)
-   Complex Object \(com.glide.cobject\)

**Note:** Some of these plugins are licensable features and require appropriate licenses, if used outside the spoke implementation.

## Spoke actions

The Redox Electronic Health Record Spoke provides actions to automate Redox tasks when events occur in your ServiceNow instance. Available actions include:

<table id="table_a5c_wj2_tsb"><thead><tr><th>

Category

</th><th>

Action

</th><th>

Description

</th></tr></thead><tbody><tr><td rowspan="6">

Scheduling

</td><td>

Create Appointment

</td><td>

Creates a new appointment.

</td></tr><tr><td>

Reschedule Appointment

</td><td>

Reschedules an existing appointment.

</td></tr><tr><td>

Modify Appointment

</td><td>

Modifies an existing appointment.

</td></tr><tr><td>

Cancel Appointment

</td><td>

Cancels an existing appointment.

</td></tr><tr><td>

Look up Booked Appointments

</td><td>

Queries and returns booked appointments within a given time range.

</td></tr><tr><td>

Look up Available Slots

</td><td>

Queries and returns times available for booking an appointment within a given time range.

</td></tr><tr><td rowspan="3">

Clinical Summary

</td><td>

Look up Latest Clinical Summary

</td><td>

Queries and returns the most recent clinical summary for a given patient at the specified health system.

</td></tr><tr><td>

Look Up Visit Summary

</td><td>

Queries and returns visit summaries for a given patient at the specified health system within the specified time frame.

</td></tr><tr><td>

Send Visit Information

</td><td>

Sends a visit summary to another application or to an EHR.

</td></tr><tr><td rowspan="4">

Media

</td><td>

Create Media Document

</td><td>

Adds a new media document to the patient's chart.

</td></tr><tr><td>

Replace Media Document

</td><td>

Replaces a media document that was previously added to the patient's chart.

</td></tr><tr><td>

Delete Media Document

</td><td>

Deletes a media document that was previously added to the patient's chart.

</td></tr><tr><td>

Look Up Media Documents

</td><td>

Queries and returns media documents based on the specified filter criteria.

</td></tr><tr><td rowspan="4">

Notes

</td><td>

Create Note Document

</td><td>

Adds a new note document to the patient's chart.

</td></tr><tr><td>

Replace Note Document

</td><td>

Replaces a note document that was previously added to the patient's chart.

</td></tr><tr><td>

Delete Note Document

</td><td>

Deletes a note document that was previously added to the patient's chart.

</td></tr><tr><td>

Look Up Note Documents

</td><td>

Queries and returns note documents based on the specified filter criteria.

</td></tr><tr><td rowspan="3">

Patient Education

</td><td>

Send Patient Education

</td><td>

Adds education assignments to a patient's chart.

</td></tr><tr><td>

Send Patient Update

</td><td>

Updates education assignments in a patient's chart.

</td></tr><tr><td>

Send Patient Education Delete

</td><td>

Removes education assignments from a patient's chart.

</td></tr><tr><td rowspan="2">

Patient Admin

</td><td>

Look up Patient Demographics and Visit Information

</td><td>

Queries and returns patient demographics and visit information.

</td></tr><tr><td>

Look up Admitted Patients

</td><td>

Queries and returns all currently admitted patients from a facility.

</td></tr><tr><td>

Referral

</td><td>

Update Referral

</td><td>

Modifies a referral.

</td></tr><tr><td rowspan="2">

Result

</td><td>

Look up Results

</td><td>

Queries and returns results of diagnostic tests including labs, radiology, and imaging.

</td></tr><tr><td>

Pull Diagnostic Info

</td><td>

Displays a diagnostic result message.

</td></tr><tr><td rowspan="2">

Vaccination

</td><td>

Look up Patient Vaccinations

</td><td>

Queries and returns patient's vaccinations based on demographic data.

</td></tr><tr><td>

Look Up Vaccine Administration

</td><td>

Queries and returns vaccine administration information.

</td></tr><tr><td>

Patient Search

</td><td>

Look Up Patient

</td><td>

Queries and returns an existing patent record.

</td></tr></tbody>
</table>## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection. For more information, see Connections and Credentials.

For information about setting up the spoke, see [Set up the Redox Electronic Health Record Spoke](../task/redox-setup.md#).

