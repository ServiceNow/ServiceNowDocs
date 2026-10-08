---
title: Configure the applicant information form for a grant program
description: Select the form that the Applicant must submit when creating a proposal.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/government-industry/psds-config-gmp-applicant-info-form.html
release: zurich
topic_type: task
last_updated: "2026-04-01"
reading_time_minutes: 1
breadcrumb: [Set up a grant program, Grants Management, Playbooks and Solutions, Configure agent workspaces, Configure, Public Sector Digital Services \(PSDS\)]
---

# Configure the applicant information form for a grant program

Select the form that the Applicant must submit when creating a proposal.

## About this task

The Applicant Information Form Activity allows the Grant Program Manager to select the form that the Applicant must submit when creating a proposal. The Grant Program Manager has access to the Form Builder, where they can either configure an existing form or create a new form on the Applicant table.

By default, Grants Management includes a generic applicant information form \(ApplicantIntakeGrantCase\) which can be modified using Form Builder to meet your agency's needs. You can also create a new form.

## Before you begin

Role required: admin

## Procedure

1.  In the Grant Setup Playbook Applicant Information form activity, select **Open the form builder** to open Form Builder to the applicant information form.

2.  Select **Add new form view** to add a new form, or duplicate the default form by selecting **Duplicate this form view**.

    **Note:** When creating a new form, confirm there are a minimum of two form sections added.

3.  Add the form view name and select **Create**.

4.  Select **Add a field in the table** to create a field, then and drag the field onto the form canvas.

    **Note:** Only fields which are present on the Applicant Table \("sn\_svc\_appl\_info\_applicant"\) or the fields that are referenced from this table can be added to this table. To add a field that is a not default field, it must first be added on to the table.

5.  Select **Save**, and verify that the form appears as expected.


## Result

The new form view appears in the Applicant information form field dropdown.

**Parent Topic:**[Set up a grant program in Grants Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/government-industry/psds-config-gmp-grant-pgr.md)

**Previous topic:**[Configure point-in-time content for a grants program in Grants Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/government-industry/psds-config-gmp-point-in-time-content.md)

**Next topic:**[Configure the Spending Overview Widget and Filter pills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/government-industry/psds-gm-config-spending-overview-widget.md)

