---
title: Add a script include method for the Playbook tab
description: Add a script include method that controls the Playbook tab visibility on the contract repository record by verifying plugin availability and applying conditional logic.
locale: en-US
release: zurich
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2025-11-25"
reading_time_minutes: 1
breadcrumb: [Configure the Playbook tab, Configure CM Pro for your workspace, Configure, Contract Management Pro, Legal and Contract Operations, Employee Service Management]
---

# Add a script include method for the Playbook tab

Add a script include method that controls the **Playbook** tab visibility on the contract repository record by verifying plugin availability and applying conditional logic.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Script Includes**.

    The Script Includes table appears.

2.  In the **Name** column, search for the Script Include where you want to add the method.

3.  Open the Script Include record.

    ![Script include form to add the wrapper method](../image/cmpro-playbook-method.png "Script include form")

4.  In the **Script** box, add the following method.

    ```
    hidePlaybookTab(table, sysId) { 
                            var pMgr = new GlidePluginManager(); 
                            if (pMgr.isActive("com.sn_cm_gen_ai")) { 
                            return new sn_cm_gen_ai.ContractsMetadataExtractionHelper().hidePlaybookTab(table, sysId);  
                            }  
                            return true;  
                            },
    ```

    This method checks if the Now Assist in Contract Management \(com.sn\_cm\_gen\_ai\) plugin is active. If the plugin is not active, it returns `true` hiding the tab by default.

5.  Select **Update**.


**Parent Topic:**[Configuring the Playbook tab on contract repository records](cmpro-config-playbook-tab.md)

