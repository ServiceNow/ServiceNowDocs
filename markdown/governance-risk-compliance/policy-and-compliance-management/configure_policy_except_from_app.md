---
title: Configure policy exceptions from other applications
description: Before you can request policy exceptions from applications other than Policy and Compliance Management, you must add a UI action for making the request and, optionally, create a new list view to see policy exception target records on the Policy Exception form.
locale: en-US
release: australia
product: Policy and Compliance Management
classification: policy-and-compliance-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Allow policy exception requests, Enhancement steps, Implement, Policy and Compliance Management, Governance, Risk, and Compliance]
---

# Configure policy exceptions from other applications

Before you can request policy exceptions from applications other than Policy and Compliance Management, you must add a UI action for making the request and, optionally, create a new list view to see policy exception target records on the Policy Exception form.

## Before you begin

Role required: sn\_compliance.manager, ui\_action\_admin or admin

The GRC business user \(sn\_grc.business\_user\) or business user – lite \(sn\_grc.business\_user\_lite\) is the minimum required role to raise a policy exception from an upstream application.

## About this task

Starting with Version 10.1 of Policy and Compliance Management, if you have installed Version 10.3 of the Vulnerability Response application, you can request policy exceptions using the GRC policy exception management capability inherent in the Policy and Compliance Management application. The procedure below is not necessary requesting policy exceptions from Vulnerability Response as the UI action is automatically installed.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **UI Actions**.

2.  Select the table on which you want to create the UI action.

3.  Click **New**.

4.  Create a new UI action with the following parameters:

    -   **Name**: Request policy exception
    -   **Show update** check box: Selected.
    -   **Form button** check box: Selected.
    -   **Onclick**: Type the `popupDispList()` function call.

        **Note:** This field is available only when **Client** option is selected.

    -   **Condition**: Apply any conditions you require.
    -   **Script**: Enter this script:

        ```
        function popupDispList(){
        
                    ScriptLoader.getScripts(['sn_compliance.PolicyExceptionUtils.jsdbx'], function() {
        
                                sn_compliance.PolicyExceptionUtils.createPolicyException('incident');   
        
                    }); 
        
         
        
        }
        
        ```

        **Note:** The argument for the `createPolicyException` function varies based on the integration.

5.  Save the UI action.

6.  To create a new list view to see policy exception target records on the Policy Exception form, see [KB0783018](https://support.servicenow.com/kb_view.do?sysparm_article=KB0783018).


**Parent Topic:**[Allow policy exception requests from other applications](../concept/allow-other-app-policy-except.md)

