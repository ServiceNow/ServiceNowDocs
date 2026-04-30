---
title: Add a workspace action button for initiating a contract request
description: Define an action button in your workspace and map it to the built-in action that initiates a contract request.
locale: en-US
release: zurich
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
keywords: [Initiate contract, Initiate contract button, Initiate contract action, Uptake steps for initiate contract, BU configuration]
breadcrumb: [Configure CM Pro for your workspace, Configure, Contract Management Pro, Legal and Contract Operations, Employee Service Management]
---

# Add a workspace action button for initiating a contract request

Define an action button in your workspace and map it to the built-in action that initiates a contract request.

## Before you begin

Role required: admin

## Procedure

1.  Add initiate contract request functionality to your workspace.

    1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **Declarative Actions** &gt; **Form Actions**

        For more information, see [Customizing Configurable Workspace with declarative actions](https://www.servicenow.com/docs/access?context=declarative-actions-landing&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US)

    2.  Select **New**.

    3.  Set the action to the type UXF client action and map the action to the initiate contract request functionality and by entering the following field values.

        |Field|Value|
        |-----|-----|
        |Implemented as|UFX Client Action|
        |Specify client action|Initiate contract|

        ![Add initiate contract declarative action to your workspace](../image/cmpro-bu-form-actn-initiate-cntr.png)

    4.  On the form, fill in the other fields.

        For details, see [Action assignment form](../reference/cmpro-actn-assignment-form.md)

    5.  Right-click the form header and select **Save**.

2.  Create an event mapping for the initiate contract declarative action.

    1.  Select **Advanced view** listed under Related Links.

    2.  Select UX Add-on Event Mappings related list.

    3.  Select **New**.

    4.  In the Source Component field, select Action bar.

    5.  In the Source Declarative Action field, select initiate\_contract.

    6.  In the Controller field, select Form.

    7.  In the Target Event field, select \[Record Page\] Open modal.

    8.  In the **Target Payload Mapping** field, define the fields to send by pasting the following JSON code.

        ```
        {
            "container": {
                "fields": {
                    "binding": {
                        "address": [
                            "fields"
                        ]
                    },
                    "type": "EVENT_PAYLOAD_BINDING"
                },
                "params": {
                    "binding": {
                        "address": [
                            "params"
                        ]
                    },
                    "type": "EVENT_PAYLOAD_BINDING"
                },
                "route": {
                    "binding": {
                        "address": [
                            "route"
                        ]
                    },
                    "type": "EVENT_PAYLOAD_BINDING"
                }
            },
            "type": "MAP_CONTAINER"
        }
        ```

    9.  On the form, fill in the other fields.

        ![Create event mapping for initiate contract action](../image/cmpro-uptake-ux-add-event.png)

        For a description of the field values, see [UFX Add on Event mapping form](../reference/cmpro-ufx-event-map-form.md).

    10. Select **Submit**.

3.  Configure visibility conditions for initiate contract action button.

    1.  Select **Advanced view** listed under Related Links.

    2.  Select to the Conditions related list.

    3.  Set the conditions for the visibility of the action button.


## Result

An action button to initiate contract requests from a contract record is available in your workspace.

![Initiate action button added to your workspace](../image/cmpro-bu-initiate-contract-button.png "Initiate contract action configured")

**Parent Topic:**[Add and configure contract request functionality into your workspace](../concept/cncore-uptake-steps.md)

**Related topics**  


[Configure non-task tables for contract templates](cmpro-config-non-tsk-tbl-cn-tmplt.md)

[Add Contract requests tab to the contract request record](cncore-add-relatedlist-conreq.md)

[Add amendment tabs to contract repository record](cncore-BU-amend-relatedlist.md)

[Add Contract documents tab to the contract repository record](cncore-add-con-doc-relatedl.md)

[Copy fields from parent request to contract request](cncore-copy-fld-frm-parent.md)

[Group contract documents by contract type in a contract request](cncore-config-srp-grouping.md)

[Add access to obligation management from contract repository records](cmpro-add-access-to-ob-mgmt.md)

[Configure the contract request form header for your workspace](cncore-configure-header.md)

[Assign a role for configuring template mappings](cncore-tbl-access-config-role.md)

[Enable contract request fields in condition builders](cncore-add-cmr-condtion-build.md)

[Configuring the Playbook tab on contract repository records](cmpro-config-playbook-tab.md)

