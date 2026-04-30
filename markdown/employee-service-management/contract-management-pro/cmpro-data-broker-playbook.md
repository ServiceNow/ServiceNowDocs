---
title: Add a data broker server script for the Playbook tab
description: Configure a data broker server script that connects the UI Builder component to the script include method controlling the Playbook tab visibility.
locale: en-US
release: zurich
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2025-11-25"
reading_time_minutes: 1
breadcrumb: [Configure the Playbook tab, Configure CM Pro for your workspace, Configure, Contract Management Pro, Legal and Contract Operations, Employee Service Management]
---

# Add a data broker server script for the Playbook tab

Configure a data broker server script that connects the UI Builder component to the script include method controlling the **Playbook** tab visibility.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to the **All** menu and enter `sys_ux_data_broker_transform.list`.

    The Data Broker Server Scripts table appears.

2.  Select **New**.

    The Data Broker Server Script form opens.

    ![Data Broker Server Script form displaying sample values to configure for the playbook visibility.](../image/cmpro-data-broker-playbook.png "Data Broker Server Script form")

3.  In the **Name** field, enter the name for your configuration.

4.  In the **Application** field, select the appropriate application scope for your implementation.

5.  In the **Description** field, enter a description.

    For example, `Whether to show or hide the Playbook tab on the Legal Counsel Center`

6.  In the **Properties** field, add the following JSON configuration:

    ```
    [{
                            "name": "table",
                            "label": "Table",
                            "fieldType": "string",
                            "mandatory": true
                            },
                            {
                            "name": "sysId",
                            "label": "Sys ID",
                            "fieldType": "string",
                            "mandatory": true
                            }]
    ```

7.  In the **Script** field, add the script for the data broker.

    Example:

    ```
    function transform(input) {
                            var table = input.table;
                            var sysId = input.sysId;
                            if (!table || !sysId) return true;
                            
                            return sn_lg_cf_workspace.LegalUIBWorkspaceDataBrokerHelper.hidePlaybookTab(table, sysId);
                            }
    ```

    This function receives the table and sysId from the input, validates them, and calls the helper method to determine tab visibility.

8.  Select **Update** to save the data broker server script.


**Parent Topic:**[Configuring the Playbook tab on contract repository records](cmpro-config-playbook-tab.md)

