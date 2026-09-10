---
title: Configure scripted extension points in Grants Management
description: The grants management application uses a scripted extension point to publish grant programs. Implementing this extension point in the correct application scope lets a grant program move to the Accepting Applications state so that contacts and constituents can submit proposals.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/government-industry/psds-config-gmp-fdtn-scripted-ext-pt.html
release: zurich
topic_type: task
last_updated: "2026-03-17"
reading_time_minutes: 2
breadcrumb: [Foundation, Grants Management, Playbooks and Solutions, Configure agent workspaces, Configure, Public Sector Digital Services \(PSDS\)]
---

# Configure scripted extension points in Grants Management

The grants management application uses a scripted extension point to publish grant programs. Implementing this extension point in the correct application scope lets a grant program move to the Accepting Applications state so that contacts and constituents can submit proposals.

## Before you begin

Role required: admin

The Grants Management application ships with the scripted extension point `sn_svc_appl_pgm_mg.PublishGrantProgram`. Before a grant program manager can publish a program, this extension point must be implemented in the Global scope and made accessible from all application scopes. Perform this procedure during Grants Management setup, before setting up a grant program. The publishing extension point must be implemented once per instance.

Set your application scope to **Global** by selecting the application picker \(\[Omitted image "globe-fill-24.svg"\]\) in the Unified Navigation bar and selecting **Application Scope** &gt; **Global**.

## Procedure

1.  Navigate to **All** &gt; **Scripted Extension Points** &gt; **Scripted Extension Points**.

2.  In the API name column, search for `sn_svc_appl_pgm_mg.PublishGrantProgram` and select the record.

3.  Under Related Links, select **Create Implementation**.

    The system creates and registers a new Script Include as an extension point instance.

    \[Omitted image "psds-gmp-scripted-extension.png"\] Alt text: create implementation view

4.  In the dropdown next to **Accessible from** field, select **All application scopes**.

5.  Select **Update**.

6.  Verify the implementation by publishing a grant program and confirming it moves to the **Accepting Applications** state.

    If you're creating a custom playbook, perform these additional steps to make sure you reference the intended playbook definition:

    1.  Open the intended playbook definition record and copy its `sys_id` from the record header menu or the record URL.

    2.  On the extension point implementation, set the **process\_definition** field to that `sys_id`.

        If the field is not on the form, add it by using form layout, or edit it from the record list.

    3.  Select **Update**.

    4.  Reopen the proposal and confirm the activity now appears.

        The activity list on a proposal is resolved from the playbook definition referenced in `process_definition`. If it points to a different playbook, such as the base-system proposal playbook, activities that exist only in the intended playbook don't display.


## Result

The publishing extension point is implemented. Grant program managers can now publish programs, which moves each program to the Accepting Applications state and makes it available to contacts for proposals.

**Parent Topic:**[Configure Grants Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/government-industry/psds-config-gmp-foundation.md)

**Previous topic:**[Configure Grants Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/government-industry/psds-config-gmp-foundation.md)

**Next topic:**[Configure Restricted Caller Access \(RCA\) for Document Templates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/government-industry/psds-config-gmp-fdtn-doc-template-rca.md)

