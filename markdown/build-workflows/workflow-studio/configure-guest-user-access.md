---
title: Configure guest user access to playbooks
description: Set up a playbook, public audience record, and UI experience so that guest users can run playbooks without a ServiceNow login through a public URL.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/build-workflows/workflow-studio/configure-guest-user-access.html
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2026-06-11"
reading_time_minutes: 3
breadcrumb: [Design Playbook Experience, Playbooks, Workflow Studio, Build workflows]
---

# Configure guest user access to playbooks

Set up a playbook, public audience record, and UI experience so that guest users can run playbooks without a ServiceNow login through a public URL.

## Before you begin

Role required: playbook.admin, pd\_author, playbook.write, ui\_builder\_admin, admin

An admin must create a public table to receive guest-submitted records. The public table must be registered in `sys_public`, have the **public** role applied, and have create ACLs configured. For more information, see **Configure tables to work with guests**.

**Note:** Standalone playbooks can't be configured for guest user access. The playbook must use a public table as its parent table.

## Procedure

1.  In Workflow Studio configure a record driven playbook with a parent table to permit public access.

    Playbooks must be configured to be publicly accessible when you create them. You can't change a playbook to be embedded on public pages later.

    1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

    2.  Select **New** and **Playbook**.

    3.  On the form, fill in the fields.

        |Field|Action|
        |-----|------|
        |Type|Select **Standard playbook**.|
        |Playbook name|Enter a unique, user-facing name for your playbook. This name appears to agents and fulfillers during runtime of your playbook.|
        |Now assist input|Enter a short description about your playbook.|
        |Application|Choose an application scope that you want your playbook to run in. Selecting **Global** lets your playbook run in any application scope. For more information, see Application scope.|
        |Execution type|Select **Record driven** to tie the playbook to a public record. You can't make a standalone playbook public.|
        |Parent table|Set the parent table to the public table you created as the prerequisite. This field is activated when you select Record driven Execution type.|
        |Allow this playbook to be publicly accessible and embedded on public pages|Select this option to permit embedding the playbook on public pages. The playbook can be made public only after embeddables setup is complete.|

        \[Omitted image "pe-guest-1.png"\] Alt text: Screenshot showing the required fields for a guest user playbook.

    4.  Select **Generate playbook preview**.

    5.  Review the generated playbook, and select **Save and edit playbook**.

    The builder displays in **Diagram view**.

2.  Configure the trigger for the publicly accessible playbook.

    1.  On the left sidebar of the **Diagram view**, select the **Triggers** icon \(\[Omitted image "triggers-icon.png"\]\).

    2.  Select **Add trigger**.

    3.  Under **Record based**, select **When record is created**.

        \[Omitted image "pe-guest-2.png"\] Alt text: Screenshot showing the menu flow to add the trigger When record is created.

    4.  Enter a label for the trigger.

    5.  Select **Save and close**.

    6.  Select **Activate** so the playbook runs when its related form is created or updated on your development instance.

3.  Create a public audience record.

    1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **Building Blocks** &gt; **Audiences**.

    2.  Select **New**.

    3.  Enter a descriptive **Name**.

    4.  Select the **Unlock roles** icon \(\[Omitted image "lock-outline-24.svg"\]\) and add the **public** role to the audience.

        The public role allows users without a ServiceNow login to be included in this audience.

    5.  Select **Submit**.

4.  Create a page in UI Builder to host the playbook experience, and assign the public audience to the page to designate it for guest users without authentication.

    1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder** &gt; **Experiences**.

    2.  Select an existing Experience or create an Experience to work in.

    3.  Select the **+** icon next to **Pages** to create a page.

    4.  Select **Create a new page**.

    5.  On the **Select a template** screen, choose one:

        -   To use the Standard record template, select the **Standard record template** tile, then confirm by selecting **Use template**.
        -   To start with an empty page, select **Create from scratch instead**.
    6.  Enter a **Name**, review generated URL path, parameters, and select **Looks Good**.

    7.  In the Tell us about your variant window, select **+ Add** next to **Audiences**.

    8.  Search for and select the public audience you created in step 3.

    9.  Select **Create**.

    The page opens in UI Builder. Configure the user experience according to your requirements.

5.  Add a route ACL to grant the public role access to the page's route.

    1.  **All** &gt; **System Security** &gt; **Access Control \(ACL\)**

    2.  Select **New**.

    3.  On the form, fill in the fields.

<table id="table_smw_zcm_pjc"><thead><tr><th>

Field

</th><th>

Action

</th></tr></thead><tbody><tr><td>

Type

</td><td>

Select **ux\_route**.

</td></tr><tr><td>

Name

</td><td>

Enter the page's path with each forward slash replaced by a period. **Note:** For example, the path `now/myapp/test-form` becomes `now.myapp.test-form`.

</td></tr><tr><td>

Requires role

</td><td>

Under **Conditions**, in the **Requires role** section, add the **public** role.

</td></tr></tbody>
</table>    4.  Select **Submit**.

6.  Test the guest user experience.

    1.  Open the experience URL in an incognito or private browser window to simulate a guest user session.

    2.  Submit a record through the experience and confirm that the playbook starts and displays stages and activities.


