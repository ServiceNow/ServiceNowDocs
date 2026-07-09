---
title: Configure page security in the GDS Service Portal by role
description: Set up GDS Service Portal pages to be public, or filter them by role.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/government-industry/psds-config-gds-page-sec.html
release: australia
topic_type: task
last_updated: "2026-06-01"
reading_time_minutes: 2
breadcrumb: [Manage Portal Access by role, Configure UK GDS Service Portal, GOV.UK Developer Toolkit, Set up self-service, Configure, Public Sector Digital Services \(PSDS\)]
---

# Configure page security in the GDS Service Portal by role

Set up GDS Service Portal pages to be public, or filter them by role.

## Before you begin

Role required: admin or sp\_admin

## About this task

Public pages won't require a user login; anyone can access them. All other pages require user authentication.

By default, the GDS Service Portal [pre-login](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/psds-config-gds-registlogin.md) page is set to public. All other pages require authentication and the following roles \(snc\_external, snc\_internal\) to be viewed and accessed.

## Procedure

1.  In the Service Portal configuration page \(**Service Portal** &gt; **Service Portal Configuration**\), open the Page Editor.

2.  In the Select Page list, search for the page to apply page security to.

3.  Select the highest level node in the tree view.

4.  Configure page security.

    -   To make a page public, select the **Public** check box. All users can access pages marked as **Public**.
    -   To limit access to a certain role, add the roles in a comma separated list. Users without the role listed can see links to the page if they appear in the portal. Trying to open the page results in a "page not found" error.

        **Note:** If you select **Public** and add a list of roles, the page is still accessible by any user.

    -   To create a draft page that only administrators can see while the page is still in development, select **Draft**. Users must have the admin role to see any pages in draft. Users without the admin role see a "page not found" error.
5.  Select **Save**.


## What to do next

Follow the steps in [Configure widget security](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/psds-config-gds-widg-sec.md) to configure security for the widgets on your page.

**Parent Topic:**[Manage role-based access to pages and widgets in GOV.UK Design System Service Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/psds-config-gds-man-acc.md)

**Previous topic:**[Manage role-based access to pages and widgets in GOV.UK Design System Service Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/psds-config-gds-man-acc.md)

**Next topic:**[Configure widget security in the GDS Service Portal by role](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/psds-config-gds-widg-sec.md)

