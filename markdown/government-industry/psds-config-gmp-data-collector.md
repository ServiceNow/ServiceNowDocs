---
title: Create a case data collector for a PaCE policy in Grants Management
description: Create a data collector within PaCE to use a set of data within a policy.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-12-02"
reading_time_minutes: 2
breadcrumb: [Configure Eligibility Rules Engine Policies, Configure PaCE Eligibility Framework Engine, Grants Management, Playbooks and Solutions, Configure agent workspaces, Configure, Public Sector Digital Services \(PSDS\)]
---

# Create a case data collector for a PaCE policy in Grants Management

Create a data collector within PaCE to use a set of data within a policy.

## About this task

Data collectors collect input process data from within your organization or from a provided external data source to provide an output that can be used in the policy logic to make a decision. This will be used when creating a policy and referencing fields that need to be calculated or cannot be dot walked from the case. You can define and manage data collectors by creating, editing, updating, and activating them to your policy builder.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Workspaces** &gt; **CSM Configurable Workspace**.

2.  From the CSM Configurable Workspace sidebar, navigate to the **Policy Home**.

3.  In the Variable Definition list, select the **Data Collectors** list.

4.  Select **New** to create a data collector.

5.  Enter the name of the data collector and a description, then select **Save**.

6.  Select **Save**.

7.  Select the **Versions \(1\)** related list, and select **Draft-V0.1**.

8.  Select the **Build** tab.

9.  Under Define Variables, select **Add** to add an input variable.

10. On the form, fill in the fields with the following information.

    |Field|Value|
    |-----|-----|
    |Label|Label of the input variable.|
    |Name|The name of the output variable used within the data collector script.|
    |Type|The input variable data type. This can be reference, string, int.|
    |Description|The description of what this input variable is used for.|
    |Table|Table referenced for the input variable|

11. Under Define Variables, select the Output tab, then select **Add** to add an output variable.

12. On the form, fill in the fields with the following information.

    |Field|Value|
    |-----|-----|
    |Label|The label of the output variable|
    |Name|The name of the output variable used within the data collector script|
    |Type|The data type of the output variable. This can be reference, integer, string/|
    |Description|This is the description of the output variable.|

13. Under Data collector script, enter the following code snippet:

    ```
    (function(inputs, outputs) { 
        var totalGrossIncome = 0; 
     
        var incomeDetailsGr = new GlideRecord("sn_svc_appl_info_income_details"); 
        incomeDetailsGr.addQuery("case_record", inputs.case.sys_id); 
        incomeDetailsGr.query(); 
        //Loop through each income details record for the case 
        while (incomeDetailsGr.next()) { 
            var tempPaymentFrequency = incomeDetailsGr.getValue("payment_frequency"); 
             
            if(tempPaymentFrequency == "every_2_weeks") 
              totalGrossIncome += incomeDetailsGr.amount * 2; 
            else if(tempPaymentFrequency == "weekly") 
              totalGrossIncome += incomeDetailsGr.amount * 4; 
            else if(tempPaymentFrequency == "once_a_year") 
              totalGrossIncome += incomeDetailsGr.amount/12; 
            else 
              totalGrossIncome += incomeDetailsGr.amount; 
        } 
     
        outputs.total_gross_income = totalGrossIncome; 
    })(inputs, outputs);
    
    ```

14. Select **Save**, then select **Publish**.

15. Select the checkbox next to **Activate this data collector** and then select **Publish**.


## Result

A data collector for a policy version is now created.

**Parent Topic:**[Configure Eligibility Rules Engine Policies in Grants Management](../task/psds-config-gmp-eligibility.md)

