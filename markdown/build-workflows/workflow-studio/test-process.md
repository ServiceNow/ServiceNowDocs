---
title: Test a playbook
description: Verify that your playbook works as expected by running the playbook with test trigger data. Identify and resolve all errors before activating your playbook.
locale: en-US
release: zurich
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Playbooks in Workflow Studio, Building playbooks, Use, Workflow Studio, Build workflows]
---

# Test a playbook

Verify that your playbook works as expected by running the playbook with test trigger data. Identify and resolve all errors before activating your playbook.

## Before you begin

-   Set up an application in Guided Application Creator to store Playbooks content.
-   [Create a playbook](create-process-definition.md)
-   Role required: the admin, playbook.admin, or pd\_operator roles grant users access to test playbooks and to view process execution records.
-   The Playbook Experience plugin is required to preview a playbook in runtime.
-   Plugin required: the Playbook Experience \(sn\_playbook\_exp\) plugin grants users access to test playbooks and to preview playbooks in runtime. Users need a role to view process execution records.

## About this task

Testing a playbook bypasses the normal playbook trigger to run it with the sample data you provide. Every test you run creates or changes records on your instance. To avoid unwanted record changes, test playbooks on a non-production instance that contains relevant demonstration data.

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio** &gt; **Playbooks**.

    The Playbooks landing page appears.

2.  Open the playbook you want to test.

    The playbook details screen appears.

3.  Select **Test**.

    The system displays the Test your process modal. The contents of the modal depend on the type of trigger record your playbook uses.

4.  Select a playbook trigger record to use for testing.

    **Note:** Testing ignores the playbook trigger conditions. You can select any existing record for testing. If there are no existing records to select, you can create a test record.

    The playbook runs as if the selected test record met the playbook trigger conditions.

5.  Create a test record.

    1.  In the **Test your process modal**, select **Create a new record**.

        In a new browser tab, the system opens a create record form in the ServiceNow AI Platform.

    2.  Enter the new record values.

        The fields of a record vary depending on what table your playbook is triggered from.

    3.  Select **Submit**.

        The system creates the record with the values you specified.

    4.  Return to the Workflow Studio browser tab with the **Test your process** modal open in the Playbooks builder.

    5.  Close or cancel the **Test your process** modal.

    6.  Repeat steps 2-4 and select the test record you created.

    **Note:** The system only displays the **Create a new record** option when there are no records in the table.

6.  Select **Run Test**.

    The system runs the playbook using the record you selected as test data. When the test is complete, the system displays options to view process execution details and a playbook preview.

7.  **View** the **Process execution details** for information about the playbook state, activities run, and log messages produced.

    **Note:** This option is only visible to users with the admin, playbook.admin, pd\_operator roles.

    The system opens a Process Execution form in a new tab.

8.  To see the **Playbook preview**:

    1.  Select a playbook experience type.

    2.  Select **View**.

    **Note:** This option is only visible on instances where the Playbook Experience plugin is activated.

    The system opens a sample playbook in a new tab.

9.  Identify and resolve any errors in your playbook.

10. Update and test your playbook until it is ready for release.


## What to do next

Publish your playbook to a production instance and activate it.

**Parent Topic:**[Playbooks in Workflow Studio](../concept/process-definitions.md)

**Related topics**  


[Create a playbook](create-process-definition.md)

[Playbook variants](../concept/playbook-variants.md)

[Restart](../concept/restart.md)

[Duplicate Playbooks](duplicate-process.md)

[Add translations for playbooks](add-translations-playbooks.md)

[View all buttons without hover](view-all-buttons-without-hover.md)

