---
title: Create a grant program using Grants Management program setup for Public Sector Digital Services
description: Use the Public Sector Digital Services Grants Management program setup​ to either create a grant program, or create one from an existing configuration.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/government-industry/public-sector-digital-services/psds-gmp-using-set-up-grants-management-program.html
release: zurich
product: Public Sector Digital Services
classification: public-sector-digital-services
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
keywords: [Create a grant program, How to set up a grant program]
breadcrumb: [Set up a grant program, Grants Management Program Setup, Grants Management, Playbooks and solutions, Use, Public Sector Digital Services \(PSDS\)]
---

# Create a grant program using Grants Management program setup for Public Sector Digital Services

Use the Public Sector Digital Services Grants Management program setup​ to either create a grant program, or create one from an existing configuration.

## About this task

\[Omitted image "psds\_gmp-using-create-gp.png"\] Alt text: grant manager create grants program view

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **CSM Configurable Workspace**.

2.  Navigate to **Lists** &gt; **Grant Programs** &gt; **All** and select **New**.

    Here, you have the option to create a program from the default template, or start by copying data and configurations from an existing grant program.

    -   To create a grant program without using any pre-existing configurations, choose **New**.
    -   To copy data and configurations from a pre-existing grant program, choose **Create a new program from an existing program**. Choose the existing grant program from the drop-down menu and select **Continue**.

        You can determine which fields are copied over to the new grant program record, as well as fields in related records, including default fields. You can add or remove fields.

    A new grant program is created within the Grant Program table \(sn\_svc\_appl\_pgm\_mg\_grant\_program\), and the playbook is moved to the **Define Program** stage. A product model record, service definition record, and draft playbook content item have been automatically created for the grant program.

3.  Select **Save**.

4.  On the **Grant Program** form, fill in the details of the grant program.

<table id="table_rbc_wyy_t3c"><thead><tr><th>

Program information form fields

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Category

</td><td>

Category of the grant

</td></tr><tr><td>

Opportunity ID:

</td><td>

ID of the grant program

</td></tr><tr><td>

Program title:

</td><td>

Title of the grant program

</td></tr><tr><td>

Summary statement:

</td><td>

A summary of the grant program to be displayed to applicants.

</td></tr><tr><td>

Program start date

</td><td>

The start date of the program. Present and future dates are allowed.**Note:** The two-digit year format \(yy\) isn't supported. Use the dd/mm/yyyy format.

</td></tr><tr><td>

Program end date

</td><td>

The end date of the program. Present and future dates are allowed.

</td></tr></tbody>
</table>5.  Select **Mark Complete** to move to the next activity.


