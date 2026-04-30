---
title: Set up custom Playbooks for Portals
description: Create custom Playbooks for Portals to provide end users with the playbook experience on your service portal.Create a content item of Playbook type on portal so that users can navigate to the playbook experience. These content items are specifically configured to enable the playbook experience on portals.You can set up a widget to reroute the user to the csm\_ticket page once the record state changes from draft to new, indicating that the user has completed the intake process.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Playbooks for Portals, Playbooks in Customer Service Management, Agent tools, Organize agent workspaces, Configure, Customer Service Management]
---

# Set up custom Playbooks for Portals

Create custom Playbooks for Portals to provide end users with the playbook experience on your service portal.

## Overview of Playbooks

Playbooks guide users through complex processes and enable them to save their progress and resume their work when convenient. They can also get the information that they need for each stage of the flow and its associated activities with the Customer Service Management \(CSM\) playbooks on service portals.

You can activate Playbooks for Portals if you have the admin role. The base system is delivered in an inactive state. You must activate it in the Playbooks \(PAD\) for the user to see it.

Plugins required:

-   Playbooks for Customer Service Management: sn\_csm\_playbook
-   Playbook Experience: sn\_playbook\_exp
-   Case Playbook for Onboarding: sn\_onboarding \(required if you need the predefined playbook experience\)
-   Case Playbook for Product Support: sn\_product \(required if you want to use the product case playbook and record generator\)

Plugins are available from the ServiceNow® Store. For more information, see [Playbook plugins](customer-service-case-playbooks.md).

## Summary of steps for setting up Playbooks for Portals

You can set up Playbooks for Portals using the following high level steps.

1.  Define your process using Workflow Studio. See [Create a playbook](https://www.servicenow.com/docs/access?context=create-process-definition&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US) for more information.
2.  Activate the record generator. For more information, see [Activate the record generator](activate-the-record-generator.md).
3.  Set up ACLs \(Access Control Lists\) to provide the appropriate read, write, and create permissions for users. See [Explicit Roles in CSM](../../../administer/contextual-security/concept/explicit-roles-in-csm.md) for more information.

    **Note:** Add write and create roles with a condition based on "State=draft" so that users can only edit the fields in the draft state.

4.  Create a Playbook Content Item so that users can navigate to the Playbook experience. See [Create a Playbook Content Item](activate-playbooks-for-portals.md#) for more information.
5.  Set up a redirection widget so that users are redirected to the playbook intake experience once the state changes from "draft" to "new." See [Set up a redirection widget](activate-playbooks-for-portals.md#) for more information.

## Create a Playbook Content Item

Create a content item of Playbook type on portal so that users can navigate to the playbook experience. These content items are specifically configured to enable the playbook experience on portals.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Playbook Content Items** &gt; **New**.

    ![content item form showing all fields](../image/playbook-content-item.png "Content item form")

2.  In the form, fill out the fields.

<table id="table_bpj_hvr_1fc"><thead><tr><th>

Field

</th><th>

Definition

</th></tr></thead><tbody><tr><td>

Name

</td><td>

The name of the content item you are creating

</td></tr><tr><td>

Table

</td><td>

Map your table here

</td></tr><tr><td>

Record ID

</td><td>

Always enter -1

</td></tr><tr><td>

Playbook experience

</td><td>

The name of your playbook experience

</td></tr><tr><td>

Playbook experience record generator

</td><td>

Map your record generator

</td></tr><tr><td>

Portal page

</td><td>

`csm_intake` standard with the Playbooks for Customer Service Management application.**Note:** You can clone the `csm_intake` page and modify it per your requirements.

</td></tr><tr><td>

Title

</td><td>

Title that appears at the top of the page.

</td></tr></tbody>
</table>3.  Select **Submit**.


### What to do next

After completing this step, you can navigate to the portal where the catalog is mapped and execute the content item. The playbook intake experience opens, with the record generator mapped as the first activity.

## Set up a redirection widget

You can set up a widget to reroute the user to the `csm_ticket` page once the record state changes from draft to new, indicating that the user has completed the intake process.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Service Portal** &gt; **Widgets**.

2.  Open the widget **CSM Intake Redirect**.

3.  Add the following code the in the client controller section.

    **Note:** As a best practice, clone the **CSM Intake Redirect** widget to modify and replace it on the `csm_intake` page, or on your custom page.

    ```
    spUtil.recordWatch($scope, 'sn_customerservice_case', c.data.filter, function(response) { //replace sn_customerservice_case with your table.
    
            if (response.data.operation == "update" && response.data.record.state && response.data.record.state.value != "0") { //checking if the state is not draft
    
                if (($window.location.href).indexOf('?id=csm_ticket&') == -1);
                $window.location = "?id=csm_ticket&table=" + c.data.table + "&sys_id=" + c.data.sys_id;
            }
        });
    ```

4.  Select **Update**.


