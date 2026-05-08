---
title: Enable integration with Microsoft Dynamics CRM
description: Integrating your ServiceNow instance with the Microsoft Dynamics CRM platform enables seamless data exchange and process synchronization between the two platforms. This integration is done through the Microsoft Dynamics CRM spoke.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Customer success, Customer Success Management, Customer Success Management]
---

# Enable integration with Microsoft Dynamics CRM

Integrating your ServiceNow instance with the Microsoft Dynamics CRM platform enables seamless data exchange and process synchronization between the two platforms. This integration is done through the Microsoft Dynamics CRM spoke.

By enabling integration of the Microsoft Dynamics CRM platform during the engagement lifecycle you can track renewals, assess risks, and create renewal opportunities. The Microsoft Dynamics CRM integration is available with the Customer Success Management application and can be configured to work with other CRM platforms.

The following use cases are supported:

-   Creating opportunity for renewals from renewal playbooks.
-   Creating task from risk record when renewal date is missing in the account.
-   Updating the ServiceNow records when any change is made to the CRM task table.

To set up the integration, follow these steps:

**Note:** Before you set the integration, you must configured the Recommended Actions application. See [Set up recommended actions for account onboarding](../task/account-lifecycle-setup-rec-action.md) for details.

1.  Set up the Microsoft Dynamics CRM spoke. See Microsoft Dynamics CRM Spoke for details.
2.  On the Microsoft Dynamics CRM platform, you must do the following:

    -   Create an account with the same name as the account associated with your internal play task.

        Before creating an opportunity from an internal play task, make a note of the account associated with the task.

        ![Internal play task - account](../image/account-lifecycle-crm-integ-play-task-assn.png)

        Before creating a task from the risk signal, make a note of the account associated with Risk and Issue record as shown below.

        ![Risk and Issue - account](../image/account-lifecycle-crm-integ-risk-sign-assn.png)

        In the Microsoft Dynamics CRM platform, you must create an account with the same account name \(**Genixify**\) associated with your internal play task as shown in the above examples. This account must be configured later in the mapping file.

    -   Create currencies that correspond to the currencies in the Customer contracts table. While creating currencies, you must add the name of the currency with the symbol in the `TechOnbConstants` script include as follows:

        ```
        TechOnbConstants.MS_DYNAMICS_CRM_CURRENCY = {
            '£': 'CURRENCY_GBP',
            '$': 'CURRENCY_USD',
            '€': 'CURRENCY_EUR',
            '¥': 'CURRENCY_JPY',
            'CHF': 'CURRENCY_CHF'
        };
        ```

    **Note:** Use the **DynamicsCRMMappingConstants** script include to define mappings between ServiceNow Sys IDs and their corresponding GUIDs in Microsoft Dynamics CRM.

    Sample mappings are shown in the following image.

    ![Dynamics CRM script include](../image/account-lifecycle-crm-script-include.png)

3.  Update the `getRiskSysIdFromCRMRequest()` function in the `DynamicsCRMTaskUpdateHandlerUtilOOB` script include to handle the task updates from Microsoft Dynamics CRM by processing the input parameters and updating the associated risk signal record.

    The Process Task Update Event demo action can be further configured and added as part of sub flow which you would need to create and add it in the decision table \(Dynamics CRM Webhook Decision Policy\) of Microsoft Dynamics CRM Spoke.

4.  \(Optional\) You can optionally configure an UI action to create a CRM task in your ServiceNow instance.
5.  Use the `AleCRMUtilOOB` script include to interact with CRM platforms like Microsoft Dynamics CRM.

    Use The `executeAction` function perform actions like creating opportunities or tasks on the CRM platform.

    ```
    executeAction(CRMPlatformName, action, recordData)
    where 
    - CRMPlatformName is the name of the CRM platform on actions are to be performed.
    - action is the action to be performed 
    - recordData is the SysID of the risk signal record that is updated when the action is performed.
    
    ```


The following examples show how you can create an opportunity or a task in Microsoft Dynamics CRM:

-   **Creating an Opportunity in Microsoft Dynamics CRM**:

    ```
    var aleCRMUtil = new AleCRMUtil();
    
    var CRMPlatformName = 'MS_DYNAMICS';
    var action = 'OpportunityCreationWithSpoke';
    var recordData = { internalPlayTaskSysId: '02de3efaeb3d5a10ddd6f94fbad0cd16' };
    
    var response = aleCRMUtil.executeAction(CRMPlatformName, action, recordData);
    
    gs.info('Opportunity Creation Response: ' + JSON.stringify(response));
    
    ```

-   **Creating a Task in Microsoft Dynamics CRM**

    ```
    var aleCRMUtil = new AleCRMUtil();
    
    var CRMPlatformName = 'MS_DYNAMICS';
    var action = 'TaskCreationWithSpoke';
    var recordData = { riskSignalIssuesSysId: 'b07062b53ba29a10be57327aa5e45a0c' };
    
    var response = aleCRMUtil.executeAction(CRMPlatformName, action, recordData);
    
    gs.info('Task Creation Response: ' + JSON.stringify(response));
    
    ```


After you have setup the integration, you can do the following:

-   [Create an opportunity in Microsoft Dynamics CRM](../task/account-lifecycle-create-crm-opportunity.md)
-   [Create a task in Microsoft Dynamics CRM](../task/account-lifecycle-create-crm-task.md)

-   **[Create an opportunity in Microsoft Dynamics CRM](../task/account-lifecycle-create-crm-opportunity.md)**  
Create a renewal opportunity in the Microsoft Dynamics CRM platform from your ServiceNow instance.
-   **[Create a task in Microsoft Dynamics CRM](../task/account-lifecycle-create-crm-task.md)**  
Create a task in the Microsoft Dynamics CRM platform from your ServiceNow instance and receive updates to the task in your ServiceNow instance.

**Parent Topic:**[Customer success](account-lifecycle-config-cust-success.md)

