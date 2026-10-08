---
title: Configure point-in-time content for a grants program in Grants Management
description: Establish point-in-time content, such as disclaimers, which are crucial for the Grants Management Sign and Submit Playbook Activity.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/government-industry/psds-config-gmp-point-in-time-content.html
release: zurich
topic_type: task
last_updated: "2026-03-29"
reading_time_minutes: 2
breadcrumb: [Set up a grant program, Grants Management, Playbooks and Solutions, Configure agent workspaces, Configure, Public Sector Digital Services \(PSDS\)]
---

# Configure point-in-time content for a grants program in Grants Management

Establish point-in-time content, such as disclaimers, which are crucial for the Grants Management Sign and Submit Playbook Activity.

## About this task

Create point in time content, such as disclaimers, so that you can provide constituents an opportunity to make attestations before signing the form. Disclaimer information is stored in the ‘Point in time content’ table \(sn\_svc\_appl\_info\_pitc\).

The terms and conditions are configured through the **Terms and Conditions** activity in the Configure Application stage of Grant Program setup. The grant program manager can also create a new set of terms and conditions for a record.

There are two ways through which a Grant Program Manager can create new terms and conditions:

-   Navigate to **CSM Workspace** &gt; **Terms &amp; Conditions**
-   Select the link in the **Terms and Conditions** activity

Set the table to Grants Management Case and the field name to "disclaimer”. The product field needs to be set as the product model related to the Grant Program.

**Note:** Each Grant Program requires its own Point in Time content record. If you wish to have the same T&amp;Cs for multiple Program records, you can clone the point in time content record and replace the Grant Program in the new record.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **CRM Workspace** &gt; **Terms and conditions**.

2.  Select **New**.

3.  On the form, fill in the fields.

<table id="table_rzc_53g_t3c"><thead><tr><th>

 

</th><th>

 

</th></tr></thead><tbody><tr><td>

Title

</td><td>

Disclaimer for \[Grants Program Name\]

</td></tr><tr><td>

Table

</td><td>

Grants Management Case

</td></tr><tr><td>

Field Name

</td><td>

Disclaimer

</td></tr><tr><td>

Product

</td><td>

Grants Management Product Model

</td></tr><tr><td>

Service Definition

</td><td>

Grants Management Program service definition

</td></tr><tr><td>

Content

</td><td>

I understand that by signing this application under penalty of perjury \(making false statements\), that:-   I read or had read to me, the information in this application and my answers to the questions in this application.
-   My answers to the questions are true and complete to the best of my knowledge.
-   Any answers I may give throughout the application process will be true and complete to the best of my knowledge.
-   I read, or had read to me, the Program Rules and Penalties.
-   I understand that giving false or misleading statements or misrepresenting, hiding, or withholding facts to establish eligibility is fraud and that I may be penalized under federal law if I provide false or untrue information. Fraud can cause a criminal case to be filed against me, and/or I may be barred for a period \(or life\) from receiving benefits and cash assistance.
-   I understand that identity information for household members applying for benefits may be shared with the appropriate government agencies as federal law requires.


</td></tr></tbody>
</table>    **Note:** If you want to have the same T&amp;Cs for multiple grant programs, you can clone the point in time content record and replace the Grant Program name in the new record.

4.  Right select the header to open the context menu, then select **Save**.

5.  Select **Publish**, then select **Update**.

    These set of terms and conditions would be available for selection for a grant program only after they are published.


## Result

After the state of the Terms and conditions is changed to published, they are available for selection in the ”Terms and conditions” activity of a Grant Program.

**Parent Topic:**[Set up a grant program in Grants Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/government-industry/psds-config-gmp-grant-pgr.md)

**Previous topic:**[https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/government-industry/psds-config-gmp-calendar-period.md](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/government-industry/psds-config-gmp-calendar-period.md)

**Next topic:**[Configure the applicant information form for a grant program](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/government-industry/psds-config-gmp-applicant-info-form.md)

